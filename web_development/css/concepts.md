## Three Pillars of Writing Good HTML and CSS
1. Responsive Design
  Fluid layouts, media queries, responsible images, correct units, desktop-first vs mobile-first
2. Maintainable and scalable code
  clean, easy-to-understand, growth, resuable, how to organize files, how to name classes, how to structure HTML
3. Web Performance
  less http requests, less code, compress code, use a css preprocessor, less images, compress images(use less bandwidth for the end users)
  
## How CSS Works Behind the Scenes:
```
LoadHTML  --> Parse HTML --> Document Object Model(DOM)                                                                                          --|
                  |                                                                                                                                |
                  |               Resolve conflistion CSS declarations(cascade)                                                                    |- Render Tree
                  |                    |                                                                                                           |        |
              Load CSS --> Parse CSS  -- Process final CSS values(including converting units defined in % to pixles) --> CSS Object Model(CSSOM) --|        |
                                                                                                                                                            |
                                                                                                                                                            |
                            Final rendered website <--------- Website rendering: the visual formatting model <-----------------------------------------------
```

## CSS Rules
1. Cascade
  Process of combining different styles and resolving conflicts between different CSS rules and declarations, when more than one rule applies to a certain element
  css sources: a. Author b. User c. Browser(user agent)
  ### Precedence Determination: Importance(Weight) > Specificity > Source Order
  #### Importance
  1. User !important declarations
  2. Author !important declarations
  3. Author declarations
  4. User declarations
  5. Default browser declarations
  #### Specificity (Inline, IDs, Classes, Elements)
  1. Inline style
  2. IDs
  3. Classes, pseudo-classes, attribute
  4. Elements, pseudo-elements
  * The last declaration in the code will override all other declarations and will be applied. 
  * Only use !important as a last reource. It's better to use correct specificities - more maintainable code!
  * The universal selector * has no specificity value (0,0,0,0);
  * Rely more on specificity than on the order of selectors;
  * But, rely on order when using 3rd-party stylesheets - always put your author stylesheet last.
  
## How Units are converted from relative to absolute
### Font based
* em(font) - ```x * parent computed font-size```
* em(length) - ```x * current element computed font-size```
* rem - ```x * root element computed font-size```
### Viewport based
* vw - ```x * 1% of viewport width```
* vh - ```x * 1% of viewport height```

## Inheritance: What you need to know
* Inheritance passes the values for some specific properties from parents to children - more maintainable code
* Properties related to text are inherited: font-family, font-size, color, etc. padding, margin etc are not inherited.
* Inheritance of a property only works if no one declares a value for that property
* The inherit keyword forces inheritance on a certain property.
* The initial keyword resets a property to its initial value.

## The Visual Formatting Model
Algorithm that calculates boxes and determines the layout of these boxes, for each element in the render tree, in order to determine the final layout of the page.
* Dimension of boxes: the box model
* Box type: inline, block and inline-block
* Positioning scheme: floats and positioning;
* Stacking contexts;
* Other elements in the render tree;
* Viewport size, dimensions of image etc;

## Box Types: Inline, Block, and Inline Block
### Block-level boxes
* Elements formatted visually as blocks
* 100% of parent's width
* Vertically one after another
* Box-model applies as showed
### Inline boxes
* Content is distributed in lines
* Occupies only content's space
* No line-breaks
* No heights and widths
* Paddings and margins only horizontal(left and right)
### Inline-block
* A mix of block and inline
* Occupies on content's space
* No line-breaks
* Box-model applies as showed

## Positionning Schemes: Normal flow, Absolute positioning and Floats
### Normal flow
* Default positioning scheme;
* Not floated;
* Not absolutely positioned;
* Elements laid out according to their source order
### Floats
* Element is removed from the normal flow;
* Text and inline elements will wrap around the floated element;
* The container will not adjust its height to the element;
### Absolute positioning
* Element is removed from the normal flow
* No impact on surrounding content of elements
* We use top, bottom, left and right to offset the element from its relatively positioned container.

## Stacking Contexts
* Z-index
* Opacity, transform...




  
  
  
  
