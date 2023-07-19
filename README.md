# JS Odometer 
## A simple js odometer for animating numbers.
## See src/index.html for demo

### Install via npm

`npm install simple-odometer`  

`import "simple-odometer/src/js/odometer.js";`

`import "simple-odometer/src/css/odometer.css";`

### Or just link them
 `<link rel="stylesheet" href="simple-odometer/src/js/odometer.css">`
 
 `<script src="simple-odometer/src/js/odometer.js"></script>`


### Your HTML

    <span id="odometer">0</span>
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
    // Target the element to animate
    const target_elem = document.querySelector('#odometer');

    // Create na instance
    const OdoInstance = new Odometer({
        // pass the element ref
        el: target_elem,

        // Old value to animate from
        value: target_elem.innerHTML
    });

    // Finally, give it a new value to animate to
    OdoInstance.update(Math.random() * 1000); // new value
}
</pre>
