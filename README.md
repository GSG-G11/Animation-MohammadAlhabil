# CSS Transitions


CSS transitions allows you to change property values smoothly, over a given duration.

CSS transitions provide a way to control animation speed when changing CSS properties. Instead of having property changes take effect immediately, you can cause the changes in a property to take place over a period of time. For example, if you change the color of an element from white to black, usually the change is instantaneous. With CSS transitions enabled, changes occur at time intervals that follow an acceleration curve, all of which can be customized.

Animations that involve transitioning between two states are often called implicit transitions as the states in between the start and final states are implicitly defined by the browser.

How to Use CSS Transitions?
To create a transition effect, you must specify two things:

the CSS property you want to add an effect to
the duration of the effect
Note: If the duration part is not specified, the transition will have no effect, because the default value is 0.


how use it
```css
    .class{
        font-size: 1.1rem;
        transition-property: font-size;
        transition-duration: 4s;
        transition-timing-function: ease-in-out ;
        transition-delay: 2s;
    }
```

- property: name property or all for give all properties
- duration:  
- timing function:  
- delay:  


we can write all this rules in one line 

```css
    transition: <property> <duration> <timing-function> <delay>;
```

example
```css
   .class{
        font-size: 1.1rem;
        transition: font-size 4s ease-in-out 2s;
    }
```

transition-timing-function have some property like:

| Property        | Description     | 
| ------------- |:-------------:|
| ease |  specifies a transition effect with a slow start, then fast, then end slowly (this is default) | 
| linear|  specifies a transition effect with the same speed from start to end | 
| ease-in|   specifies a transition effect with a slow start | 
| ease-out|  specifies a transition effect with a slow end | 
| ease-in-out|  specifies a transition effect with a slow start and end | 





## example


```html
    <section>
        <div class="trani trani_1"> with </div>
        <div class="trani trani_2"> without </div>
    </section>
```


```css

    .trani{
        background-color: rgb(211, 211, 211);
        height: 100px;
        width: 100px;
        display: flex;
        font-size: .9rem;
        align-items: center;
        justify-content: center;
    }


    .trani_1{
        transition: background-color 0.6s ease-in,  font-size 0.6s ease-in  ;
    }

    .trani:hover{
        background-color: rgb(56, 255, 222);
        font-size: 1.2rem;
    }


```

![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/tran1.gif)

You see defirint now!





# CSS transform


The transform property applies a 2D or 3D transformation to an element. 

The transform CSS property lets you rotate, scale, skew, or translate an element. It modifies the coordinate space of the CSS visual formatting model.


Property Transform

- rotate: Defines a rotation, the angle is specified in the parameter

```css
    .class_1{
        transform: rotate(-15deg); 
    }

    .class_2{
        transform: rotate(15deg); 
    }
```

![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/1.PNG)



- translate: Defines a translation


```html
    <div class="wrapper">
        <div class="card card_1">
            before
        </div>
        <div class="card card_2">
            before
        </div>
        <div class="card card_3">
            before
        </div>
    </div>

```


```css

    .wrapper {
        background-color: rgb(226, 226, 226);
        width: 100%;
        height: 200px;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }

    .card{
        width: 200px;
        height: 200px;
        background-color: rgb(68, 101, 161);
        font-size: 1.1rem;
        color: #fff;
        display: flex;
        align-items: center;
        justify-content: center;
    }
```
![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/befpre%20tra.PNG)


but if we use transform translate then will add 

```css
    .card_1 {
        transform: translate(-50px, -120px);
    }

    .card_2 {
        transform: translateX(80px);
    }

    .card_3{
        transform: translateY(90px);
    }

```

![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/after%20tra.PNG)


- scale:   Defines a scale transformation	

```css
    .card_1 {
         transform: scale(0.7);
    }

    .card_2 {
        transform: scaleX(0.5);
    }

    .card_3{
        transform: scaleY(0.5);
    }

```

![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/scale.PNG)


- skew:  Defines a 2D skew transformation along the X- and the Y-axis	


```css
    .card_1 {
         transform: skew(20deg, 20deg);
    }

    .card_2 {
        transform: skewX(30deg);
    }

    .card_3{
        transform: skewY(30deg);
    }

```
![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/skew.PNG)



we can write more property with same line
```css
    .card_2{
        transform: translateY(100px) rotate(45deg) scale(1.5);
    }
```

![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/mores.PNG)




# What is css animation?
#### CSS animations is a proposed module for Cascading Style Sheets that allows the animation of HTML document elements using CSS.

CSS animations make it possible to animate transitions from one CSS style configuration to another. Animations consist of two components, a style describing the CSS animation and a set of keyframes that indicate the start and end states of the animation’s style, as well as possible intermediate waypoints.



### The animation property is a shorthand property for:

| Property        | Description     | 
| ------------- |:-------------:|
| animation-name      |  Specifies the name of the keyframe you want to bind to the selector | 
| animation-duration     | Specifies how many seconds or milliseconds an animation takes to complete      |  
| animation-timing-function | Specifies the speed curve of the animation      |   
| animation-delay | Specifies a delay before the animation will start      |   
| animation-iteration-count | Specifies how many times an animation should be played      |   
| animation-direction | Specifies whether or not the animation should play in reverse on alternate cycles      |   
| animation-fill-mode | Specifies what values are applied by the animation outside the time it is executing      |   
| animation-play-state | Specifies whether the animation is running or paused      |   


### then we can write this in one line, how?
 
animation: name duration timing-function delay iteration-count direction fill-mode;

Example: 
```css
animation: nameAnimation 0.5s ease-in-out;
```


#### And when we use animation then we use keyframes with it
#### what keyframes?


