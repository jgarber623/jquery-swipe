# jquery-swipe #

A jQuery plugin for binding actions to left and right swipe events in Mobile Safari (or any browser that supports onTouchStart, onTouchEnd, onTouchMove, and onTouchCancel events).

This plugin is based heavily on [Ryan Scherf](http://www.ryanscherf.net)'s [jQuery Swipe Plugin](http://archive.plugins.jquery.com/project/swipe). Credit for all the hard maths go to him.


## Requirements ##

- [jQuery](http://jquery.com/) (1.7.2 or greater is recommended)
- A device running iOS or the iPhone Simulator


## Usage ##

	$( window ).swipe({
		left: function() {
			console.log( "You swiped left!" );
		},
		right: function() {
			console.log( "You swiped right!" );
		},
		threshold: {
			x: 200,
			y: 50
		}
	});

### Parameters ###

- `left`: A function you'd like to execute when a left swipe is detected. Defaults to `function( event ) {}`.
- `right`: A function you'd like to execute when a right swipe is detected. Defaults to `function( event ) {}`.
- `threshold`: An object containing an `x` and `y` value. The threshold is used to determine what constitues a swipe. The implied unite is pixels and the default threshold is `{ x: 100, y: 25 }`.


## TODO ##

- Add support for callbacks
- Improve event handling
- Figure out what the heck touchCancel is