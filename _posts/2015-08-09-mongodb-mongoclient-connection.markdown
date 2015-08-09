---
layout: post
title:  "MongoDB MongoClient Connection"
date:   2015-08-09
categories: jekyll update
---  
I was recently working on a project where I wanted to use MongoDB and Node together. While
building the app, I came across a deprecation issue with the latest release (version 2.0.40
and up) of the Node.js driver in the npm module 'mongodb'.

First up, I will demonstrate the older, now deprecated way to connect:

    var mongoclient = new MongoClient(new Server('localhost', 27017, {native_parser: true}));
    
    var db = mongoclient.db('course');
    
    app.get('/', function(req, res) {
      res.render('hello', {'name': 'Swig'});
    });
    
    app.get('*', function(req, res) {
      res.send('Page Not Found!', 404);
    });
    
    db.open(function(err, db) {
      if(err) throw err;
    
      app.listen(8080);
      console.log('Express server started on port 8080');
    });

Now for anything equal or above version 2.0.40:

    MongoClient.connect('mongodb://localhost:27017/test', {native_parser: true}, function(err, db) {
      if(err) throw err;
    
      app.get('/', function(req, res){    
        db.collection('hello_mongo_express').findOne({}, function(err, doc) {
          res.render('hello', doc);
        });
      });
    
      app.get('/*', function(req, res){
        res.status(404).send("Page Not Found!");
      });
    
      db.open(function(err, db) {
        if(err) throw err;
    
        app.listen(8080);
        console.log("Express server started on port 8080");  
      })
    });


Essentially, the mongoclient.db() method is out, while the newer way seems to be including all
related app calls inside of MongoClient.connect(). Just a good reminder of how things change.