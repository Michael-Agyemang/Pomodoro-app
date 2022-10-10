# Frontend Mentor - Pomodoro app solution

This is a solution to the [Pomodoro app challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/pomodoro-app-KBFnycJ6G). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

  - [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
  - [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

The idea of a [Pomodoro technique](https://en.wikipedia.org/wiki/Pomodoro_Technique) is
that during the day you can block chunks of time of 25 minutes and try to focus on doing
one thing, without any destructions.

In the FrontendMentor's design the idea is evolved to have 3 shortcut values to
set common time-chunks of 25, 5 and 15 minutes. 

Original design providing the circled progress-bar that runs clockwise and time
decrements accordingly from 25:00 to 00:00 in the end.

Main Features:

- Ability to Start 3 types of timers
- Ability to change visual of the app
- Ability to pause, start and restart the timer


### The challenge

Users should be able to:

- Set a pomodoro timer and short & long break timers
- Customize how long each timer runs for
- See a circular progress bar that updates every minute and represents how far through their timer they are
- Customize the appearance of the app with the ability to set preferences for colors and fonts

### Screenshot

![Image of pomodoro](./assets/pomodoro1.jpg)
![Image of pomodoro form](./assets/pomodoro-form.jpg)
![Image of pomodoro with timer in motion](./assets/pomodoro-in-motion.jpg)
![Image of pomodoro in purple color](./assets/pomodoro-in-purplecolor.jpg)
![Image of pomodoro in voilet color](./assets/pomodoro-in-voiletcolor.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Javascript
- [Styled Components](https://styled-components.com/) - For styles



### What I learned

### SVG Progress Bar

One of the challenging parts of this project is the circular progress bar . I thought that with CSS building
it might be tricky and we as developers have a great SVG technology.

ATM I am not entirely happy with the result, moving between stops
are a bit chunky even with the transitions. And there are a few great
demos/articles that helped me to build this functionality


To see how you can add code snippets, see below:

```html
<svg class="progress-ring" width="272" height="272" aria-label="pomodoro clock">
        <circle class="progress-ring__circle" stroke="white" stroke-width="8" fill="transparent" r="120" cx="136"
          cy="136" />
      </svg>
```
```css
.progress-ring {
  -webkit-box-shadow: 0px 1px 5px 17px #292d53;
          box-shadow: 0px 1px 5px 17px #292d53;
  background-color: #161932;
  border-radius: 50%;
}

.progress-ring__circle {
  stroke: #F87070;
  -webkit-transition: 0.35s stroke-dashoffset;
  transition: 0.35s stroke-dashoffset;
  -webkit-transform: rotate(-90deg);
          transform: rotate(-90deg);
  -webkit-transform-origin: 50% 50%;
          transform-origin: 50% 50%;
} 
```
```js
function setProgress(percent) {
  const offset = circumference - percent / TIME_LIMIT * circumference;
  circle.style.strokeDashoffset = offset;
}
}
```

### Continued development

Ability to make values change in the application settings.


### Useful resources

- [resource 1](https://www.youtube.com/watch?v=a7Kt7S_4HOA) - This helped me understood pomodoro count. I really liked this pattern and will use it going forward.
- [resource 2](https://www.youtube.com/watch?v=MtYR2vCs2R0) - This is help me understood pomodoro start and pause concept. I'd recommend it to anyone still learning this concept.

## Author

- Website - [Michael Agyemang Duah](https://www.your-site.com) 
- Twitter - [@duahmichael3](https://www.twitter.com/duahmichael3)
- Facebook - [Michael Duah](https:www.facebook.com/MichaelDuah)



## Acknowledgments

I would like to thank Chamu Mutazva, a github User




