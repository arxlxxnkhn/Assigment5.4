## Assignment 5.4 — CSS Variables & Design Tokens

### 1. `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Design Tokens</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>My Design System</h1>

    <div class="card">
        <h2>Welcome</h2>
        <p>This webpage uses reusable CSS variables.</p>
        <button>Learn More</button>
    </div>
</body>
</html>
```

### 2. `style.css`

```css
:root {
    --primary-color: navy;
    --secondary-color: orange;
    --background-color: #f0f4f8;
    --text-color: #333;

    --spacing-small: 8px;
    --spacing-medium: 16px;
    --spacing-large: 24px;

    --font-small: 14px;
    --font-medium: 18px;
    --font-large: 32px;
}

body {
    background-color: var(--background-color);
    color: var(--text-color);
    font-family: Arial, sans-serif;
    padding: var(--spacing-large);
}

h1 {
    color: var(--primary-color);
    font-size: var(--font-large);
}

.card {
    background: white;
    padding: var(--spacing-large);
    margin-top: var(--spacing-medium);
    border-radius: var(--spacing-small);
}

.card h2 {
    color: var(--primary-color);
}

p {
    font-size: var(--font-medium);
}

button {
    background: var(--primary-color);
    color: white;
    padding: var(--spacing-small) var(--spacing-medium);
    border: none;
    cursor: pointer;
}

button:hover {
    background: var(--secondary-color);
}
```

**Submission:** Save both files in the same folder and open `index.html` using Live Server. Change `--primary-color` in `:root` to see multiple elements update automatically.