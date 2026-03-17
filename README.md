In this assignment, start with the base “Notes to Self” app in index.html

A few things to note about this app:

- It has input fields! This app has two: an `<input>` field for a title, with id title, and a larger `<textarea>` field for the note itself. The code on lines 30-31 is what lets you get the current text in those fields, using the .value property. (Note: you can also use the `.value` property to set the content of those fields, just pass in a value or an empty string, like in lines 42-43.)
- The “Add Note” button calls the `addNote` function when clicked. (This connection is set up by line 18: `addEventListener("click", addNote)`.)
- In `createNoteDiv`, the different parts of the `div` for the new note are appended to the main note `div`. The main div itself has the class "note", while the titleElement and noteElement each use the `.textContent` property to attach the specific text from the specific input to each subelement.
- The app uses JSON to record the notes in your browser's localStorage (line 49) and loads them into the page on startup (lines 20-26).
- Take some time to read through this code to make sure you understand what it does. We like to “poke” at code a bit when we're doing this, to really make sure we understand what's going on. Often this looks like adding console.log() statements in various places to confirm our understanding of, say, what happens when a button is clicked. But it can also look like minor changes made to see what breaks—by, say, changing the id of the input, textarea, button, or notes div.

## On to the assignment!

- Fix the formatting! Right now, the notes show up as a very plain subject & post on two separate lines. Add some formatting by, perhaps, bolding the subject, or prefixing the word "Subject:" to it, adding an extra line break between notes, etc.—use your design skills to think about what would make this look better, and then implement it. Anything goes here: feel free to use CSS, extra HTML elements, etc.
- Clear the inputs after adding the note. In other words, after saving the note, blank out the Subject and Post fields so that the page is ready to accept your next note.
- Number the notes. One way to do this is to add notes.length to the appended text to add a number. Or, make a new element for it. Or, use an ordered list, <ol>! Bonus points: update a <span> somewhere on the page with a "total notes count" that just tracks how many notes have been added in total.
- Challenge: Add an extra field to the notes, perhaps a "category" or "urgency". Feel free to use a text input (like title) and pattern match using the existing code. Or, get creative and try using a <select> dropdown element!

