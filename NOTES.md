#WWWWH SVG
## Who What When Why? HOW? svg
### Ben Marks

#### Precis
Why should you, as a developer care about the what and why of SVG? Join us September 11th as we dive into the structure and capabilities of SVG, and find out some of the implications to software development.


## Why should I care about SVG?
- They are _scalable_ -- for all you responsive nuts out there
- They are _XML_
    - easy to understand
- They can be manipulated _just like any other tag_
    - CSS -- YES!
    - Javascript
    - and Internal animations!
- They can hold text
- change width/height to percent or vh!
- change viewBox to what it needs to be for your view. This might be a good use of JS...


**Note: The value of a pixel depends on the view box**

**build an app for this. just press buttons. And don't switch windows 
for no reason. Always include a 'back' button.**

#### Agenda

- ~~History (10-15)~~
- Use cases:
    - Good at:
        - size: Wow! these are text files. Do a comparison.
        - responsiveness
            - Graphics do not have to be different for different screen 
            sizes and density. One file for all use-cases. These graphics 
            can also be reused on the page. And be very complex (as we will see)
        - scalability (think reuse)
        - simple animations
            - Not really designed for animation, but simple animations can 
            be accomplished and are built in (including animate along a path.)
        - building graphics on the fly
          - since the drawing is a collection of elements, you can build 
          one on the fly either in-browser, or on the server. they are 
          pretty light-weight (being "just text") 
    - Bad at:
        - IE and Edge. Everyone else is ok. There are shivs available
        - user friendliness. the complicated attributes used can be daunting
        - canvas-like activities
        - complicated animations
            - since these are essentially built in the browser, processors 
            can get bogged down with computation.
- Format and structure (15-20)
    - call up a "control file"
    - Read more about tags!
    - `<svg>`
        - attributes
    - `<g>`
    - shape and path elements
    - animation elements
    - the `xlink:href` attribute is deprecated. just use `href`
- Usage (15-20)
    - tied into the above explanation... then tie it together with a big thing.
    - make a site to contain all this!

#### What I think I know

_Forget all you know, or **think** you know_ - Willow

- **S**calable **V**ector **G**raphics
- used in CAD way back?
- based on XML
- makes more than straight lines

### History??

### Format

### Usages

#### direct manipulation?
#### d3.js definitely

#### applications?
- Custom loading icons
- Reusable graphics
- Simple 

## Slides

1. Intro - name and title
    1. Title of talk
    1. Name and background
1. Brief History
    1. Microsoft and Adobe
    1. W3C standard
1. Disadvantages
1. Advantages
    1. responsiveness
    1. size
    1. etc
1. Construction
    1. elements
    1. important tags
    1. starting off
1. Applications
    1. current uses
        - Maps!
    1. cool animation
        - NWP logo?
        - water/ocean
    1. color-blind app
    1. Monty Python Animation
1. Holy god the examples!




# Take a step BACK:
1. as a developer, why do I care about SVG?
    - explore capabilities
1. as a developer, what can I do with svg, that I cannot do any other way?
    - These have some caveats
    - highlight EASE of USE and integration
1. Ok, now we HAVE to mention d3.js
    - Refer to delaine's talk.
    - go through some examples from the tutorial site
    