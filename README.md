### General Assembly Project-2: React based website that comsumes a public API
# ITVDB (Internet TV Database)
A TV show database where you can discover and favorite series.  
Contributors: [Mayur Kumar](https://github.com/Kumasta), [Bashar Othman](https://github.com/greenplastic90) 
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

The nav bar is fairly simple with 3 main buttons The brand/home page link, the TV show list and favourites pages can all be accessed from here. All the button have a hover a effect of inversive the text and border colour. The home page is made up of a random array of TV show images with a check to make sure each one is unique. On page load it will display a random number of TV show images displaying them in a container that spans the screen. A div in the middle has a black transparent background to enable users to see images behind it but also ease of readability of the site name text. A button below acts as the same link as the TV shows button in the nav bar.    
<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134134-1cf7e5e9-5d3e-43d6-aec4-9de0c5ca97bf.png">

### TV shows page

All TV shows are pulled from a GET request from the API and map in a container in our card component, the card will show basic information including the name, image and average score of the TV show as well as a favourite button.
<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134121-38ebb398-3c49-4098-9ec2-6faa581b578f.png">

### Search bar

The search bar allows for real time filtering of TV shows by text and genres selected from the drop down box. The search/filter uses RegEx to convert search text and results into lowercase and remove all spaces to allow for slightly more lenient search results. 

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134308-50bb2345-b03b-4be6-a3ef-d1b9a212269c.png">

### Favourites page

On click, the favourite button will change background from a normal emoji face to a heart one or vice versa. This will trigger a function that will check an array of Ids saved in local storage. If the id of that TV show is not in the array, it will be added and local storage is updated, on second click, the array is checked to see if that id is present and will find the index of it and remove it. The favourite state of the card is checked on page load to see if the icon needs to be altered or not. Any show that is favorited will then be seen on the favourites page that can be accessed from the nav bar like below: 
 
<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134175-ed580fc3-baac-44a9-a234-13d310dfab09.png">

### Side card

On the TV shows page or the favourites page, clicking on a card will display more information about the show on the side card such as the genres, network and show status. at the bottom is a link that will take you to the show single showcase page for even more information. In practice, this system was not very intuitive and visually unappealing as you would need to click on two places, the card and then the side card, to get to the showcase page. 

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134212-b54bbd23-a39f-4618-8c6b-b5447b030a5c.png">

### Showcase

Here on the showcase page you will see the most information about any show by using the id to make another GET request from another API endpoint. along with a higher quality image of what you see on the cards and front page. 

<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134226-79fd3fc6-ee83-4d02-a9a3-dec4dca36d94.png">

### Cast list

Using the third and last API endpoint, we get the cast details and map them through another card component at the bottom of the page. 


<img width="80%" alt="image" src="https://user-images.githubusercontent.com/94964514/159134251-aa574052-d821-4a78-bcc7-0081aa7ae09f.png">

## Challenges 
- As this was one of our first times using local storage, we had bugs when creating the favourite system. It was a good experience to go through as we better understand how to use local storage. 
- The site was not built with mobile in mind and some of the components such as the side card are not displayed well in mobile view.
- Time, this was only a 2 day project and we felt rushed for time and some things we wanted to implement were not done.
- Styling bootstrap components was a challenge as they would be hard to target, we would learn that using !important would be a good way to override native styling properties of them.
- VS code live share is good but not very responsive for us as the person joining a session at times. When one person would code in an error, the others would have the error too on the page and not be able to see their webpage until the bug was fixed. 

  
## Future Improvements 
- Make it mobile responsive.
- Remove or alter side cards to be more practical and user friendly.
- Add dynamic changes to the home screen random show banner with transition animations. So a show image will fade one at a time and a new one will pop fade in. 
- Integrate a back-end API server to allow users to create accounts and log in to save there favourites to there account and not just the browser/machine they are using.  
- Add fullness to the search bar.   
- Make the site mobile friendly. 

## Main Takeaways 
- Using a git repo and push and pull branches would be more efficient to avoid lag with Live share.
- Design with mobile in mind from the start.
- Plan out the components of a project and divide them up and allocate to each person to avoid conflicts or wasted time.

  
## Contact

Social - https://www.linkedin.com/in/mayur-kumar-dev/

email - mayurkumardev@googlemail.com

Project Link: https://itvdb-sei61.netlify.app/

Git Hub: https://github.com/Kumasta

<p align="right">(<a href="#general-assembly-project-2-react-based-website-that-comsumes-a-public-api">back to top</a>)</p>

