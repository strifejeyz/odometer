# JS Odometer 
## A simple js odometer for animating numbers.

## How to use:

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


### Configuration when page is loads/when component is mounted

<pre>
window.odometerOptions = {
    format: '(,ddd).dd',
    duration: 2000,
}
</pre>

### Then update your config like so:

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
