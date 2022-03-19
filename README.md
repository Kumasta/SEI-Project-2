### General Assembly Project-2: React based website that comsumes a public API
# ITVDB (Internet TV Database)
A TV show database where you can discover and favorite series. 
### Project Link : https://itvdb-sei61.netlify.app/

<img width="1680" alt="image" src="https://user-images.githubusercontent.com/94964514/159133803-8275bc53-643d-400d-8d7a-1b409b6a828d.png">


## Table of Contents

- [Brief](#brief)
- [Concept](#concept)
- [Built With](#built-with)
- [Approach](#approach)
  - [Planning](#planning)
    - [API](#api)
    - [Wire Frame](#wire-frame)
- [Section Breakdown](#section-breakdown)
- [Challenges](#challenges)
- [Future Improvments](#future-improvements)
- [Main Takeaways](#main-takeaways)
- [Contact](#contact)


## Brief
This is the second project in the course, the aim is to **build a React application** that consumes a **public API**. The app must also be made of several **components** and be made up of **several pages**. This was the first project that will be built in a pair.  


## Concept
We brainstormed a few different APIs to build a website with and in the end we choose to go with a TV show API from TVMAZE.com   
We would use this API to create a site like IMDB but for TV shows where users could browse the database and favourite shows that would display on another page. We decided to build the structure of the site with bootstrap and add our own custom colour theme and styling. 


## Built With
This project was built using following languages and packages:

* React
* CSS/SASS
* JavaScript
* Axios
* Bootstrap
* React-bootstrap
* React-dom
* React-router-dom

## Approach

As we were working in a pair, we decided to use VS Code's live share feature to work on the same project file at one time. We started with choosing the public API before we went into the rough design of the site with a wireframe. 


### Planning

#### API
TV mazes API reasouce is very extensive with many endpoints.  
<img width="607" alt="image" src="https://user-images.githubusercontent.com/94964514/159134394-d5c6c1e8-7a90-43ed-93ec-7bbba53ac623.png">   
Link: https://www.tvmaze.com/api    

After going through the different endpoints and their outputs we settled on 3. To get all base data for all shows and then for further detail for each the end points for information about a show's seasons and the cast. As this was a 2 day project we felt that this would be enough to work with.  
<img width="244" alt="image" src="https://user-images.githubusercontent.com/94964514/159134433-8e5930c4-bdad-4c8b-b865-538cce9a074a.png">


#### Wire Frame

We then created our wireframe of the site. We knew we wanted to try a side card system to display more information about each show before going to the showcase of that show. We also knew we would need a simple card to display shows in a list that would be used in several places. We were unsure where the search bar would be used, In the end we settled on using the search bar on one page for the timescale of this project. 

![wireframe](https://user-images.githubusercontent.com/94964514/159134675-66aee7ee-b722-44fd-9165-3bb664345d7b.png)

## Section Breakdown

### Nav bar and home page

The nave bar is fairly simple with 3 main buttons The brand/home page link, the TV show list and favourites pages can all be accessed from here. All the button have a hover a effect of inversive the text and border colour. The home page is made up of a random array of TV show images with a check to make sure each one is unique. On page load it will display a random number of TV show images displaying them in a container that spans the screen. A div in the middle has a black transparent background to enable users to see images behind it but also ease of readability of the site name text. A button below acts as the same link as the TV shows button in the nav bar.    
<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134134-1cf7e5e9-5d3e-43d6-aec4-9de0c5ca97bf.png">

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134121-38ebb398-3c49-4098-9ec2-6faa581b578f.png">

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134308-50bb2345-b03b-4be6-a3ef-d1b9a212269c.png">

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134175-ed580fc3-baac-44a9-a234-13d310dfab09.png">

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134212-b54bbd23-a39f-4618-8c6b-b5447b030a5c.png">

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134226-79fd3fc6-ee83-4d02-a9a3-dec4dca36d94.png">

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134251-aa574052-d821-4a78-bcc7-0081aa7ae09f.png">

## Challenges 

  
## Future Improvements 
- Make it mobile responsive.
- Remove or alter side card to be more praticle and user freindly.
- Add dyanimic changes to the home screen random show bannar with transition animations. So a show image will fade a one at a time and a new one will pop fade in. 
- Intergrate a back-end API server to allow users to create accounts and log in to save there favorites to there account and not just the broswer/machine they are using.  
  
## Main Takeaways 

  
## Contact

Social - https://www.linkedin.com/in/mayur-kumar-dev/

email - mayurkumardev@googlemail.com

Game Link: [https://github.com/your_username/repo_name](https://kumasta.github.io/Virus-Buster/)

Git repo: https://github.com/Kumasta/Virus-Buster

<p align="right">(<a href="#general-assembly-project-1-web-browser-game">back to top</a>)</p>

