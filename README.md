# Project Description

Our group was assigned to work on a RESTful application project. The primary objective of the project was to create an e-commerce website that allows users to register, log in, and have their own shopping basket to purchase items. 

The website is named 'Kleur', which means 'colour' in Dutch. Users can purchase colours with paint names similar to those of Farrow & Ball and Dulux. Additionally, we included an interactive feature that allows users to select a custom colour and name it whatever they wish. The custom colour is then displayed on a 3D cube rendered using react-three-fiber, a React library built on top of three.js for creating 3D graphics and animations. 

For the front-end, we used Material UI, React, TypeScript, and other libraries, such as react-three-fiber to render the 3D cube, axios for making HTTP requests to our API, and react-color for the colour picker component.

For the backend, we used Express, Node, TypeScript, MongoDB and used libraries such as bcrypt for password encryption, mongoose to interact with MongoDB and JWT for user authentication and authorization.

## If you’d like to try the code locally.

Front-End
Clone the front-end repository
Run - npm i
Add .env file (receive upon request) at the root of repository
Run - npm run dev

Back-End
Have MongoDB installed, running and using the default port 27017
Clone the back-end
Run - npm i
Add .env file (receive upon request) at the root of repository
Run - npm run seed
Run - npm run dev
You can use the URL "http://127.0.0.1:8000/api" in your preferred API testing tool and to view the available endpoints check the "views" folder.

## Timeframe
Our group, which included Rob, Lukasz, and me, had less than two weeks to complete the project. Lukasz was leading the project and made the decision for us to split up the work. He worked on the backend by himself, while Rob and I were assigned to focus on the front end since there was a significant amount of work to be done in that area.

## Technologies Used

### Back-End
- Node
- Express
- MongoDB
- TypeScript
- Insomnia

### Front-End
- React
- TypeScript
- Material UI
- Three.js 

## Project Brief

- Work in a team, using git to code collaboratively.
- Build a full-stack application by making your own backend and your own front-end
- Use an Express API to serve your data from a Mongo database
- Consume your API with a separate front-end built with React
- Be a complete product which most likely means multiple relationships and CRUD functionality for at least a couple of models
- Implement thoughtful user stories/wireframes that are significant enough to help you know which features are core MVP and which you can cut
- Have a visually impressive design to kick your portfolio up a notch and have something to wow future clients & employers. ALLOW time for this.
- Be deployed online so it's publicly accessible.
- Have automated tests for at least one RESTful resource on the back end. Improve your employability by demonstrating a good understanding of testing principles.

## Planning

As a group, we agreed to utilise Jira Software for planning our sprints, as it is one of the most commonly used project planning software for teams. It was deemed valuable to learn how to use this software, as many companies use it for their own sprints.

{image}

To aid in determining and conceptualising the requirements for the website, we utilised Excalidraw to create a wireframe of the project and also generated some pseudocode.

{image}

{image}

### Splitting Tasks

We opted to divide our project into two primary sprints - one for Front-End and one for Back-End - and established tasks based on the features that our website required.
For this project, my responsibilities included developing the UI/UX design using Figma, utilising MUI to replicate the Figma design, implementing Three.js for website interactivity, and creating React components.
Meanwhile, Rob was tasked with mastering MUI, building React components, and assisting Lukasz with backend development. Lukasz, on the other hand, was responsible for designing the backend, including creating the ERD, and developing endpoints and middlewares, among other related duties.

## Coding Process

### Figma

As Rob and Lukasz were setting up the project's framework and Github, I worked on designing the website's UX/UI using Figma. I allowed myself a three-day window to finish the task since I required time to understand the fundamentals of UX/UI.

{image}

View this in detail here: Figma link

### Colour Picker

To enable the user to select a colour of their preference and to facilitate interactivity in one of the functionalities of the project, a colour picker was required. For this purpose, the react-color library was selected, as it appeared to be the most suitable option to achieve the desired outcome. Although the library offers numerous components, only two were needed - the hue picker for primary colours and an alpha picker for opacity, which enabled the selection of various shades of primary colours. The Hue component presented a slider that, when clicked, returned an array of colour formats such as HEX, RGBA, HSL, and HSV. Similarly, the Alpha component offered a slider that utilised the alpha value of the colour formats provided by the Hue component. The selected colour and alpha value were then stored in the state to enable real-time colour changes.

