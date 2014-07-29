Animates elements inside a {{> AnimateWithVelocity}} block, by adding specific attributes to elements.

Requires at least Meteor version 0.8.3-rc5
<!-- Demo: http://templatesession2demo.meteor.com -->

Installation
============

    $ mrt add animation-helper-velocity

Usage
=====


Wrap the templates or template parts with the {{#Animate}}..{{/Animate}} helper and add the animate class to it. Then you can specify the `data-property`, `data-from-value` and `data-to-value` attributes to animate elements:

	{{#AnimateWithVelocity}}
		<div data-animate data-property="opacity" data-duration="500" data-from-value="0" data-to-value="1">
			...
		</div>
	{{/AnimateWithVelocity}}

	// or animating multiple css properties

	{{#AnimateWithVelocity}}
		<div data-animate data-properties="left, opacity" data-from-values="1000px, 0" data-to-values="0px, 1">
			...
		</div>
	{{/AnimateWithVelocity}}

## Defaults
	data-property: 'opacity',
	data-duration: 200, // milliseconds
	data-from-value: 0,
	data-to-value: 1

Note: You can use the attributes in plural or singular form as you wish.
