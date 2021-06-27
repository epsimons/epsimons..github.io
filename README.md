# Ethan Simons

## My ePortfolio

###  Narratives
The artifact I am using is my gz_to_xz_converter.py program. What it does is scour a directory and convert any GZip files it finds into XZip files. This was created for a work project where I needed to create more space on a hard drive. Within this artifact are examples of software design and engineering, algorithms and data structures, and databases. For the software design and engineering portion, I chose this artifact because it imports libraries to utilize, the components are modular, and reusable if needed. Certain command line inputs are expected, and some are optional, and the program now outputs data to three different outputs: the screen, a log file, and a database. For the algorithms and data structures, there are arrays, lists, variables to hold values and objects. Calculations and manipulations of lists must occur as the program compiles a list and splits this list into separate lists for every available thread. The database is a late inclusion that takes some of the output of the program and inserts it into a MongoDB database. If the database does not exist, it gets automatically created, then documents are added to the database as the program runs. 

This item has been included in my ePortfolio because it showcases my ability to use different data structures, object-oriented programming, and my ability to call in and utilize various external libraries. It also shows my ability to create a database and insert data into it. The process of enhancing this artifact allowed me to find some errors and clean up the code a bit. I started with the original program, and I cleaned up the code. I went through the code looking for variables that were not named in a way that tells you what it does. Next I added and cleaned up some of the comments that were there to be more descriptive. Coming back to a project after some time can make it hard to remember all the abbreviations you used when naming things. I added the database and then every time there was a call to send data to the log file, it now also sends some information to the database. I at some point, this program may rely entirely on the database, so it can scan the records and see if a particular file had been processed.

### Code Evaluation

Link to program before corrections were made: 

https://github.com/epsimons/Python/blob/main/gz_to_xz_converter.py

Link to program after corrections were made:

https://github.com/epsimons/Python/blob/main/gz_to_xz_converter_V3.0.2.py

### Software Review

Video of software:

https://youtu.be/ETi62wgwrhM




<html>
  <body>
<iframe width="560" height="315" src="https://www.youtube.com/embed/ETi62wgwrhM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </body>
  </html>

