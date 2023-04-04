# Using ChatGPT-4 to Design a Website From Scratch

<https://chat.openai.com/>

This project is an attempt to build a website entirely from scratch using nothing but ChatGPT-4 prompting. With each prompt, the website code is updated, errors/bugs are reported to ChatGPT, and the process continues. The website itself was built for local non-profits and required interactivity, at least some dynamic scaling, and custom and easily changeable information/data. 

The only instances of a human editing the code were simple replacements of existing key information (such as color codes, URLs, and text) without changing the functionality of the code itself.

The essential structure of each prompt follows this format: context of the issue at hand, the issue itself, and the requested assistance.

## About This Document

This document is intended to share the prompting used for the project as a whole. Each prompt below includes a summary/explanation of what happened that required the following prompt. 

## Prompts

<ul>
<li>
<details open="open">
  <summary>Initial Prompt: request plan of attack</summary>
  I need to create a webpage titled "The Periodic Table of Black History". This webpage will need:

    1. A grid of squares modeled after the table of elements, but with:

      1a. The initials of historical figures instead of chemical symbols
  
      1b. The date of birth of historical figures instead of mass

    2. Each square to be a button that, when clicked, reveals a modal window (or light box) which:

      2a. Slides from the right side of the page, covering the entire site
    
      2b. Is to be populated (from a CSV file) with:

        2b-i. The historical figure's name at the top
  
        2b-ii. The historical figure's date of birth (and optionally date of death) in parentheses to the right of their name
  
        2b-iii. An optional YouTube video (in the CSV as a URL) embedded below the name and date(s)
  
        2b-iv. An image (in the CSV as a URL) of the historical figure below the name/dates or below the video if included
    
        2b-v. A paragraph of text about the historical figure to the right of their image

        2b-vi. Has an X to close the modal window, returning the viewer to the table

    3. To be a responsive design so that viewers using different devices can navigate the webpage

Please help me by creating an outline of steps needed to build this page.
<li>
<details>
  <summary>Request HTML</summary>
  I need to create a webpage titled "The Periodic Table of Black History". This webpage will need:
  
    1. A grid of squares modeled after the table of elements, but with:

      1a. The initials of historical figures instead of chemical symbols
  
      1b. The date of birth of historical figures instead of mass

    2. Each square to be a button that, when clicked, reveals a modal window (or light box) which:

      2a. Slides from the right side of the page, covering the entire site
    
      2b. Is to be populated (from a CSV file) with:

        2b-i. The historical figure's name at the top
  
        2b-ii. The historical figure's date of birth (and optionally date of death) in parentheses to the right of their name
  
        2b-iii. An optional YouTube video (in the CSV as a URL) embedded below the name and date(s)
  
        2b-iv. An image (in the CSV as a URL) of the historical figure below the name/dates or below the video if included
    
        2b-v. A paragraph of text about the historical figure to the right of their image

        2b-vi. Has an X to close the modal window, returning the viewer to the table

    3. To be a responsive design so that viewers using different devices can navigate the webpage

I would like to create this in the following steps:
  
    1. Set up the project structure:
  
      1a. Create an HTML file for the main structure of the webpage
  
      1b. Create a CSS file to style the webpage
  
      1c. Create a JavaScript file to handle interactivity and data fetching
  
    2. Design the main structure of the webpage in the HTML file
  
    3. Style the webpage using the CSS file
  
    4. Set up csv with the historical figures' data:
  
    5. Implement interactivity and data fetching in the JavaScript file
  
    6. Test the webpage on various devices and browsers to ensure compatibility and responsiveness.
  
    7. Deploy the webpage to a web server or hosting platform.
  
Can you first help me by giving me HTML for this project?
</details>
</li>
<li>
<details>
  <summary>Request CSS</summary>
  Can you create the styles.css file for me, based on the information I gave you?
</details>
</li>
</li>
<li>
<details>
  <summary>Request Javascript</summary>
  Excellent, can you create the Javascript next?
</details>
</li>
<li>
<details>
  <summary>Changes/Additions to CSV file</summary>
  I decided to include the element number for each figure in the first column of the csv file. Can you rewrite with that in mind?
</details>
</li>
<li>
<details>
  <summary>The Table did not have the needed blank spaces, but instead was just a grid of squares.</summary>
  
  Using Javascript in an HTML page (styled through CSS), I am trying to create a grid modeled after the Periodic Table of Elements, but with custom data in it pulled from a CSV file. Currently, the grid is displaying the squares 18 per row, which is a good start, but the requisite blank spaces (as needed in the periodic table) are not there. Here is the Javascript:
  
  [CODE BLOCK]
  
  Here is the CSS:
  
  [CODE BLOCK]
  
  I would like:

    1. The CSV file to have some entries filled with 0 in each field, indicating an empty entry
  
    2. The javascript to create the grid of squares (18 per row)

      2a. Creating a visible square with data for entries that have data
  
      2b. Creating an unclickable, invisible square with nothing in it for entries marked with 0

    3. The CSS to format:

      3a. The visible squares as visible (as they currently are)
  
      3b. The invisible squares as unclickable and not visible
  
      3c. The entire grid to scale to fit the browser window it is in
  
  Can you change these for me?
  </details>
</li>
<li>
<details>
  <summary>Modals only close with the x, and do not close when clicking outside the content.</summary>
  
  I have created a website with popup modals. Currently they can only be closed by clicking the X. I would like it to also be able to be closed by clicking anywhere outside the modal window. Here is the current code for closing a modal:
  
  [CODE BLOCK]
  
  Can you rewrite this to include what I need?
</details>
</li>
<li>
<details>
  <summary>If there is no video in a line of CSV, the space for a video is still there, resulting in a large blank spot</summary>
  
  I am making an HTML website, with data in a CSV that is pulled using Javascript, and all styled using CSS. Here is the Javascript:
  
  [CODE BLOCK]
  
  Here is the CSS:
  
  [CODE BLOCK]
  
  When clicking a square in the grid, a modal pops up. Right now, if a YouTube link is missing from the CSV file, there is a large blank space. I need the Javascript to put nothing into that area if a YouTube link is not found in the expected column of the CSV file. Can you help me rewrite the Javascript and CSS as necessary to fix this?
</details>
</li>
<li>
<details>
  <summary>Wanted to add a sticky header</summary>
  
  I am making an HTML website, with data in a CSV that is pulled using Javascript, and all styled using CSS. Here is the Javascript:
  
  [CODE BLOCK]
  
  Here is the CSS:
  
  [CODE BLOCK]
  
  Currently the content and header scroll together, but I would like the header to be sticky and the content to scroll behind it. Can you rewrite my code to ensure this happens?
</details>
</li>
</ul>
