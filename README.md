# Project Nemo
Project Nemo — Proposal Website

Project Nemo is an interactive, animated, and fully personalized proposal website designed with HTML, CSS, and JavaScript.
It includes dynamic UI behavior, music playback, Firebase logging, smooth animations, and a passcode-protected entry system.

Features
1. Passcode-Protected Entry

The website begins with a landing screen.

Access is granted only after entering the correct passcode.

On successful entry, the page title dynamically changes to “I love you apoorva”.

2. Personalized Visual Experience

Custom gradients and modern UI styling using the Poppins font.

Multiple sections with images, compliments, and flirty notes.

Designed as a multi-section scrolling page with animations and photo galleries.

3. Interactive “Yes / No” Proposal

A “Yes” button triggers:

Confetti animation

Floating hearts

Transition to a dedicated success screen

Firebase logging of the response and page interaction data

A “No” button:

Moves away on hover

Displays playful popup messages

Counts how many times it was clicked

4. Analytics Tracking

The website tracks:

Time spent on each section

Number of times each section was viewed

Time spent reading paragraphs

Total time on page

Passcode failure count

User’s browser metadata

This data is pushed into Firebase Realtime Database on the Yes response.

5. Anti-Inspection Scripts

Blocks:

Right-click

F12

Ctrl+Shift+I / J / C

Ctrl+U

(to prevent casual users from accessing source files)

6. Background Music

Auto-plays at a specified timestamp after successful passcode entry.

Tech Stack
Component	Technology Used
Frontend	HTML5, CSS3, JavaScript
Animations	CSS Keyframes, Canvas Confetti
Fonts	Google Fonts (Poppins)
Database / Logs	Firebase Realtime Database
Media Assets	Local image + audio files
Project Structure
/
|-- index.html
|-- res/
|   |-- song.mp3
|   |-- photo-1.png
|   |-- photo-2.png
|   |-- photo-3.png
|   |-- ...
|-- README.md


Images and audio are stored in the res/ directory.

How It Works
1. User opens the site

The landing screen appears with a button titled Open.

2. User enters passcode

If correct:

The landing screen disappears

Background music starts at 25 seconds

Main content loads

Page title changes

If incorrect:

Access denied

Failure count increments

3. User scrolls

Each section triggers view and timing analytics.

4. User answers the proposal

Yes → animations + data logged + final page

No → button escapes + funny message

Setup Instructions

Clone this repository:

git clone https://github.com/your-username/project-nemo.git
cd project-nemo


Add your Firebase configuration inside index.html under:

const firebaseConfig = { ... }


Place your images and audio in the res/ folder.

Deploy using any static hosting option:

GitHub Pages

Deployment (GitHub Pages)

Commit all files

Go to Repository → Settings → Pages

Select branch: main

Select folder: /root

Save
The site will be available in a few minutes.

License

This project is personal and not intended for reuse, redistribution, or commercial purposes.

If you want, I can also create:

A banner for the README

A GitHub Pages-optimized version

A cleaner minified HTML/CSS/JS bundle

A separate config.js file to externalize settings
