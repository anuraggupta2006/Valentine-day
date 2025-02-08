# Will You Be My Valentine? 💌

This project is designed to be an interactive webpage to ask someone to be your Valentine. Please use this code as inspiration and avoid simply copying it without understanding or giving credit.

---

## How It Works 

This project consists of a simple webpage with a "Yes" and "No" button. When the user clicks the "No" button, the button text changes to a series of  messages, and the "Yes" button grows larger. If the user clicks the "Yes" button, they are redirected to a new page (`yes_page.html`).

### Features:
- **Interactive Buttons**: The "No" button cycles through , while the "Yes" button grows in size.
- **Responsive Design**: The webpage is designed to work on all screen sizes.

---

## How to Use 

1. **Download the Files**:
   - Clone this repository or download the `index.html`, `styles.css`,`yes_style.css`,`yes_page.html` and `script.js` files.

2. **Open the Project**:
   - Open the `index.html` file in your web browser.


---

## A Note on Code Usage 

While I am happy to share this project, I encourage you to use it as inspiration.
If you use this code as a base for your own project, please give credit where it's due. A simple shoutout or link back to this repository is appreciated!

---

## Code Overview 

### Files:

- `index.html`: The main HTML file that structures the webpage.
- `styles.css`: The CSS file that styles the webpage.
- `script.js`: The JavaScript file that handles the button interactions.
- `yes_page.html`: The yes page that sturctures the webpage.
- `yes_style.css`: The css file that styles the yes webpage.



### Key Functions:

- `handleNoClick()`: Changes the "No" button text and increases the size of the "Yes" button.
- `handleYesClick()`: Redirects the user to `yes_page.html`.

---

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Enjoy 💖



body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f9e3e3;
    font-family: 'Arial', sans-serif;
    flex-direction: column;
  }
  
  .container {
    text-align: center;
  }
  
  h1 {
    font-size: 2.5em;
    color: #d32f2f;
  }
  
  .buttons {
    margin-top: 20px;
  }
  
  .yes-button {
    font-size: 1.5em;
    padding: 10px 20px;
    margin-right: 10px;
    background-color: #4caf50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .no-button {
    font-size: 1.5em;
    padding: 10px 20px;
    background-color: #f44336;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .gif_container img {
    max-width: 100%;
    height: auto;
    border-radius: 10px;
    margin-top: 20px;
  }
const messages = [
    "Are you sure?",
    "Really sure??",
    "Are you positive?",
    "Pookie please...",
    "Just think about it!",
    "If you say no, I will be really sad...",
    "I will be very sad...",
    "I will be very very very sad...",
    "Ok fine, I will stop asking...",
    "Just kidding, say yes please! ❤️"
];

let messageIndex = 0;

function handleNoClick() {
    const noButton = document.querySelector('.no-button');
    const yesButton = document.querySelector('.yes-button');
    noButton.textContent = messages[messageIndex];
    messageIndex = (messageIndex + 1) % messages.length;
    const currentSize = parseFloat(window.getComputedStyle(yesButton).fontSize);
    yesButton.style.fontSize = `${currentSize * 1.5}px`;
}

function handleYesClick() {
    window.location.href = "yes_page.html";
}
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f9e3e3;
    font-family: 'Arial', sans-serif;
}

.container {
    text-align: center;
}

.header_text {
    font-size: 3em;
    color: #d32f2f;
}

.gif_container img {
    width: 100%; 
    max-width: 500px; 
    height: auto; 
}