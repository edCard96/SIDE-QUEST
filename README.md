# Side Quest: A Simple Guide to Basic Coding Concepts

![Side Quest Screenshot](https://placehold.co/600x400/1a1a2e/e0e0e0?text=Side%20Quest%20Preview)

An interactive, game-themed webpage designed to teach fundamental programming concepts to absolute beginners in a fun and engaging way.

## About The Project

"Side Quest" transforms the often daunting task of learning to code into an exciting adventure. By presenting core concepts like variables, functions, and loops as "quests" in a video game, it makes the information more relatable and easier to digest for a non-technical audience. The project is a single, self-contained HTML file that runs in any modern web browser, requiring no installation or setup.

The key goal is to provide a friendly first step into the world of programming, sparking curiosity and building confidence.

## Features

- **Interactive Quest System:** Lessons are structured as quests in a "Quest Log," allowing users to navigate and learn at their own pace.
- **Thematic Learning:** Complex topics are explained using simple, game-based analogies (e.g., variables as "magical labeled boxes").
- **Knowledge Checks:** Each quest concludes with a simple multiple-choice quiz to reinforce learning with instant feedback.
- **Dynamic Theming:** Users can select from multiple game genre themes (Fighting, RPG, Strategy, Horror, Adventure) that change the entire visual appearance of the page, including colors, fonts, and background textures.
- **Persistent Theme Choice:** The site remembers the user's last selected theme for a personalized experience on return visits.
- **Background Music:** An optional, royalty-free background track with a mute/unmute controller adds to the game-like atmosphere.
- **Fully Responsive:** The layout works smoothly on desktops, tablets, and mobile devices.

## How to Use

Simply open the `side-quest.html` file in any modern web browser (like Chrome, Firefox, Safari, or Edge). No internet connection is required after the initial page load.

1.  Select a visual theme from the dropdown in the top-left corner.
2.  Click on a quest in the "Quest Log" to start learning.
3.  Read through the content and take the quiz at the end.
4.  Use the "Next Quest" button to proceed or select another quest from the log.
5.  Use the music controller in the bottom-right corner to toggle the background music.

## Technologies Used

This project is built with standard web technologies and is designed to be as accessible as possible.

- **HTML5:** For the core structure and content.
- **Tailwind CSS:** For utility-based styling and layout.
- **Vanilla JavaScript:** For all interactivity, including quest display, quiz logic, theme switching, and audio control.
- **CSS Variables:** To allow for dynamic and easy theming.
- **Google Fonts:** For the unique, thematic fonts used in different visual modes.

## Customization

The project is designed to be easily extendable.

### Adding a New Quest

1.  Open the `side-quest.html` file in a text editor.
2.  Locate the `QUEST_DATA` constant in the `<script>` section.
3.  Add a new entry to the JavaScript object. The key should be a unique ID, and the value should be an object containing `title`, `icon`, `content`, and an optional `quiz` object.

    ```javascript
    "5": {
        title: "Your New Quest Title",
        icon: '✨',
        content: `
            <h2 class="font-title ...">New Quest</h2>
            <p>Your lesson content here, written in HTML.</p>
        `,
        quiz: {
            question: "What is your new question?",
            options: { "A": "Option 1", "B": "Option 2", "C": "Option 3" },
            answer: "B"
        }
    },
    ```

### Adding a New Theme

1.  In the `<style>` section, create a new `[data-theme="yourthemename"]` block.
2.  Define the values for the CSS variables within that block (e.g., `--bg-primary`, `--accent-primary`, `--heading-font`, etc.).
3.  Add the new theme as an `<option>` in the `#theme-select` dropdown in the HTML body.

## Credits

- **Music:** "8-bit Arcade" via [Pixabay](https://pixabay.com).
- **Textures:** [Transparent Textures](https://www.transparenttextures.com/).
- **Fonts:** [Google Fonts](https://fonts.google.com/).