### Three.js
As someone with a background in 3D animation, I was particularly excited about using the react-three-fiber library for a project that involved rendering and manipulating a 3D cube's colour using a colour picker. Since this was a React project, react-three-fiber proved to be more convenient than using Three.js, as it offered a variety of helpful components that did not require classes.
One of the most useful components provided by react-three-fiber is the canvas component, which is similar to the HTML canvas but designed specifically for drawing 3D graphics. This canvas allows you to set up your 3D scene by incorporating elements such as 3D assets, lighting, orbit controls, and even physics.

To integrate the colour picker's variable into the 3D cube's colour, I passed the stored colour variable as a prop to the cube component.




### Carousel

Our aim was to incorporate a carousel feature for the product's image. However, as MUI didn't have a carousel library, I came across a useful MUI carousel library. The Collections component was utilised to retrieve the products from our API. Subsequently, I utilised the ProductCard component to map all the information and present the product layout. In this component, I integrated the react material UI carousel component, which has numerous props to modify the carousel layout. Additionally, I utilised another component to map the images array as props to display the images. I also passed the product ID as a prop to the component to make the product image clickable and redirect to a single page featuring the product.

## Challenges

### TypeScript

In this project, using TypeScript proved to be a major obstacle. Although the libraries I employed had their own interfaces and types, some of them were ineffective. I spent a few hours attempting to modify one of the types, but no luck. However, based on past experiences, I was aware that TypeScript can be time-consuming, so I made a conscious decision to leave comments above any unresolved issues and address them at a later time.

### MUI

In my opinion, MUI is the superior library for creating user interfaces. However, one area where they fall short is the absence of clear documentation on the most effective component configurations to use together. For example, it can be unclear whether to use container and box or container and grid. Additionally, I found it challenging to understand how responsiveness works within the MUI library. This has resulted in some issues with the website's responsiveness, such as when the web page is shrunk horizontally, causing all the text to stack on top of each other, while vertical shrinking works as intended.
Another challenge we encountered with MUI was the multitude of ways to style the components, making it difficult to determine the most effective approach. To avoid creating messy and disorganised code, we ultimately decided to stick to one consistent method of styling the components.


### Colour Picker

During the project, I encountered a technical issue related to the colour picker component. Specifically, there was a delay in the display of the selected colour, which only appeared after the page was refreshed or after selecting another colour. Although I was able to identify the source of the problem, the deadline for the project had already been reached, and I was unable to address the issue at that time.

# Challenges

### Team Work

Rob and I worked together to learn MUI, collaborating to understand how to implement it within our project. This cooperative approach hastened our learning of the library, as we each tackled different aspects of it and shared the most effective methods of working with it.

### Responsive Design

Despite time constraints preventing us from completing every page, we were able to replicate 80% of the Figma design and ensure its responsiveness. In my view, this is a significant achievement.

### 3D Environment

Ever since I began attending this boot camp, I've had the desire to incorporate a 3D element into my projects. Unfortunately, I couldn't find a suitable opportunity to do so. Fortunately, my team was supportive of my ambition to learn Three.js and integrate something engaging into our website. Ultimately, I was able to master the fundamentals of WebGL and create a 3D environment where I could construct a 3D mesh, shader, lighting, and even physics.

## Key Learnings/ Takeaways

During this project, my appreciation for teamwork has increased, as it allowed for regular feedback and support from my colleagues, resulting in a quicker project turnaround time. We held daily standups to update each other on our progress and tasks. The use of Jira was also beneficial as it facilitated the fair allocation of work and allowed us to track our progress.

Although challenging, learning MUI proved to be worthwhile as it enabled me to create visually appealing user interfaces in a more efficient manner.

The most enjoyable aspect of the project for me was learning react-three-fibre, as I had always wanted to incorporate it into a project. Being able to view a 3D scene in a web browser still amazes me. While I wish we had more time to work on it and make it more interactive with controls, unfortunately, time constraints didn't allow for it.

## Bugs

1. Delayed colour change on the front page
1. Delayed colour change on the cube
1. The opacity slider works on the front page but the slider circle doesn’t move.
1. When on a smaller screen the item isn’t exactly centred
1. Selecting a colour resets the opacity value

## Future Improvements

1. Fix spacing between texts on the main page
1. Make the custom page more presentable
1. Make single product page more presentable
1. Add more controls to the cube and buttons to reset its position
1. Find the opacity prop for the cube component
1. Working basket
1. Fix the position of the carousel arrows
1. Make footer links clickable
1. Replace ipsum lorem text with the actual text
1. Add a feature where users can create and post their own colour









