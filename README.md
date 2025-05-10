# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨


HTML(index.html)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Interaction</title>
    <style>
        #dynamicText {
            color: blue;
            font-size: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to My Page</h1>
    </header>
    <main>
        <section>
            <p id="dynamicText">This text will change dynamically.</p>
            <button onclick="changeText()">Change Text</button>
        </section>
        <section>
            <button onclick="toggleElement()">Toggle Element</button>
            <div id="toggleDiv">This element can be added/removed.</div>
        </section>
        <section>
            <button onclick="changeStyle()">Change Style</button>
        </section>
    </main>
    <footer>
        <p>© 2025 Your Name</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>


JAVASCRIPT (script.js)


// Function to change text content
function changeText() {
    document.getElementById("dynamicText").textContent = "Text has been changed!";
}

// Function to modify CSS styles
function changeStyle() {
    document.getElementById("dynamicText").style.color = "red";
    document.getElementById("dynamicText").style.fontSize = "25px";
}

// Function to add/remove an element
function toggleElement() {
    let div = document.getElementById("toggleDiv");
    if (div) {
        div.remove();
    } else {
        let newDiv = document.createElement("div");
        newDiv.id = "toggleDiv";
        newDiv.textContent = "This element is back!";
        document.body.appendChild(newDiv);
    }
}
