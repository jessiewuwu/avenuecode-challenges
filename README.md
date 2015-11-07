# Avenue Code UI Challenge - Part I #


### How to compile and run the application.
1. In your terminal, go to the directory where you want to download this repo.
2. To clone the repo, enter this in your termina: `https://jessiewuwu@bitbucket.org/jessiewuwu/ui-challenge.git`
3. Open the app in your browser either by entering `open index.html` in your terminal or by locating the directory in your Finder and double-clicking index.html.
4. Because everything is set up with CDN links and everything needed is in the directory, you don't need to install anything.

## How to run the suite of automated tests
* Testing is done in Jasmine, a Behavior-Driven-Development testing framework.
1. In your terminal, go to the js folder and open SpecRunner.html.
2. To see the tests, go to js > spec > ModelSpec.js

## Technologies and Libraries Used
* Backbone - I recently started studying Backbone and enjoy the simplicity of it.
* jQuery + Ajax - These two are my two absolute favorite things to do. I love being able to manipulate elements and data and if I could, I'd do jQuery and Ajax all day!
* Bootstrap for grid columns and responsiveness, along with media queries
* SASS - I used SASS mostly for the variables and nesting. SASS is so important because it makes CSS seem like a programming language by adding logic to it.
* Jasmine - Jasmine is very similar to rspec, a testing tool that we worked with a lot during Dev Bootcamp and I love how the tests are displayed in the browser, unlike rspec in the console.

## To-Do's
* Add more design to the app based on my mockup:
![mockup](imgs/geolocationmockup.jpg)

* Currently, when we have the company location and user's location, the map only focuses on the location that was last clicked. I was able to pseudocode a possible way to add boundaries and have both pinpoints in the map. In geolocation.js, on line 28 and 29, I determined the bounds so that map could fit to these bounds and added another feature where it would zoom out to include these bounds.
* For the Locate click event, it works with jQuery where when you click the Locate button, it does an API call based on the url input field. However, with Backbone events, it is not firing off. I've left the pseudocdoe for the events function syntax in line 158 of geolocation.js file.
* The given GeoIP API doesn't give an exact latitude and longitude because it rounds up after the tenth decimal, which makes the location inaccurate by a few blocks.
  - Possible Solution - find a better API that gives exact latitude and longitude. Ideally it would also be nice to get the physical address of the location so that the user can also have that information, rather than just a pinpoint in the map.
  - Possible Solution - instead of using a pinpoint, use a circle range to cover a broad area (about 5x5 block radius). However, this would be a huge circle so the first solution may be more ideal.
* After clicking Reset Location (without looking up a company URL), the Map pinpoints the ocean. Instead, it should zoom out and center on the entire United States. I tried looking into this and believe this would require another function that takes zoom integer into consideration. Right now the initialize function that runs the Google Maps API is hardcoded with zoom integer of 12. Since the United States is quite big, we would have to zoom out.
* Jasmine Testing - I will admit, testing is not my strongest suit. It is definitely something I feel is very valuable to programming because it checks for quality, working code in the long run. I learned Jasmine over a span or one or two days during Dev Bootcamp and unfortunately it was something we didn't prioritize for our final project, so I didn't have as much exposure and practice as I liked.

- For this app, I wanted to test Ajax with Jasmine so I started looking into Jasmine spies. On Jasmine's github, there was documentation on using mock Ajax to test the data received from API's. Although I wasn't able to successfully implement this with the given time, I feel like I am able to do it looking at more resources on my own or pairing with an engineer.

- Testing is something I plan on diving deeper and perfecting. I am adding more projects to my portofolio and will be doing test-driven-development. I am pretty confident with enough practice, I can write tests in my sleep. I believe I have the foundation in testing but just need a bit more practice and room before I can spread my wings, or as R. Kelly would say "If I can see it, then I can do it (I can do it). If I just believe it, there's nothing to it. I believe I can fly"












