# JS Odometer 
## A simple js odometer for animating numbers.

## How to use:

### Install via npm

`npm install simple-odometer`  



### Your HTML

`</span><span class="odometer">0</span>`

`<button id='animate'>Animate</button>`


### Configuration

`window.odometerOptions = {
    format:   '(,ddd).dd',
    duration: 2000,
};
`

### Then modify the innerHTML:

`const odometer = document.querySelector('.odometer');`
 
`const button = document.querySelector('#animate')`

`button.onclick = () => {
   odometer.innerHTML = 2000;
}`
