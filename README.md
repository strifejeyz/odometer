# JS Odometer 
## A simple js odometer for animating numbers.

## How to use it:

### Install via npm (for JS frameworks)

`npm install simple-odometer`  

`import "simple-odometer/src/js/odometer.js";`

`import "simple-odometer/src/css/odometer.css";`

### Otherwise, just link them
 `<link rel="stylesheet" href="simple-odometer/src/js/odometer.js">`
 
 `<script rel="stylesheet" href="simple-odometer/src/js/odometer.js"></script>`


### Your HTML

    <span class="odometer">0</span>
    <button id='animate'>Animate</button>


### Configuration

<pre>
window.odometerOptions = {
    format: '(,ddd).dd',
    duration: 2000,
}
</pre>

### Your event handler:

<pre>
const button = document.querySelector('#animate');
button.onclick = () => {
    const odometer = document.querySelector('.odometer');
    const config = new window.Odometer({
        el: odometer, // pass the element ref
        value: odometer.value // old value
    });
    config.update(Math.random() * 1000); // new value
}
</pre>
