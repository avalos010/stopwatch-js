# Stopwatch JS

Small JavaScript library that generates beautiful countdown.
##Demos
you can see a live demo on the Codepen [demo](http://codepen.io/neostar123/full/kIsqd)
##Usage

Download and include the JavaScript file in your HTML like shown below:
```
<script src="circle.min.js"></script>
<script src="stopwatch.min.js"></script>
<script src="PATH-TO-YOUR-JS"></script>
```

Now you need to create container for stopwatch where you want to start watch. And you will also need to setup elements for start, pause and reset. You can add custom method call onClick to that(you'll see implementation later here). It will look like this:

```
<div class="watch" id="mywatch"></div>
<input type="button" value="start" onClick=startWatch();/>
<input type="button" value="pause" onClick=pauseWatch();/>
<input type="button" value="reset" onClick=resetWatch();/>
```

Now you can call this library by using "id" of div on window load event and simply implement stopwatch operations like this:

```
var watch, clocktimer;
window.onload = function() {
    watch = new Stopwatch("mywatch");
};

function startWatch() {
    clocktimer = setInterval("watch.update(false)", 1);
    watch.start();
}

function pauseWatch() {
    watch.stop();
    clearInterval(clocktimer);
}

function resetWatch() {
    watch.reset();
}
```

And this is it. You'll see aa awesome stopwatch on screen.

##Browser support
The library use the `canvas` element, you can check the support on [caniuse](http://caniuse.com/#search=canvas)

##Licence
This library is licensed under the terms of the MIT License.

##Inspired from
	[Circular charts](https://github.com/Whyounes/circle) - circle.min.js is edited a bit to work with this library here so use this file

Watch this library to get updates.
If you like this library, don;t forget to give it a star ;).
If you have any creative idea feel free to fork and improve this.