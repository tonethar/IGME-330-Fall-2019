# Week 6A - Wrap up Modules / Look at Audio Visualizer Prototypes



## I. Review Questions (ES6 Modules) <a id="review-questions"></a>

1) **True or False.** With JavaScript ES Module syntax, there is exactly one module per file and one file per module

2) **True or False.** One disadvantage of ES6 modules is that in general you will need to have a lot more &lt;script> tags in your HTML file

3) How do you "tell" your HTML file that a particular JavaScript file is an ES6 Module (as opposed to being a regular JS file)? 

4) **True or False.** JavaScript code written inside of an ES6 Module runs in *strict mode* by default

5) **True or False.** JavaScript code written inside of an ES6 Module is *private* (not visible from outside the module) by default. This includes variables & functions declared with `let, `var`, and `const`, as well as functions declared with the `function` keyword

6) **True or False.** It is possible to create a *global* variable (i.e. visible on the `window` object) from within an ES6 Module

7) *Modular programming* is the process of subdividing a computer program into separate sub-programs. Modules have the following characteristics:

    A) enforce logical boundaries between components and improve maintainability
  
    B) are implemented through interfaces (i.e. publicly available methods or properties)
  
    C) are designed in such a way as to minimize dependencies between different modules

- **Describe how A above is reflected in ES6 Modules**
- **Describe how B above is reflected in ES6 Module Syntax (*i.e. which keyword?*)**
- **Describe how C above is reflected in ES6 Module Syntax (*i.e. which keyword?*)**

## II. Writing maintainable code

- The Audio Visualizer HW code is "not scalable" demo code. It should be refactored when used in your Project 1's - let's look at some examples of things we could do:

### II-A. Custom `audioGraph` object literal

- The main **index.html** page of the AudioVisualizer HW has a bunch of variables cluttering up the code:
- How about wrapping all of those up into an object, and pushing off the creation code into another 

**audio-utils.js**
```js
export {createAudioGraph};

function createAudioGraph(){
  let audioGraph = {};
	audioGraph.ctx = ///
	audioGraph.analyzerNode = //
	audioGraph.trebleNode = //
	
	return Object.freeze(audioGraph);
}
```

**main.js**
```
// main.js
import {createAudioGraph} from "./audio-utils.js"

let myAudioGraph = createAudioGraph();
```

## III. Project 1
- Look at [Project 1 - Audio Visualizer](../projects/project-1.md) prototypes



<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-05B-notes.md**](week-05B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-06B-notes.md**](week-06B-notes.md)
