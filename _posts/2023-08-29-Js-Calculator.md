---
comments: false
layout: post
title: Timo's JS Calculator
description:
type: hacks
courses: {‘csse’: {‘week’: 1}, ‘csp’: {‘week’: 1}, ‘csa’: {‘week’: 0}}
categories: [‘C4.1’]
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GPA Calculator</title>
    <style>
        /* Add some basic styling for clarity */
        body {
            font-family: Arial, sans-serif;
        }

        h1, h2, h3 {
            text-align: center;
        }

        h2 {
            font-size: 18px;
        }

        h3 {
            font-size: 16px;
        }

        label {
            font-weight: bold;
        }

        input[type="number"] {
            text-align: right;
            width: 5em;
        }
    </style>
</head>
<body>
    <!-- Heading -->
    <h1>GPA Calculator</h1>
    <h2>Input scores and press "Enter" to add each new number.</h2>
    <!-- Totals -->
    <h3>
        Total : <span id="total">0.0</span>
        Count : <span id="count">0.0</span>
        Average : <span id="average">0.0</span>
    </h3>
    <!-- Rows -->
    <div id="scores">
        <!-- JavaScript-generated inputs -->
    </div>

    <script>
        let index = 0; // Index for each input line

        // Function to create a new input line
        function newInputLine() {
            index++;

            // Create a label for the input
            const label = document.createElement('label');
            label.setAttribute('for', 'score-' + index);
            label.innerHTML = index + ". ";
            document.getElementById("scores").appendChild(label);

            // Create the input element
            const input = document.createElement("input");
            input.setAttribute('id', 'score-' + index);
            input.setAttribute('type', "number");
            input.setAttribute('name', "score");
            input.setAttribute('style', "text-align: right; width: 5em");
            input.addEventListener('keydown', calculator); // Add an event listener
            document.getElementById("scores").appendChild(input);

            // Create a line break after the input
            const br = document.createElement("br");
            document.getElementById("scores").appendChild(br);

            // Set focus on the new input line
            document.getElementById('score-' + index).focus();
        }

        // Function to calculate and update totals
        function calculator(event) {
            if (event.key === "Enter") {
                const scores = document.getElementsByName('score');
                let total = 0;
                let count = 0;

                scores.forEach((scoreElement) => {
                    const value = parseFloat(scoreElement.value);
                    if (!isNaN(value)) {
                        total += value;
                        count++;
                    }
                });

                document.getElementById('total').textContent = total.toFixed(2);
                document.getElementById('count').textContent = count;
                document.getElementById('average').textContent = (count > 0) ? (total / count).toFixed(2) : "0.0";

                // Add a new input line if all inputs have valid values
                if (count === scores.length) {
                    newInputLine();
                }
            }
        }

        // Create the first input box on window load
        window.addEventListener('load', () => {
            newInputLine();
        });
    </script>
</body>
</html>
