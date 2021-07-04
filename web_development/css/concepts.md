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
  
  
  
