# JavaScript
- JavaScript Object Model
    - window
        - Represent the current browser instance
        - provides Global Events
            - onOpen, onClose, mouse and Keyboard events 
    - document
        - the current HTML DOM loaded in browser
        - used for following
            - REading HTML Element
            - Setting properties and events on HTML Elements
- REading HTML Element and assigning Event

````html
    <input type="button" id='btn'>
````
    - Extracting button to attach event e.g. 'click' event for button
````javascript
    // 1. REad element based on 'id'
    var btn  = document.getElementById('btn');
    // 2. Attahing Event
    // Parameters 
    // P1: Name of ye event
    // P2: The Fuction callback containing logic that
    // will be executed when the event is fired
    // P3: Boolean value that will be used to specify whether
    // the event is kept attached with an element  
    btn.addEventListener('click', function(){.....}, false);

````

- REad multiple elements having same name (name is an attribute)
    - document.getElementsByName(); returns an array of elements

- REad multiple elements having same class name (class is an attribute)
    - document.getElementsByClass(); returns an array of elements

- REad multiple elements having same tag name (name is an attribute)
    - document.getElementsByTagName(); returns an array of elements

- Events
    - click, mousemove, mouseenter, mouseleave, change (fired when an input:text, checkbox, radio element is changes), blur  (fired when an input:text lost the focus (means press TAB)), keyup, keypress, etc.

- Programming COnstructs     
    - if, if..else, switch..case
    - for..loop, for..of (ES 6), while..loop
- Types
    - variable is declared using 'var'
    - Each declaration using var is an object by default
    - var uses parse-time data types
        - var x = 'sss'; here x is string
        - uses same x for other type values
        - x = 100; number
        - x = new Date(); object
        - x = {}; object literal aka JSON
        - x = []; array
        - x = function(){.....}; the function object
- Functions bodies
    - function NAME (){};
        - no input and no output
    - function NAME(x,y){}
        - input parameters but no output
    - function NAME(x,y){return}
        - with input and output parameters
# Function MOdules
- Mechanism of creating class using function
- Reference Fucntions means storing a function body in a variable

````javascript
    var MyFunction =  function() {
          this.add = function(){};
          this.sub = function(){};  
            // private
          function myprivate(){}
    };

    // the 'this' is s MyFunction object itself
    // each declaration preceeds using 'this.' is
    // a publically exposed member

    var obj1 = new MyFunction();
    obj1.add(); obj1.sub();


````

- Close type function, the returns the Object Literal as Public members

````javascript
function MyFunctionObject() {
    /// ... other private members

    // public members are returned
    return {
        f1:function(){},
        f2:function(){}
    };

    var obj = new MyFunctionObject();
    obj.f1();obj.f2();
}
````
- Immediately Invoked Function Expression (IIFE)
    - Self-Executable JS
````javascript
   (function(){......})();
````

# jQuery
- Download the jQuery for Current Project OR Use 'Content-Delivery-Network (CDN)'
- JS Library for DOM aka UI
- USe '$' for 
    - Extracting DOM Element
        - by id
            - $("#{ID-OF-ELEMENT}")
        - by class name
            - $(".{CLASS-NAME-APPLIED-TO-ELEMENT}")    
        - by tag name
            - $('{TAG-NAME}')     
    - Attaching Event to an element
        - $("#{ID}").on('EVENT-NAME', function(){...});
    - For Plugins (ready-to-use-custom-functions)
        - loops
            - $.each()
                - for..each loop
            - $.ajax()
                - AJAX Call    



 
