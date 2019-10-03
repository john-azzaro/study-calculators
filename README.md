# Calculator Study
See it Live: https://john-azzaro.github.io/study-calculators/

<br>

## What is the Calculator Study?
"Calculator Study" is an examination of basic calculator programming and functionality.  Doing some research on calculators, there are a *lot* of ways of making a calculator, and after a bit of trial and error this seems to be a personal fit that you might find interesting as well.  This study includes a variety of HTML and CSS layout and styling designs, as well as a variety of JavaScript code using different tools and coding paradigms such as classes, constrcutors, and some basic OOP!

Here are a few questions from the study to explore:

* [What are some interesting takeaways from the calculator study?](#What-are-some-interesting-takeaways-from-the-calculator-study)
* [Does Calculator Study feature commentary?](#Does-Calculator-Study-feature-commentary)
* [What are the key features of Calculator Study?](#What-are-the-key-features-of-Calculator-Study)

<br>

## What are some interesting takeaways from the calculator study?

<br>

### Using data attributes for selectors helps keeps code manageable
For this study, I used data attributes to try something different, but also to see how it could make my code a little "prettier".  Although I do like it since it keeps the id and class attributes a little cleaner, simply having an additional class works just as well.
```HTML
    <button data-number class="numerical-button">1</button>   <== "data-number"
    <button data-number class="numerical-button">2</button>
    <button data-number class="numerical-button">3</button>
```
Additionally, remember to add square brackets when you do your selectors.
```JavaScript
    const numberButtons = document.querySelectorAll('[data-number]');
```

<br>

### Use of class and constructors is EXTREMELY useful
In a nutshell, classes are constructor functions with a prototype property where the class keyword starts a class declaration and allows you to define a constructor and a set of methods in a single place.  As a personal note, after using factory functions for a bit, getting into the ES6 classes and constructors have proven to be extremely useful and easy to use once you get the hang of it.   Below I did cut-down version of the prototype in this study with emphasis on the clear functionality so you can get a sense of the functional flow.
```JavaScript
    class Calculator {                                                                               // Second, create calculator class
        constructor(previousOperandTextElement, currentOperandTextElement) {                         // ... with a constructor that takes all the inputs ...
            this.previousOperandTextElement = previousOperandTextElement; calculator)
            this.currentOperandTextElement = currentOperandTextElement; 
            this.clear(); 
        } 
        clear() {                                                                                    // ... clear numbers
            this.currentOperand = '';                                                                // ... and for the current operand, when cleared, it will default to an empty string.
            this.previousOperand = '';                                                               // ... and for the the previous operand it will also be cleared.
            this.operation = undefined;                                                              // ... and lastly the operation will be undefined.
        }
        delete() { ... }
        appendNumber(number) { ... }
        chooseOperation(operation) { ... } 
        compute() { ... } 
        updateDisplay() { ... }
    }

    const calculator = new Calculator(previousOperandTextElement, currentOperandTextElement)         // Third, create a calculator object and pass everything from the constructor into it.

    const allClearButton = document.querySelector('[data-all-clear]');                               // First, select an element (in this case, the clear button)

    allClearButton.addEventListener('click', function(event) {                                       // Fourth, select a button on click and 
        calculator.clear();                                                                          // ... and call the "clear" method in the calculator class
        calculator.updateDisplay();                                                                  // ... and update the display!
    })
```

<br>

## Does Calculator Study feature commentary?
Yes!  I try to make use of EXTENSIVE commentary (mostly in the form of my thought process) so that the new and curious can follow the logic in the program and get an idea of my reasoning behind each and every line of code, . 

<br>

## What are the key features of Calculator Study?
Since this study is ongoing, basic functionalities are covered first and more advanced features are added or will be added in the future.  For a complete list of current and future changes, see below:


| **Features:**                            | **Feature Notes:**                             |
| ---------------------------------------- | ----------------------------------------------|
| Current Operand Display                  |   |
| Previous Operand Display                 |  Basic operation TBA |
| Basic Operations                         |  Basic operations include: mult, div, add, sub |  
| Clear                                    |   | 
| Delete                                   |  Delete increment of 1  |    
| Equals                                   |   | 

<br>

## Screenshots

![calcScreenShot](https://user-images.githubusercontent.com/37447586/60772122-89e4cf80-a0a6-11e9-92e0-432788b4a50f.png)
