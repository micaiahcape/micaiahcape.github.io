---
layout: project
type: project
image: img/stravalytics.png
title: "Stravalytics (In Progress)"
date: 2023-09-01
published: true
labels:
  - JavaScript
  - Node.js
  - MongoDB
summary: "A web application that allows you to view your Strava (a fitness tracker) data in great detail via different visualizations."
---
## How to use
Stravalytics is a web application that I built where users can connect their Strava (a fitness app) and analyze their running data in detail. When on the site, simply connect the "Connect to Strava" button to link your Strava accounts, and see your statistics via beautiful visualizations!

You can view the site here: [stravalytics.cyclic.cloud](https://stravalytics.cyclic.cloud/)

## How the application works
A user connects their Strava account, and a call is made to the Strava API to retrieve all their activities (greatly simplified; see how authentication works in the next section). Once a user connects their Strava account, LocalStorage and MongoDB is used to keep them "logged in" to prevent them from having to connect their Strava account again (unless they decide to "logout" and disconnect it). When the API returns back the data, it is sorted and displayed in many different visualizations. Users can tinker with the numbers, such as displaying different variables, filtering displayed activities out by date, or changing the zoom on the visualizations.

## How authentication works

### The short version

1. Obtain authorization code by connecting Stravalytics to Strava.
2. Make an API call to strava using this authorization code. A `refreshToken` is returned.
3a. If the returned `refreshToken` does not exist in database, create new document with a unique user ID and `refreshToken`. Store `refreshToken` in `localStorage`.
3b. If the returned `refreshToken` exists in database, simply store `refreshToken` in `localStorage`.
4. Make an API call to Strava using `refreshToken`. This returns an `accessToken`.
5. Stravalytics finally makes more API calls using the `accessToken` to get users' activities.

### The long version

The Strava API has two components that are required to get an athlete's data: a `refreshToken` and `accessToken`. `accessToken` is a temporary (short-lived) string used to retrieve the user's data, and `refreshToken` is a string that generates `accessToken`s. When a user connects Stravalytics with their Strava account, the user is redirected to Strava's login page, where they must input their Strava email and password. Upon successful authentication, the user is redirected back to Stravalytics with an authorization code in the URL. It looks like this:

```
https://stravalytics.cyclic.cloud/?state=&code=bdd55c5743cea421e334fef3f168cd5372ffa433&scope=read,activity:read_all
```

Automatically, the application makes an API call to the Strava API call with the code `bdd55c5743cea421e334fef3f168cd5372ffa433` (in this example). The API call from Strava returns the user's account information, such as name and their `refreshToken`.

The application stores unique user IDs and `refreshToken`s in a mongoDB database. 

```
_id: 64e1c5ae2dc716ba9e33e3f2 // unique user ID
refreshToken: "34900da21faf4931efbd143c32b437a5812b383f" // refresh token
__v: 0
```

When the obtained refreshToken can't be found in the database, it means that a new user is trying to connect their account. Thus, a new document is created in MongoDB, with a randomly generated unique user ID and their `refreshToken`. This randomly generated user ID is also stored in browser `localStorage` so that a user can "stay logged in." In other words, when a user closes the tab and returns to the website, the user ID in `localStorage` can be used to find a mongoDB document containing their `refreshToken`.

A second API call is made to Strava with the `refreshToken`, and an `accessToken` is obtained. 

Using the obtained `accessToken`, the application finally starts calling the Strava API to get the user's activities

## Stravalytics currently has the following visualizations:
<img class="img-fluid" width = "30%" src="../img/stravalytics.png">
* Histograms that sort your activities by pace, elevation gain, distance, and uptime.
<br><br>
<img class="img-fluid" width = "30%" src="../img/stravalytics_scatter.png">
* An interactive scatterplot that allows you to analyze relationship between many different variables, such as cadence, stride length, distance, heart rate, elevation gain, etc...
<br><br>
<img class="img-fluid" width = "30%" src="../img/stravalytics_line.png">
* Totals, averages, and moving averages of most run statistics, visualized by line graphs!
<br><br>

* Analyzing a single week, month, or year's worth of activities in detail (coming soon)

## Challenges
* As the UI got more complicated, there were more graphs to render upon every refresh (especially the anychart.js line graphs take a relatively long time to render compared to using the DOM.) I'm still working on resolving this issue - on a laptop it can take up to only 1 second to re-render the whole UI; however on lowend devices like my phone it takes up to 4 seconds, which is very noticable.
* Integrating the Strava API into my application. Documentation online was limited and was confusing to some degree, which forced me to look up YouTube tutorials on how to do it. After several nights, I as finally able to make the first Strava API call using this application. A few more nights of tinkering and I successfully was able to make it so that all users can connect their Strava account and view their statistics.
* Deployment. I used [Cyclic.sh](https://cyclic.sh), which is a free, quick hosting service. This was the very first time both my API and my frontend were in a single project (the previously mentioned [PitchKeys website](https://pitchkeys.github.io) actually used an external API that I deployed separately). Thus, I needed to work around a lot of error messages during deployment.



