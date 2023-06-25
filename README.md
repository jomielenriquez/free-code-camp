# Data Visualization with D3 Lessons

1. Using Select (select)
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Source: https://www.javatpoint.com/d3-js-installation -->
        <script src = "https://d3js.org/d3.v4.min.js"></script> 
    </head>
    <body>
        <a>

        </a>
        <script>
            d3.select("body")
                .append("h1")
                .text("Learning D3")
        </script>
    </body>
</html>
```

2. Using Select All (selectAll)
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Source: https://www.javatpoint.com/d3-js-installation -->
        <script src = "https://d3js.org/d3.v4.min.js"></script> 
    </head>
    <body>
        <ul>
            <li>Example</li>
            <li>Example</li>
            <li>Example</li>
        </ul>
        <script>
            d3.selectAll("li")
                .text("list item")
        </script>
    </body>
</html>
```

3. Working with Data
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Source: https://www.javatpoint.com/d3-js-installation -->
        <script src = "https://d3js.org/d3.v4.min.js"></script> 
    </head>
    <body>
        <script>
            const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

            // Add your code below this line
            d3.select("body")
            .selectAll("h2")
            .data(dataset)
            .enter()
            .append("h2")
            .text("New Title")


            // Add your code above this line
        </script>
    </body>
</html>
```

4. Dynamic data
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Source: https://www.javatpoint.com/d3-js-installation -->
        <script src = "https://d3js.org/d3.v4.min.js"></script> 
    </head>
    <body>
        <script>
            const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

            d3.select("body")
            .selectAll("h2")
            .data(dataset)
            .enter()
            .append("h2")
            .text((d) => d + " USD");

        </script>
    </body>
</html>
```

5. Inline Styling
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Source: https://www.javatpoint.com/d3-js-installation -->
        <script src = "https://d3js.org/d3.v4.min.js"></script> 
    </head>
    <body>
        <script>
            const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

            d3.select("body")
            .selectAll("h2")
            .data(dataset)
            .enter()
            .append("h2")
            .text((d) => (d + " USD"))
            .style("font-family","verdana")

        </script>
    </body>
</html>
```