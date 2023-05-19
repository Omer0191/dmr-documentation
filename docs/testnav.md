<!DOCTYPE html>
<html>
<head>
    <title>GitHub Markdown Navigation</title>
    <style>
        body {
            margin: 0;
            padding: 0;
        }

        #container {
            display: flex;
        }

        #sidebar {
            position: fixed;
            top: 0;
            left: 0;
            width: 200px;
            height: 100vh;
            background-color: #f1f1f1;
            padding: 20px;
            box-sizing: border-box;
        }

        #content {
            margin-left: 220px;
            padding: 20px;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <div id="container">
        <div id="sidebar">
            <ul>
                <li><a href="#section1">Section 1</a></li>
                <li><a href="#section2">Section 2</a></li>
                <li><a href="#section3">Section 3</a></li>
            </ul>
        </div>
        <div id="content">
            <h1 id="section1">Section 1</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            
            <h1 id="section2">Section 2</h1>
            <p>Donec nec odio vitae odio varius placerat. Ut non quam vitae nunc cursus viverra a at arcu.</p>
            
            <h1 id="section3">Section 3</h1>
            <p>Sed dapibus urna sit amet leo tristique, ut gravida turpis lacinia.</p>
        </div>
    </div>
</body>
</html>
