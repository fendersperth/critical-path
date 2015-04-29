# The critical path and perceived performance

## Improving perceived performance

After doing all the hard work to optimise our images, minifying our CSS, concatenating our Javascript, and all the other recommended steps, things can still be slow. If your website is content heavy, with lots images, styles or scripts, chances are, the initial load will still take a while. The first time someone visits your website, they will need to download all your website assets, that payload may still be large. The actual performance associated with your website can only be optimised so far. 

To improve things further, you need to look into how to optimise the perceived performance of your website. This can be achieved is by understand how the website renders, what causes the rendering of your website to stop i.e why we see a white page, so we can understand where the bottlenecks are, and in short, we need to be able to prioritise how the website content loads.

## Determining bottlenecks

performance budgets
size of assets
symptoms
- white page
- unstyled text
- content moving around while waiting for javascript to load
- images taking a while to load

## Prioritising content

Defer things you don't need (what is critical?)
- the fold (multiple devices)
- deciding on critical css
  - decide which elements are above the fold
  - css critical for layout (layout and dimensions)
  - background color and font color 
  - font stack (selecting base fonts that won't break your layout)
- defer js that isnt critical
- defer css that isnt critical

## Techniques 

### async loading css

- critical css in the head
- async load css function (https://github.com/filamentgroup/loadCSS)
- only load css required on that page (break up css files into common + pages?)

### async loading js

. critical js in the footer
- async load js library like headJS (http://headjs.com/)
- only load scripts required for the device (limit animations and libraries) or page 
	- check screen width and load scripts for the device
	- break up js files into modules / blocks and load required stuff only (or use a modular loader like require.js)

### async load fonts 

- use js font loader (https://github.com/typekit/webfontloader)
 
 ### others

- limit http requests for critical path (inline critical css and js into the html)
- limit initial payload e.g. lazy load images 

