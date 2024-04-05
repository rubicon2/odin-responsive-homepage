# Odin Responsive Homepage
https://rubicon2.github.io/odin-responsive-homepage/

## Challenges
As per (what I perceive to be) common advice, I started working on the mobile layout first before considering the tablet and desktop layouts. 
However this ran into problems with the layout of the header image and text in particular, trying to achieve the desired positions and behaviour. 

The layout scaled up pretty well from mobile to desktop, just by using a max-width on the container that holds the content and flex-wrap on the projects section. 

Next time, it may be a good idea to look at what elements need to change between different layouts and plan ahead accordingly; not just with regard to the HTML structure, 
but with regard to CSS organisation. My CSS, in the end, was a mess. 

For example, there were two sets of social links, one on the header and one on the footer, as well as some other social links within each project. I thought I would be smart use one class that formatted them, 
but then realised the two sets of social links should respond differently to different viewport sizes. My solution was to have general classes for the common functionality (`flex` class for `display: flex`, 
`social-links` class for `list-style: none` and a flex gap) and specific classes (e.g. `header-social-links`, `footer-social-links`) that respond to the media queries. 

I think that using this approach from the beginning instead of starting halfway through would have made everything clearer and easier to understand. 

I also ran into a problem with `<picture>` where the element would add a little gap below the child `<img>`: [demo of img gap issue](https://codepen.io/rubicon2/pen/zYXRamo). It was absolutely maddening. Luckily after some searching 
online I found [this great post that helped solve the issue](https://dev.to/christiankaindl/the-strange-img-gap-in-html). 

I am also not familiar with the css `float` property. I remembered it from dabbling in websites circa 2012, and it mostly worked how I expected, but would like to learn more about it, as it 
seems to be the only way to get the header text to wrap around the image the way I wanted it to. I was under the impression the text would only wrap around sibling elements, but this appears 
not to be the case since the paragraph text that is a child of `header-text-container` wraps around the child image of `header-picture-section`. `header-text-container` and `header-picture-section` are sibling elements. 

Also my naming convention for elements is not very consistent or clear, so I want to work on that too. 

## Stuff To Do
- Learn about floats and text-wrapping around elements
- Decide upon a css class naming convention that is clearer and easier to read
- Make another responsive website for practice, this time making note of the layout differences before starting, delineating which elements need specific styles and which will need to be used for media queries,
  against which ones will only need generic styling, etc.
