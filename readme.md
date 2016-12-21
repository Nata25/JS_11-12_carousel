
## JQUERY CAROUSEL SIMPLE PLUGIN
don't try to repeat this in real life

## Quick review

Display optional number of slides at once. Add pagination on demand, with numbers or without. Choose between cyclic and non-cyclic modes. By default, the carousel is non-cyclic; left/right controls are dynamically hidden on breakpoints. Whith `cyclic` mode set to `true`, moves to the first slide when at the end and to the last slide when at the start.

## How to use

Initialize `.jqcarousel()` method on the container of your carousel. Inside the container, put `.jqcarousel-frame` and `.jqcarousel-controls`. They should be siblings.

Style `.jqcarousel-frame` as you like and set its width – that's how wide you carousel will be. It is a custom value but is used inside script to identify shift.

Make sure .jqcarousel-frame has `overflow` property set to `hidden`

Carousel items, or slides, go inside `.jqcarousel-frame` and should be wrapped with `.jqcarousel-content`. Items inside `.jqcarousel-content` (figures, listitems, images etc.) should have `display: inline-block` property. If they have uncontrolled margins, set their `float` to `left`, otherwise px per step would be miscalculated (e.g., figure with `display: inline-block` property get whitespace around even if margins are set to 0).

Width of `.jqcarousel-content` should be really great so that all slides would fit it (use something like 10000 px).

Controls go inside `.jqcarousel-controls` container; left control should be first-child and right - last-child of the container.

If you want pagination, put `.jqcarousel-pagination` container next to controls container. It should be initially empty as it's inner HTML is generated by script and these are a set of links (`<a>`s) of class `.jqcarousel-pgitem`. Use this class name to style the elements as well as additional `.active` class being added for indicating carousel position. (Selectors like `.jqcarousel-pagination a.active` or `.jqcarousel-pgitem.active` will do).

## Customize with options

- `speed` : speed of animation in miliseconds (`500` by default)

- `easing` : animation flow, string (`"linear"` by default)

- `cyclic` : should carousel go all the way round or stop after last/first slide (`false` by default)

- `slides` : number of slides to be shown in the carousel at once (`3` by default)

- `pagination` mode : by default is `"plain"` (pagination items are generated and ready to get .active class, but without digits indicating number of slide); can be also set to `"digits"` or `false`
