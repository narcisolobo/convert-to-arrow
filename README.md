# Convert to Arrow (Practice)
Convert each function below into modern arrow function syntax!

> Learning Objectives
> - Differentiate between JavaScript functions written in different syntax
> - Implement arrow functions to adhere to modern JavaScript standards and improve code readability

This practice assignment will reinforce important learning objectives from the previous lesson(s), and allow you to take on more challenging core assignments, preparing you for graduation.

Practice and tinker with this assignment until you're comfortable performing each of the tasks. Then, be sure to submit your output as described in the steps below.

## Convert to Arrow:
You work for a company that does not have a great front end for its website, but it prides itself on its JavaScript. Since they only care about adding random JavaScript functionality, they don't want you to change the CSS of this site. They have given you a task to update the Javascript in their site to ES6, so that every method being called uses arrow functions.

Take the following HTML and update all functions to arrow functions.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Arrow Functions</title>
</head>
<body id="body">
    <h1>My Boring Website</h1>
    <p id="paragraph">
        This website is boring, with very little CSS. 
        However, we really just care about the javascript. 
        For example, if you click <button id="button">this button</button>, the background of this paragraph tag will change to blue.
    </p>
    <p>
      We also have a <button id="alert">alert</button> button that will grab the text from the input below and show it in a popup.
    </p>
    <input type="text" name="" id="popup-input" />
    <p>
        We just like random interactivity in the site, including a fun effect if you hover over <span id="hover-this"><b>this.</b></span>
    </p>
    <p id="set-color">
        We can click anywhere in this paragraph tag and it will change the background color to whatever is in this input: <input type="text" id="color-input"/>
    </p>
    <p onmouseover="mouseOverFunction(this)">
        Moving your mouse over this text will make it black, so you cannot read it!
    </p>
    <script>
        document.getElementById("button").onclick = function() {
            setBackgroundColorById("paragraph", "blue");
        }
        document.getElementById("alert").onclick = function(){
            alert(document.getElementById("popup-input").value);
        }
        document.getElementById("hover-this").onmouseover = function(){
            setBackgroundColorById("body", "red");
        }
        document.getElementById("hover-this").onmouseout = function(){
            setBackgroundColorById("body", "white");
        }
        function getValueFromId(id){
            return document.getElementById(id).value;
        }
        function setBackgroundColorById(id, color){
            document.getElementById(id).style = "background-color: " + color;
        }
        function mouseOverFunction(el){
            el.style = "background-color: black";
        }
    </script>
</body>
</html>
```

- Update all functions to utilize arrow function syntax

- Use an `onclick` listener on the paragraph element with an id attribute of `"set-color"` to call the function `setBackgroundColorById`. This function requires two arguments to be passed in for the `id` and `color` parameters. What arguments must be passed in? How do we get the `value` of the `"color-input"` text input? *Hint:* there is a function we have not used yet.
