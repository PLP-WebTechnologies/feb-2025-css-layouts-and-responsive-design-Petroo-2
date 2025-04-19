



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }

        /* Navigation Bar */
        .navbar {
            background-color: #333;
            color: white;
            padding: 1em;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .navbar-brand {
            font-size: 1.5em;
            font-weight: bold;
        }

        .navbar-links {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
        }

        .navbar-links li {
            margin-left: 1em;
        }

        .navbar-links a {
            color: white;
            text-decoration: none;
        }

        /* Main Content Area (Using Grid for Desktop) */
        .container {
            display: grid;
            grid-template-columns: repeat(3, 1fr); /* Three equal columns */
            gap: 20px;
            padding: 20px;
            max-width: 1200px;
            margin: 20px auto;
        }

        .item {
            background-color: #ddd;
            padding: 20px;
            border-radius: 5px;
        }

        .item h2 {
            margin-top: 0;
        }

        /* Footer (Using Flexbox) */
        .footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em 0;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 1em;
        }

        /* Media Queries for Responsiveness */

        /* Mobile View (up to 600px) */
        @media (max-width: 600px) {
            .container {
                grid-template-columns: 1fr; /* Single column */
            }

            .navbar-links {
                display: none; /* Hide links on mobile initially */
            }

            .navbar {
                justify-content: space-around; /* More space around brand on mobile */
            }
        }

        /* Tablet View (601px to 1024px) */
        @media (min-width: 601px) and (max-width: 1024px) {
            .container {
                grid-template-columns: repeat(2, 1fr); /* Two columns */
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="navbar-brand">My Website</div>
        <ul class="navbar-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <div class="container">
        <div class="item">
            <h2>Item 1</h2>
            <p>This is the content for item 1.</p>
        </div>
        <div class="item">
            <h2>Item 2</h2>
            <p>This is the content for item 2.</p>
        </div>
        <div class="item">
            <h2>Item 3</h2>
            <p>This is the content for item 3.</p>
        </div>
        <div class="item">
            <h2>Item 4</h2>
            <p>This is the content for item 4.</p>
        </div>
        <div class="item">
            <h2>Item 5</h2>
            <p>This is the content for item 5.</p>
        </div>
        <div class="item">
            <h2>Item 6</h2>
            <p>This is the content for item 6.</p>
        </div>
    </div>

    <footer class="footer">
        <p>&copy; 2023 My Website</p>
        <p>Follow us on <a href="#">Twitter</a></p>
    </footer>

    <script>
        // You could add JavaScript here to make the mobile navigation interactive (e.g., a toggle button)
    </script>
</body>
</html>