The @keyframes controls the intermediate steps in a CSS animation sequence by defining styles for keyframes (or waypoints) along the animation sequence. This gives more control over the intermediate steps of the animation sequence than transitions.

Example: 
If use from and to.
```css
@keyframes nameAnimation {
  from {
    transform: translateX(0%);
  }

  to {
    transform: translateX(100%);
  }
}
```

If you use percentages from 0% to 100%
```css
@keyframes nameAnimation {
  0% { top: 0; }
  50% { top: 30px; left: 20px; }
  50% { top: 10px; }
  100% { top: 0; }
}
```


Specify when the style change will happen in percent, or with the keywords "from" and "to",
which is the same as 0% and 100%. 0% is the beginning of the animation, 100% is when the
animation is complete.


#### Also we can use from and to with percentage like

```css
@keyframes myexample {
  from {top: 0px;}
  50%  {top: 100px !important;} /* ignored */
  to   {top: 200px;}
}
```

> The !important rule is ignored in a keyframe



## Examples animation:

### Ex - 1:


![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/loop.gif)


Here is the code

```html 
    <div class="box_1"></div>
```

```css 
.box_1 {
    background-color: rgb(1, 18, 255);
    animation: box1Animat 3s linear infinite;
}


@keyframes box1Animat {
    0% {
        border-radius: 0%;
        transform: scale(1);
    }

    50% {
        border-radius: 50%;
        background-color: rgb(255, 50, 67);
        transform: scale(.2);
    }

    100% {
        border-radius: 0%;
        transform: scale(1);
    }
}

```
Its work yah, but look in ```0%``` and ```100%``` the rule same and same time its default rule, 

like ```border-radius``` equl ```0%```  in ```0%```
and
like ```border-radius``` equl ```0%```  in ```100%```

already any animation when start take default rule and when finish back to this rule

then we can write code like this:

```css 
@keyframes box1Animat {
    50% {
        border-radius: 50%;
        background-color: rgb(255, 50, 67);
        transform: scale(.2);
    }
}
```

#


### Ex - 2:

![task 2 no delay](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/ani2-out.gif)


```html
    <div class="box_2">
        <div class="card" ></div>
        <div class="card" ></div>
        <div class="card" ></div>
    </div>
```


```css
.box_2 {
    background-color: royalblue;
    height: 300px;
    width: 100%;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}

.card {
    width: 200px;
    height: 200px;
    background-color: sandybrown;
    animation: cardFromLeft 1s ease-in-out;
}

@keyframes cardFromLeft {
    0%{
        opacity: 0;
        transform: translateX(-100vw) scale(0);
    }
}
```

task for you make this animation like this:

![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/ani2-slow.gif)


#

### Ex - 3:


![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/anim3.gif)


```html

    <div class="box_3">
        <div class="image animate">
            <img src="#link image" alt="">
        </div>

        <div class="info animate">
            <span>Loerm100</span>
        </div>
    </div>

```

style css for html section

```css
.box_3 {
    height: 100vh;
    width: 100%;
    background-color: rgb(228, 232, 255);
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}

.image img {
    width: 300px;
    height: 100px;
    object-fit: cover;
    animation: imageHeight 1s ease-in-out forwards 1s;
}

.info {
    width: 50%;
}

.animate {
    animation: animateSlowly 1s ease-in-out;
}

```
In this animation we have 2 keyframs

first animation for all class ```animate``` in this section


```css
    @keyframes animateSlowly {
        0% {
            opacity: 0;
            transform: translateY(200px);
        }
    }
```

second animation for image ```image``` in this section

```css
     @keyframes imageHeight {
        100% {
            height: 400px;
        }
    }
```


#

### If you use more one animation 

```css
.image img {
    width: 300px;
    height: 100px;
    object-fit: cover;
    animation: image 1s ease-in-out forwards 1s;
    animation: imageTop 1s ease-in-out forwards 2s;
    animation: imageScale 1s ease-in-out forwards 3s;
}

```
in this case just last animation will work


```css
.image img {
    width: 300px;
    height: 100px;
    object-fit: cover;
    animation: image 1s ease-in-out forwards 1s;
    animation: imageTop 1s ease-in-out forwards 2s;
    animation: imageScale 1s ease-in-out forwards 3s;
}

```

And for work all animations in the same element we use ```,``` . The first animation will be performed, then the next, and so on.


```css
    .image img {
        width: 300px;
        height: 100px;
        object-fit: cover;
        animation:  image 1s ease-in-out forwards 1s
                    imageTop 1s ease-in-out forwards 2s,
                    imageScale 1s ease-in-out forwards 3s ;
    }

```


## Play and Pause animation from js

In default animation is auto play like this line but we dont write it


```css
    animation-play-state: running;
```

but if we want stop animation just write this rule with value ```pause```
```css
    animation-play-state: pause;
```

Also in this cases we use js for play or pause the animation
and with first example update to below


![task 1](https://raw.githubusercontent.com/divluffy/css-animation/main/assets/playpause.gif)


How we did it?

first we add two btns and with ```onclick``` call his function

```html

    <div class="box box_1"></div>
    <div class="btns">
        <button class="play" onclick="isPlay()">play</button>
        <button class="pause" onclick="isPause()">pause</button>
    </div>

```

and js call element and funcations:

```js
    const box1 = document.querySelector('.box_1')

    function isPlay(){
        box1.style.animationPlayState = 'running'
    }

    function isPause(){
        box1.style.animationPlayState = 'paused'
    }

```



## Animation with scrolling



It is known that the animation is executed automatically when the page is opened, which means that all animations will be executed all the page.

But what's the problem here?

When the user initially scrolls down and makes a scroll, no animation will be executed because it has already been executed at the beginning of the page load, what is the solution?

The solution is when the user reaches a certain section, then the animation is executed, then here we use js observe().

