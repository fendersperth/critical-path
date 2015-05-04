# The critical path and perceived performance

## Improving perceived performance
- Improvements from actual performance optimisations can be limited
- We can achieve further improvements by optimising perceived performance, that is the time it takes to render to the browser
- To do this we need to understand how to determine the bottlenecks and prioritise what is loaded

## Possible symptoms
- initial white page that hangs around for seconds
- flash of un-styled text breaking layout
- content moving around while waiting for javascript to load
- images taking a while to load

## Prioritising assets for the Critical Path
- Defer things you don’t need, what is critical for the initial load?
- Try to prioritise elements above the fold, possibly on multiple devices
- Inline critical assets, defer anything non-critical

## Critical CSS
- inline critical css in the head
- styles for layout, background colour, font colour, and font size
- defer non critical styles, async load css with javascript
- only load css required on that page, if it is a large file 

## Critical Path Javascript
- Inline javascript at the bottom of the file
- defer large libraries / frameworks 
- async load javascript library like headJS
- only load scripts required for the device or page
	 
## Critical Path Fonts
- Larger font stack, selecting fallback fonts that won’t break your layout
-  use js font loader, defer loading of non critical fonts 

## Critical Path Images
- Lazy loading images where necessary
- limit http requests for critical path (inline critical css and js into the html)
- limit initial payload 

## Links
https://github.com/filamentgroup/loadCSS
http://headjs.com/
https://github.com/typekit/webfontloader
