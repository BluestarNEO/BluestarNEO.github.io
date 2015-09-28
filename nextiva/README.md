# Nextiva Test Marketing Site  
  
Welcome! The Following are just a few notes on the decisions I made and how I built this project.

###Responsiveness  
- Used 3 common break points for responsive sizing  
   1.) Under 640px    
   2.) Between 640px and 1024px  
   3.) Greater than 1024px  

###Optimized Images
- Images have been further optimized for faster loading through use of direct sizing depending on
viewport size and compression

###Retina Quality
- Images are double sized within containers for double pixel density devices

###Notes
- Lato was the provided font in the style.css file originally, so the website was created using that 
as the selected font. However, the source URLs for the fonts would not work at my location, so I
brought the Lato font in through a Google fonts link in the inex.html

- Also CDN'd Normalize.css for baseline CSS templating on index.html

- The bit of markup at the top of my index.html file that says 'permalink: /nextiva/' is for the use
of correctly routing through my Jekyll instance (which I use as the platform for my main site)
