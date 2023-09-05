---
toc: flase
comments: false
layout: post
title: Timo's Quiz
description:
type: plans
courses: { csse: {week: 1}, csp: {week: 1, categories: [4.A]}, csa: {week: 0} }
categories: [C1.4]
---


### General Knowldge Quiz

<html>
<head>
    <title>Python Quiz</title>
</head>
<body>
    <h1>Python Quiz</h1>
    <form id="quiz-form">
        <fieldset>
            <legend>Question 1: What is the built-in function to sort a list in Python?</legend>
            <label><input type="radio" name="q1" value="a">order()</label><br>
            <label><input type="radio" name="q1" value="b">sort()</label><br>
            <label><input type="radio" name="q1" value="c">arrange()</label><br>
        </fieldset>
        <fieldset>
            <legend>Question 2: Which Python data type is used to store an ordered collection of items?</legend>
            <label><input type="radio" name="q2" value="a">Array</label><br>
            <label><input type="radio" name="q2" value="b">List</label><br>
            <label><input type="radio" name="q2" value="c">Set</label><br>
        </fieldset>
        <fieldset>
            <legend>Question 3: What is the result of 2 + 3 * 4?</legend>
            <label><input type="radio" name="q3" value="a">20</label><br>
            <label><input type="radio" name="q3" value="b">14</label><br>
            <label><input type="radio" name="q3" value="c">11</label><br>
        </fieldset>
        <button type="button" id="submit-button">Submit Answers</button>
    </form>
    <div id="result"></div>
    <script>
        document.getElementById("submit-button").addEventListener("click", function() {
            const answers = {
                q1: document.querySelector('input[name="q1"]:checked'),
                q2: document.querySelector('input[name="q2"]:checked'),
                q3: document.querySelector('input[name="q3"]:checked')
            };
            let correctCount = 0;
            for (const question in answers) {
                if (answers[question] && answers[question].value === "b") {
                    correctCount++;
                }
            }
            const resultDiv = document.getElementById("result");
            resultDiv.innerHTML = `You got ${correctCount} out of 3 questions correct.`;
        });
    </script>
</body>
</html>
