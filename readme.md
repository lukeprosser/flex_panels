# Flex Gallery
An image gallery featuring dynamic spacing, built as part of 'JavaScript30' with Wes Bos.

The gallery images and text adjust size dynamically on click, utilising CSS Flexbox and vanilla JavaScript.

Live demo: Coming soon

## HTML
Markup consists of a containing div with the class 'panels', holding all 5 panels, each with a class of 'panel'. Each individual panel features 3 <p> tags with title wording.

## CSS
The CSS is more detailed, with various settings for Flexbox and transitions:
<ul>
  <li>'.panels' div set to 'display: flex'.</li>
  <li>Each individual '.panel' div features a background image, 'flex: 1' (so that the images spread evenly throughout the page), items aligned center, content justified center, a display of flex and 'flex-direction: column'.</li>
  <li>Each panel also has transition timings set for the font-size, flex and background, in readiness for the click interaction.</li>
  <li>The first and last panel paragraph tags are set to display off the page by default (so that they can appear via transform) using translateY.</li>
  <li>A second class of 'open-active' is set up so that the Y-position of the titles can be reset using JavaScript.</li>
  <li>Finally, a class of 'open' is set up so that paragraphs can be given a larger font size and the panel can expand to be 5 times larger than it's siblings (when assigned via click).</li>
</ul>

## JavaScript
The JS is actually relatively simple.
<ul>
  <li>All panels are selected and stored in a variable 'panels'.</li>
  <li>A function called 'toggleOpen' alternates a class '.open'.</li>
  <li>A function called 'toggleActive' takes in an event and toggles a class of '.open-active' if the event element's property name includes 'flex'.</li>
  <li>Loop through all panels and assign a click event that calls the 'toggleOpen' function.</li>
  <li>Loop through all panels and assign a transitionend event that calls the 'toggleActive' function. This prevents the top and bottom title text from loading in until the panel has finished expanding.</li>
</ul>