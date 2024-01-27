---
layout: project
type: project
image: img/pitchkeyslogo.jpg
title: "Pitchkeys Official Website"
date: 2023-03-01
published: true
labels:
  - MongoDB
  - Express.js
  - React.js
  - Node.js
summary: "A fullstack website that allows visitors to my YouTube channel to download the music I create and transcribe."
---

## About

This is a fullstack, responsive website that allows visitors to my YouTube channel to download the music I create. Users can sort and filter songs by keyword, bpm, genre, duration, rating, artist, etc..., and can also submit ratings for the songs. This is the first fullstack web application I created.

You can view the site here: [pitchkeys.github.io](https://pitchkeys.github.io/)

More specifically, users can download the mp3, MIDI, the MuseScore file (to edit MIDI), or the sheet music (if applicable) of each song.

## Technical Details

While creating this site, I learned the basics of React.js to build the UI, and was able to implement what I learned about basic backend development from [FreeCodeCamp](https://freecodecamp.org). All songs' info are stored in a MongoDB database, and I was successfully able to design a simple API using Express.js to retrieve the proper requested songs from the database. 

Sample API call in Express.js
```
app.post('/api/songs/:link/add', (req, res) => {
    Songs.findOneAndUpdate({generatedLink: "/" + req.params.link}, req.body, {returnOriginal: false}, (err, data) => {
        res.header('Access-Control-Allow-Origin', '*');
        res.send(data);
    })
})
```

MongoDB Schema for one song.
```
const song = new mongoose.Schema({
    songname: String,
    date: Number,
    desc: String,
    duration: Number,
    bpm: Number,
    notecount: Number,
    filters: String,
    keywords: [String],
    generatedLink: String,
    credits: {
        link: [String],
        textToDisplay: String,
    },

    download: {
        audioLink: String,
        midiLink: String,
        msczLink: String,
        ytLink: String,
        sheetMusic: String,
        coverImage: String,
    },

    stats: {
        ratings: [String],
        midiDownloads: Number,
        mp3Downloads: Number,
        msczDownloads: Number,
        pdfDownloads: Number,
        visits: Number,  
    },
})
```

I've mentioned above that users can sort and filter songs by criteria. There were "simple" criteria that could be filtered out via the MongoDB document directly by using a basic query, such as song name, date, number of notes, or bpm. On the other hand, there were "complex" criteria that needed further processing from MongoDB, such as total number of downloads (computed from summing the `midiDownloads`, `mp3Downloads`, `msczDownloads`, `pdfDownloads` fields), the average ratings (computed from averaging the ratings in the `ratings` field), or keywords (where users can type into a search bar, and an algorithm matches how close the query is to the list of keywords in the document, and returns them sorted by similarity).

The "simple" criteria were processed by directly filtering the documents out using MongoDB's built-in filtering commands, such as 
`Songs.find({notecount: {$gte: 400, $lte: 10000}, () => {...});`
This allowed processing & filtering to happen on the backend, and once the data was recieved on the frontend, no more processing was needed.

On the other hand, the "complex" criteria were processed by obtaining the entire MongoDB database via single API call, and processing it on the frontend (due to need for computation). No processing occurred in the backend. 

## Challenges
**Learning React**. This was my first project I used React.js for, and it had a steep learning curve, such as using functional and class-based components. I especially had a lot of trouble with setting `State` to the data recieved by the API calls, and it took multiple tries to make the application not jittery.

**Linking frontend with backend.** This was also my first fullstack application. Initially, I had two folders in my project: `/api` and `/client`. `/client` was where all the React components were stored, and `/api` was where my API code was stored. However, no amount of troubleshooting would allow me to make an API call to the code in the `/api` folder from the `/client` folder when developing locally. Thus, I ended up copying the `/api` folder into another separate project, and deployed that standalone API on Heroku. I was then able to successfully call the API from the `/client` folder now that they were in two separate projects.

## Images

<img width = "30%" src="../img/pitchkeys_mongodb.png">
MongoDB document.
<br><br>
<img width = "30%" src="../img/pitchkeys_find.png">
Song search page.
<br><br>
