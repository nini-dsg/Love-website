<header>
  `index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Girlfriend?</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Will You Be My Girlfriend?</h1>
        <button id="yesButton">Yes, I Do!</button>
        <button id="noButton" style="display: none;">No, Leave Me Alone</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

#### `date.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Schedule a Date</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Schedule a Date</h1>
        <label for="date">Choose a date:</label>
        <input type="date" id="date" required>
        
        <h2>Select a time:</h2>
        <div class="time-options">
            <label><input type="radio" name="time" value="Pizza"> Pizza</label>
            <label><input type="radio" name="time" value="London"> London</label>
            <label><input type="radio" name="time" value="Movie"> Movie</label>
        </div>
        
        <button id="continueButton">Continue</button>
    </div>
    <script>
        document.getElementById('continueButton').onclick = function() {
            const date = document.getElementById('date').value;
            const selectedOption = document.querySelector('input[name="time"]:checked');
            if (date && selectedOption) {
                localStorage.setItem('date', date);
                localStorage.setItem('time', selectedOption.value);
                window.location.href = 'schedule.html';
            } else {
                alert('Please select a date and a time option.');
            }
        };
    </script>
</body>
</html>
```

#### `schedule.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Date Schedule</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Your Date Schedule</h1>
        <div class="card">
            <h2>Date: <span id="dateDisplay"></span></h2>
            <h2>Activity: <span id="timeDisplay"></span></h2>
        </div>
    </div>
    <script>
        document.getElementById('dateDisplay').innerText = localStorage.getItem('date');
        document.getElementById('timeDisplay').innerText = localStorage.getItem('time');
    </script>
</body>
</html>
```

### 2. CSS Styles

Create a `styles.css` file for styling your website.

```css
body {
    font-family: Arial, sans-serif;
    background-color: #ffccff;
    color: #333;
    text-align: center;
    margin: 0;
    padding: 0;
}

.container {
    padding: 50px;
}

button {
    padding: 15px 30px;
    font-size: 20px;
    margin: 10px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    background-color: #ff66b2;
    color: white;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #ff3385;
}

.card {
    background-color: white;
    border-radius: 10px;
    padding: 20px;
    margin: 20px auto;
    width: 300px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
```

### 3. JavaScript Functionality

Create a `script.js` file for theCreating a romantic-themed website to ask someone to be your girlfriend is a sweet idea! Below is a simple HTML, CSS, and JavaScript code structure for your website. This code includes three pages as you described, with the specified features.

### 1. HTML Structure

Create three HTML files: `index.html`, `date.html`, and `schedule.html`.

#### `index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Girlfriend?</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Will You Be My Girlfriend?</h1>
        <button id="yesButton">Yes, I Do!</button>
        <button id="noButton" style="display: none;">No, Leave Me Alone</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

#### `date.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Schedule a Date</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Schedule a Date</h1>
        <label for="date">Choose a date:</label>
        <input type="date" id="date" required>
        
        <h2>Select a time:</h2>
        <div class="time-options">
            <label><input type="radio" name="time" value="Pizza"> Pizza</label>
            <label><input type="radio" name="time" value="London"> London</label>
            <label><input type="radio" name="time" value="Movie"> Movie</label>
        </div>
        
        <button id="continueButton">Continue</button>
    </div>
    <script>
        document.getElementById('continueButton').onclick = function() {
            const date = document.getElementById('date').value;
            const selectedOption = document.querySelector('input[name="time"]:checked');
            if (date && selectedOption) {
                localStorage.setItem('date', date);
                localStorage.setItem('time', selectedOption.value);
                window.location.href = 'schedule.html';
            } else {
                alert('Please select a date and a time option.');
            }
        };
    </script>
</body>
</html>
```

#### `schedule.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Date Schedule</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Your Date Schedule</h1>
        <div class="card">
            <h2>Date: <span id="dateDisplay"></span></h2>
            <h2>Activity: <span id="timeDisplay"></span></h2>
        </div>
    </div>
    <script>
        document.getElementById('dateDisplay').innerText = localStorage.getItem('date');
        document.getElementById('timeDisplay').innerText = localStorage.getItem('time');
    </script>
</body>
</html>
```

### 2. CSS Styles

Create a `styles.css` file for styling your website.

```css
body {
    font-family: Arial, sans-serif;
    background-color: #ffccff;
    color: #333;
    text-align: center;
    margin: 0;
    padding: 0;
}

.container {
    padding: 50px;
}

button {
    padding: 15px 30px;
    font-size: 20px;
    margin: 10px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    background-color: #ff66b2;
    color: white;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #ff3385;
}

.card {
    background-color: white;
    border-radius: 10px;
    padding: 20px;
    margin: 20px auto;
    width: 300px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
```

### 3. JavaScript Functionality

Create a `script.js` file for the<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Date Schedule</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Your Date Schedule</h1>
        <div class="card">
            <h2>Date: <span id="dateDisplay"></span></h2>
            <h2>Activity: <span id="timeDisplay"></span></h2>
        </div>
    </div>
    <script>
        document.getElementById('dateDisplay').innerText = localStorage.getItem('date');
        document.getElementById('timeDisplay').innerText = localStorage.getItem('time');
    </script>
</body>
</html>
  body {
    font-family: Arial, sans-serif;
    background-color: #ffccff;
    color: #333;
    text-align: center;
    margin: 0;
    padding: 0;
}

.container {
    padding: 50px;
}

button {
    padding: 15px 30px;
    font-size: 20px;
    margin: 10px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    background-color: #ff66b2;
    color: white;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #ff3385;
}

.card {
    background-color: white;
    border-radius: 10px;
    padding: 20px;
    margin: 20px auto;
    width: 300px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
<!--
  <<< Author notes: Course header >>>
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses MIT license.
-->

# GitHub Pages

_Create a site or blog from your GitHub repositories with GitHub Pages._

</header>

<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## Step 1: Enable GitHub Pages

_Welcome to GitHub Pages and Jekyll :tada:!_

The first step is to enable GitHub Pages on this [repository](https://docs.github.com/en/get-started/quickstart/github-glossary#repository). When you enable GitHub Pages on a repository, GitHub takes the content that's on the main branch and publishes a website based on its contents.

### :keyboard: Activity: Enable GitHub Pages

1. Open a new browser tab, and work on the steps in your second tab while you read the instructions in this tab.
1. Under your repository name, click **Settings**.
1. Click **Pages** in the **Code and automation** section.
1. Ensure "Deploy from a branch" is selected from the **Source** drop-down menu, and then select `main` from the **Branch** drop-down menu.
1. Click the **Save** button.
1. Wait about _one minute_ then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to the next step.
   > Turning on GitHub Pages creates a deployment of your repository. GitHub Actions may take up to a minute to respond while waiting for the deployment. Future steps will be about 20 seconds; this step is slower.
   > **Note**: In the **Pages** of **Settings**, the **Visit site** button will appear at the top. Click the button to see your GitHub Pages site.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/github-pages) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
