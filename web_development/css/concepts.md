## Three Pillars of Writing Good HTML and CSS
1. Responsive Design
  Fluid layouts, media queries, responsible images, correct units, desktop-first vs mobile-first
2. Maintainable and scalable code
  clean, easy-to-understand, growth, resuable, how to organize files, how to name classes, how to structure HTML
3. Web Performance
  less http requests, less code, compress code, use a css preprocessor, less images, compress images(use less bandwidth for the end users)
  
## How CSS Works Behind the Scenes:
LoadHTML  --> Parse HTML --> Document Object Model(DOM)                                                                                          --|
                  |                                                                                                                                |
                  |               Resolve conflistion CSS declarations(cascade)                                                                    |- Render Tree
                  |                    |                                                                                                           |        |
              Load CSS --> Parse CSS  -- Process final CSS values(including converting units defined in % to pixles) --> CSS Object Model(CSSOM) --|        |
                                                                                                                                                            |
                                                                                                                                                            |
                            Final rendered website <--------- Website rendering: the visual formatting model <-----------------------------------------------
                            
