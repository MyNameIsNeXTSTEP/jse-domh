# jse-domh
Plain JS easy DOM handler is a tool for handling operation on DOM elements by quick and easy declarative abstract like commands

## Objectives
- Let a programmer quickly create and run declarative and relatively short script to handle DOM elements
- The idea is about to implement it as assembly like insctructions or objectionary like composition structure, then return a read to go vanilla JS script

Seems to me to be something like:

*(How much is this necessary and in what form, for what tasks - this question is still not completely clear)*

1.
```
CREATE div 'block-1' WITH_STYLES './styles.css'
CREATE span 'button text' name 'submit-button-text' in 'block-1'
WRAP 'submit-button-text' with button 'submit-button'
ONCLICK submit-button go alert('test')
ADD_SCRIPT './script.js'
```

2.
```
new DomElement(
    'block-1',
    new Div(
        new Button(
            'submit-button',
             new Span('button text', 'submit-button-text')
        ).onClick(() => alert('test'))
  ).withStyles('./styles.css')
).addScript('./script.js')
```
