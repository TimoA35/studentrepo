---
commnts: false
layout: post
title: Basketball Salaries
description:
type: hacks
courses: {‘csp’: {‘week’: 2}}
categories: [‘C4.1’]
---

### Basketball Player Salary Table

<table class="table">
    <thead>
        <tr>
            <th>Player</th>
            <th>Team</th>
            <th>Position</th>
            <th>Salary (in millions)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>LeBron James</td>
            <td>Los Angeles Lakers</td>
            <td>Forward</td>
            <td>$39.2</td>
        </tr>
        <tr>
            <td>Stephen Curry</td>
            <td>Golden State Warriors</td>
            <td>Guard</td>
            <td>$43.4</td>
        </tr>
        <tr>
            <td>Kevin Durant</td>
            <td>Brooklyn Nets</td>
            <td>Forward</td>
            <td>$42.0</td>
        </tr>
        <tr>
            <td>Luka Dončić</td>
            <td>Dallas Mavericks</td>
            <td>Guard/Forward</td>
            <td>$10.2</td>
        </tr>
        <tr>
            <td>Giannis Antetokounmpo</td>
            <td>Milwaukee Bucks</td>
            <td>Forward</td>
            <td>$39.3</td>
        </tr>
        <tr>
            <td>Kawhi Leonard</td>
            <td>Los Angeles Clippers</td>
            <td>Forward</td>
            <td>$39.3</td>
        </tr>
        <tr>
            <td>Lamelo Ball</td>
            <td>Charlotte Hornets</td>
            <td>Guard</td>
            <td>$9.0</td>
        </tr>
        <tr>
            <td>Joel Embiid</td>
            <td>Philadelphia 76ers</td>
            <td>Center</td>
            <td>$31.5</td>
        </tr>
        <!-- Additional Rows -->
        <tr>
            <td>Kevin Love</td>
            <td>Cleveland Cavaliers</td>
            <td>Forward</td>
            <td>$28.9</td>
        </tr>
        <tr>
            <td>Damian Lillard</td>
            <td>Portland Trail Blazers</td>
            <td>Guard</td>
            <td>$31.6</td>
        </tr>
        <tr>
            <td>Russell Westbrook</td>
            <td>Los Angeles Lakers</td>
            <td>Guard</td>
            <td>$44.2</td>
        </tr>
        <tr>
            <td>Devin Booker</td>
            <td>Phoenix Suns</td>
            <td>Guard</td>
            <td>$29.5</td>
        </tr>
    </tbody>
</table>

<script>
    // JavaScript to highlight highest and lowest salaries
    document.addEventListener("DOMContentLoaded", function () {
        const rows = document.querySelectorAll("tbody tr");
        let highestSalary = -1;
        let lowestSalary = Number.MAX_VALUE;

        // Find the highest and lowest salaries
        rows.forEach(function (row) {
            const salary = parseFloat(row.querySelector("td:last-child").textContent.replace("$", ""));
            highestSalary = Math.max(highestSalary, salary);
            lowestSalary = Math.min(lowestSalary, salary);
        });

        // Highlight the rows with highest and lowest salaries
        rows.forEach(function (row) {
            const salary = parseFloat(row.querySelector("td:last-child").textContent.replace("$", ""));
            if (salary === highestSalary) {
                row.style.backgroundColor = "#FFD700"; // Highlight highest salary in gold
            } else if (salary === lowestSalary) {
                row.style.backgroundColor = "#FF5733"; // Highlight lowest salary in red
            }
        });
    });
</script>

<ul>
    <li><strong>Describe the difference between HTML and JavaScript:</strong> HTML is a structuring service for web content. JavaScript is used for dynamic interactions on your website.</li>
    <li><strong>Describe a benefit of a markdown table:</strong> Markdown tables are simple to read and easy to create. They don’t require any complex tags or styling, making them accessible for people who may not be well-versed in HTML.</li>
    <li><strong>Describe a benefit of a table that uses JavaScript:</strong> JavaScript allows for dynamic table interaction, like sorting and filtering without needing to reload the entire webpage.</li>
</ul>