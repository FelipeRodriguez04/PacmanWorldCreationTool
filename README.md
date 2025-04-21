<body style="font-family: Consolas, sans-serif; font-weight: normal; font-size: 12pt; color: beige">

<blockquote style="font-style: italic; color: whitesmoke"> <blockquote style="font-style: italic; color: whitesmoke; font-size: 9pt; text-align: center"> Hi there! I’m a huge fan of Markdown documents, so apologies in 

advanced for structuring this as one </blockquote>

***

<blockquote style="font-style: italic; color: whitesmoke">

<h2 style="color: beige; font-size: 14pt">&boxUR; Project Members &boxUL;  </h2>

<ul>

<li>Josué Daniel Ponce Vallejo [00330341]</li>

<li>Felipe José Rodríguez Gavela [00330528]</li>

<li>Santiago Francisco Arellano Jaramillo [00328370]</li>

</ul>

 </blockquote>

***

<h3 style="text-align: center; font-size: large"> MARIE Assembly Language Project: Simulating Pacman on a 16x16 Display</h3>

<h4 style="text-align: center; font-size: medium"> The following contains the information pertaining the project developed as the final project for the Computer Organization course given at USFQ. The idea of this final project was 

to implement a simulated game of Pac-man through the MARIE assembly programming language, using a reduced model to implement the game and practice assembly programming</h4>

***

<div style="display: flex; justify-content: center; align-content: center"> 

![Java](https://img.shields.io/badge/MARIE_Assembly_Language-%23ED8B00.svg?style=for-the-badge&logo=wasm&logoColor=white)

![JavaFX](https://img.shields.io/badge/python-%23FF0000.svg?style=for-the-badge&logo=python&logoColor=white)

</div>

<blockquote style="font-style: italic; color: whitesmoke">

<h2 style="color: beige; font-size: 14pt">&boxUR; Repository Description &boxUL;  </h2>

<p>

  This is the holder repository for the project defined as the final project for the Computer Organization course taught at USFQ. The idea of the project was to present a simulation of the Pac-man game based 

  on a simple model: movement, points, and entity management. Therefore, the project presented here has two clear components, the first is the Python tool developed to create, manipulate and modify maps within 

  the application, and the other is the actual game implementation held within a single file in the srcMARIE folder. The idea of this project was not only to introduce advanced game programming concepts like entity and asset 

  management, as well as event management, but also to translate OOP and Functional Programming practices down to the MARIE assembly language.

</p>

<p>

  To do this, the project implements various functional and OOP programming concepts like the <i>Single Responsibility Principle</i>, as well as design patterns like Adapter to handle events and information management. The 

  implementations of these are stored within the source code for our project present in the srcMARIE folder. On the other hand, the Python application implemented to design the map, and output the map to either the clipboard 

  or a file,  is stored in the src folder. 

</p>

<p>

  The project was carried out through Sprints, working on different sections of the application, entity management, map management, movement, and event handling in separate sections, focusing on decoupling, JnS methods and simplicity

  to handle communication and the overall architecture of the application, keeping it simple, streamline and simple to follow. As such, we tested the code thoroughly, working on each section with care and attention to detail but working 

  quickly to make sure the project was finished on time.

</p>

<ul>

<code>File Structure</code>

<li><b>src</b>: As mentioned above, the code is divided into two sections, and the files here are all part of the code developed to create, export, and modify map files for MARIE. The process through which this is done is explained

further down.</li>

  <li><b>srcMARIE</b>: As mentioned above, this section contains only the MARIE code done for the project, refined and tested as per the Pull Request recorded in this repository, this was the main way of code storage and communication 

  bewteen the team as we did not want to push changes into the main branch until we were done with the project.</li>

</ul>

</blockquote>

***

<blockquote style="font-style: italic; color: whitesmoke">

<h2 style="color: beige; font-size: 14pt">&boxUR; Methodology &boxUL;  </h2>

<p>

  Within the file structure of this project, there are two specific sections that matter, the first is the python (the only high level language implementation) code used to create, modify and export maps directly to code understood 

  by the MARIE lexer and assembler such that we could test quickly maps, test implementation details, as well as the whole system during our integration testing. The code presented here makes use of different python libraries, the most 

  important being <b><code>PyQT5</code></b>, which was used to handle the user desktop application view. Using this library, we were able to create a simple, fast and powerful layout that was both visually appealing and useful, allowing 

  for brush painting, single spot painting, as well as valildation with respect to the amount of entities were already placed on the canvas. 

</p>

<p>To implement this we focused on retrieving the concepts seen in the MVC pattern discussed for JavaFX and simulating both a similar style of application, as well as a similar view management and event handling. While this library proved hard to use, given that it was a first for all of us in the team, we managed to pull through and create a usable UI for this kind of application</p>

<p>

The second section of the program, held within the srcMARIE folder contains an implementation of the Pacm-man arcade game simulated within the system using this language. To handle this implementation the game is divided into different sections, specifically three, which handle three core concepts, movement, collision detection, and data storage. To implement the first section, we worked on handling future movements before they happened, checking if these were possible to implement before we skipped to do the next. In addition, we reviewed collisions with other map objects, like walls, as well as display limits (since the MARIE display only uses a 16x16 grid, we had to handle errors like overflowing). This section took us the longest as it was a completely different style of programming than what we are used to work in, as well as language. 

</p>

<p>

The second component within the second section of the project, was all about handling  the collisions that could happen between Pac-man and ghosts, or viceversa, as well as coins and powerups. To implement this, we introduced adapters as well as composition to append checks to the original flow of the application, rather than implementing whole new methods expanding the original, already defined and proven methods. This then allowed us to extend methods by composing functions, rather than changing methods entirely or rewriting them.

</p>

<p>

The last component of the second section of our project, was all about storing the data and reading the data, this component was all encompassing, as we had to handle a ton of variables and locations of these variables to make the program work. This meant that we required robust, and redundant code  to make varaible copying, variable modification, and resetting secure, robust, and quick. To do this we had to explore different JnS methods to handle loading information, mathematical operations to analyze locations, and other approaches to variable handling and storage. 

</p>

</blockquote>

***



</body>
