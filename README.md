### ![GA](https://cloud.githubusercontent.com/assets/40461/8183776/469f976e-1432-11e5-8199-6ac91363302b.png) General Assembly, Software Engineering Immersive

# Stop, Think & Go!


## Overview 

This is my first project that I created during the Software Engineering Course at GA in London. Originally our brief was to create a grid-based game which would be playable in the browser. We were given a wide selection of classic games to choose from which ranged in difficulty. 

I choose to create my own version of 'Frogger', a game where the goal is to guide a family of frogs home, whilst avoiding moving obstacles. However, I chose to adopt a new theme for my recreation. Based on the advert Stop, Look, Listen & Go, a series of adverts to help children learn to cross the road, my game focused on the user helping a series of hedgehogs across the road. In order to safety reach home, the user must also avoide cars, giraffes and elephants in the road, as shown in the advert.

The game allowed me to implement the front-end development skills I'd learnt since starting the course three weeks prior. In particular, the project focused on interacting with the DOM and how to make this interactive for the user when playing. 

Play the game ---> here 

## The Brief 

- **Render a game in the browser**
- **Design a logic for winning and display scores**
- **Include a seperate HTML/CSS/JavaScript files**
- **Be playable for one player**
- **The obstacles should be autogenerated**
- Stick with **KISS (Keep It Simple Stupid)** and **DRY (Don't Repeat Yourself)**
- Playable the game online **for everyone to play!**


## Technology Used 

- HTML
- CSS
- JavaScript (ES6)
- Google Fonts
- Git & GitHub
- IMGBIN

## The Approach 

### The Board

- The game itself is a 10x10 square grid, created in JavaScript. Divs are created within the JavaScript using a for loop (as shown below) and then appended to the grid as child elements. 

```js 
  const width = 10
  const gridCellCount = width * width
  const grid = document.querySelector('.grid')
  const cells = []
  let hog = 90

    for (let i = 0; i < gridCellCount; i++) {
    const cell = document.createElement('div')
    cell.classList.add('cell')
    cells.push(cell)
    grid.appendChild(cell)
    }
  ```
I have choosen to hide my grid during gameplay for styling purposes, but can be viewed below:

![](/images/gridScreenshot.png)

This shot is taken as you enter the page and as shown, I have my character and obstacles already in place. This is placed within the for loop where I created my grid. After adding my cells, I have defined an if statement within this loop for my hedgehog character to appear at the given cell I have choosen. 

```js 
let hog = 90

 if (i === hog) {
      cell.classList.add('hog')
    }
  ```







