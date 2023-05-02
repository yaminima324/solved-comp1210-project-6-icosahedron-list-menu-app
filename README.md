Download Link: https://assignmentchef.com/product/solved-comp1210-project-6-icosahedron-list-menu-app
<br>
You will write a program this week that is composed of three classes: the first class defines Icosahedron objects, the second class defines IcosahedronList objects, and the third, IcosahedronListMenuApp, presents a menu to the user with eight options and implements these: (1) read input file (which creates an icosahedronList object), (2) print report, (3) print summary, (4) add an icosahedron object to the IcosahedronList object, (5) delete an icosahedron object from the IcosahedronList object, (6) find an icosahedron object in the IcosahedronList object, (7) Edit an icosahedron in the IcosahedronList object, and (8) quit the program.<strong> [You should create a new “Project 6” folder and copy your Project 5 files </strong>(Icosahedron.java, IcosahedronList.java, icosahedron_data_1.txt, and icosahedron_data_0.txt)<strong> to it, rather than work in the same folder as Project 5 files.] </strong>




<table width="586">

 <tbody>

  <tr>

   <td colspan="3" width="586">An <strong>Icosahedron</strong> has 20 equilateral triangle faces, 12 vertices, and 30 edges as depicted below. The formulas are provided to assist you in computing return values for the respective methods in the Icosahedron class described in this project.</td>

  </tr>

  <tr>

   <td width="191"></td>

   <td width="191"> Surface Area (A) Volume (V) Edge length (a) Surface/Volume ratio (A/V)</td>

   <td width="204"></td>

  </tr>

  <tr>

   <td colspan="3" width="586"></td>

  </tr>

 </tbody>

</table>

<strong>       </strong>

<strong>Icosahedron.java (<u>assuming that you successfully created this class in Project 4, just copy</u> <u>the file to your new Project 6 folder and go on to IcosahedronList.java on page 4.</u>  <u>Otherwise, you will need to create Icosahedron.java as part of this project</u>.) </strong>

<strong> </strong>

<strong>Requirements</strong>: Create an Icosahedron class that stores the label, color, and edge (i.e., length of an edge, <u>which must be greater than zero</u>).  The Icosahedron class also includes methods to set and get each of these fields, as well as methods to calculate the surface area, volume, and surface

to volume ratio of an Icosahedron object, and a method to provide a String value of an Icosahedron object (i.e., a class instance).




<strong>Design</strong>:  The Icosahedron class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (instance variables): label of type String, color of type String, and edge of type double. Initialize the Strings to “” and the double to 0 in their respective declarations. These instance variables should be private so that they are not directly accessible from outside of the Icosahedron class, and <u>these should be the only instance variables in the class</u>.</li>

</ul>




<ul>

 <li><strong>Constructor</strong>: Your Icosahedron class must contain a public constructor that accepts three parameters (see types of above) representing the label, color, and edge. Instead of assigning the parameters directly to the fields, the respective set method for each field (described below) should be called. For example, instead of the statement label = labelIn; use the statement setLabel(labelIn); Below are examples of how the constructor could be used to create Icosahedron objects.  Note that although String and numeric literals are used for the actual parameters (or arguments) in these examples, variables of the required type could have been used instead of the literals.</li>

</ul>




Icosahedron example1 = new Icosahedron(“Small”, “blue”, 0.01);




Icosahedron example2 = new Icosahedron(”    Medium    “, “orange”, 12.3);




Icosahedron example3 = new Icosahedron(“Large”, ”  white  “, 123.4);




<ul>

 <li><strong>Methods</strong>: Usually a class provides methods to access and modify each of its instance variables (known as get and set methods) along with any other required methods. The methods for Icosahedron, which should each be public, are described below.  See formulas in Code and Test below. o getLabel:  Accepts no parameters and returns a String representing the label field.

  <ul>

   <li>setLabel: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the label field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getColor: Accepts no parameters and returns a String representing the color field.</li>

   <li>setColor: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the color field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getEdge: Accepts no parameters and returns a double representing the edge field.</li>

   <li>setEdge: Accepts a double parameter and returns a boolean as follows. If the edge is greater than zero, sets the edge field to the double passed in and returns true.  Otherwise, the method returns false and the edge is not set.  o surfaceArea:  Accepts no parameters and returns the double value for the total surface area calculated using the value for edge.</li>

   <li>volume: Accepts no parameters and returns the double value for the volume calculated using the value for edge.</li>

   <li>surfaceToVolumeRatio: Accepts no parameters and returns the double value calculated by dividing the total surface area by the volume.</li>

   <li>toString: Returns a String containing the information about the Icosahedron object formatted as shown below, including decimal formatting (“#,##0.0#####”) for the double values.  Newline and tab escape sequences should be used to achieve the proper layout.  In addition to the field values (or corresponding “get” methods), the following methods should be used to compute appropriate values in the toString method:</li>

  </ul></li>

</ul>

surfaceArea(), volume(), and surfaceToVolumeRatio().  Each line should have no trailing spaces (e.g., there should be no spaces before a newline (
) character).  The toString value for example1, example2, and example3 respectively are shown below (the blank lines are not part of the toString values).

Icosahedron “Small” is “blue” with 30 edges of length 0.01 units.

surface area = 0.000866 square units    volume = 0.000002 cubic units    surface/volume ratio = 396.950723




Icosahedron “Medium” is “orange” with 30 edges of length 12.3 units.

surface area = 1,310.209833 square units    volume = 4,059.844212 cubic units    surface/volume ratio = 0.322724




Icosahedron “Large” is “white” with 30 edges of length 123.4 units.

surface area = 131,874.537977 square units    volume = 4,099,581.395236 cubic units    surface/volume ratio = 0.032168







<strong>Code and Test</strong>: As you implement your Icosahedron class, you should compile it and then test it using interactions.  For example, as soon you have implemented and successfully compiled the constructor, you should create instances of Icosahedron in interactions (e.g., copy/paste the examples above).  Remember that when you have an instance on the workbench, you can unfold it to see its values.  You can also open a viewer canvas window and drag the instance from the Workbench tab to the canvas window.  After you have implemented and compiled one or more methods, create an Icosahedron object in interactions and invoke each of your methods on the object to make sure the methods are working as intended.  You may find it useful to create a separate class with a main method that creates an instance of Icosahedron then prints it out.  This

would be similar to the IcosahedronApp class you will create below, except that in the IcosahedronApp class you will read in the values and then create and print the object.







<strong>IcosahedronList.java – </strong>extended from Project 5 by <strong>adding the last six methods below.  </strong>

<strong>(<u>Assuming that you successfully created this class in Project 5, just copy</u> </strong>

<strong><u>IcosahedronList.java to your new Project 6 folder and then add the indicated methods.</u>  <u>Otherwise, you will need to create all of IcosahedronList.java as part of this project</u>.)</strong>




<strong>Requirements</strong>: Create an IcosahedronList class that stores the name of the list and an ArrayList of Icosahedron objects.  It also includes methods that return the name of the list, number of Icosahedron objects in the IcosahedronList, total surface area, total volume, average surface area, average volume, and average surface to volume ratio for all Icosahedron objects in the IcosahedronList.  The toString method returns a String containing the name of the list followed by each Icosahedron in the ArrayList, and a summaryInfo method returns summary information about the list (see below).




<strong>Design</strong>:  The IcosahedronList class has two fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (or instance variables): (1) a String representing the name of the list and (2) an ArrayList of Icosahedron objects. These are the only fields (or instance variables) that this class should have, and both should be private.</li>

 <li><strong>Constructor</strong>: Your IcosahedronList class must contain a constructor that accepts a parameter of type String representing the name of the list and a parameter of type ArrayList&lt; Icosahedron&gt; representing the list of Icosahedron objects. These parameters should be used to assign the fields described above (i.e., the instance variables).</li>

</ul>

<strong> </strong>

<ul>

 <li><strong>Methods</strong>: The methods for IcosahedronList are described below.

  <ul>

   <li>getName: Returns a String representing the name of the list.</li>

   <li>numberOfIcosahedrons: Returns an int representing the number of Icosahedron objects in the IcosahedronList.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

   <li>totalSurfaceArea: Returns a double representing the total surface areas for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

   <li>totalVolume: Returns a double representing the total volumes for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

   <li>averageSurfaceArea: Returns a double representing the average surface area for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

   <li>averageVolume: Returns a double representing the average volume for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

   <li>averageSurfaceToVolumeRatio: Returns a double representing the average surface to volume ratio for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

   <li>toString: Returns a String (does <u>not</u> begin with 
) containing the name of the list followed by each Icosahedron in the ArrayList.  In the process of creating the return result, this toString() method should include a while loop that calls the toString() method for each Icosahedron object in the list (adding a 
 before and after each).  Be sure to include appropriate newline escape sequences.  For an example, see <u>lines 2 through 19</u> in the output below from IcosahedronListApp for the <em>txt</em> input file. [Note that t<u>he toString result should <strong>not</strong> include the summary items in lines 20 through</u> <u>26 of the example.  These lines represent the return value of the summaryInfo method</u> <u>below.</u>]</li>

   <li>summaryInfo: Returns a String (does<u> not </u>begin with 
) containing the name of the list (which can change depending of the value read from the file) followed by various summary items:  number of Icosahedrons, total surface area, total volume, average surface area, average volume, and average surface to volume ratio.  Use “#,##0.0##” as the pattern to format the double values.  For an example, see <u>lines 20 through 26</u> in the output below from IcosahedronListApp for the <em>txt</em> input file.  The second example below shows the output from IcosahedronListApp for the <em>icosahedron_data_0.txt</em> input file which contains a list name but no Icosahedron data. <strong> </strong></li>

  </ul></li>

</ul>

<strong> </strong>

<ul>

 <li><strong><u>The following six methods are new in Project 6</u>: </strong></li>

</ul>

<ul>

 <li>getList: Returns the ArrayList of Icosahedron objects (the second field above).</li>

 <li>readFile: Takes a String parameter representing the file name, reads in the file, storing the list name and creating an ArrayList of Icosahedron objects, uses the list name</li>

</ul>

and the ArrayList to create an icosahedronList object, and then returns the

IcosahedronList object.  See note #1 under <u>Important Considerations</u> for the

IcosahedronListMenuApp class (last page) to see how this method should be called. <strong> </strong>

<ul>

 <li>addIcosahedron: Returns nothing but takes three parameters (label, color, and edge), creates a new Icosahedron object, and adds it to the IcosahedronList object. o findIcosahedron:  Takes a label of an icosahedron as the String parameter and returns the corresponding Icosahedron object if found in the IcosahedronList object; otherwise returns null.  <u>Case should be ignored when attempting to match the label</u>.</li>

 <li>deleteIcosahedron: Takes a String as a parameter that represents the label of the Icosahedron and returns the Icosahedron if it is found in the IcosahedronList object and deleted; otherwise returns null.  <u>Case should be ignored when attempting to match the</u> <u>label; consider calling/using </u><u>findIcosahedron in this method</u>.</li>

 <li>editIcosahedron: Takes three parameters (label, color, and edge), uses the label to find the corresponding the Icosahedron object.  If found, sets the color and edge to the values passed in as parameters, and returns true.  If not found, returns false.</li>

</ul>

<strong> </strong>

<strong>Code and Test</strong>: Remember to import java.util.ArrayList, java.util.Scanner, java.io.File, java.io.FileNotFoundException.  These classes will be needed in the readFile method which will require a throws clause for FileNotFoundException.  Some of the methods above require that you use a loop to go through the objects in the ArrayList.  You may want to implement the class below in parallel with this one to facilitate testing.  That is, after implementing one to the methods above, you can implement the corresponding “case” in the switch for menu described below in the IcosahedronListMenuApp class.




<strong>IcosahedronListMenuApp.java </strong> (replaces IcosahedronListApp class from Project 5)




<strong>Requirements</strong>: Create an icosahedronListMenuApp class with a main method that presents the user with a menu with eight options, each of which is implemented to do the following: (1) read the input file and create an icosahedronList object, (2) print the IcosahedronList object, (3) print the summary for the IcosahedronList object, (4) add an icosahedron object to the IcosahedronList object, (5) delete an icosahedron object from the IcosahedronList object, (6) find an icosahedron object in the IcosahedronList object, (7) Edit an icosahedron object in the IcosahedronList object, and (8) quit the program.




<strong>Design</strong>:  The main method should print a list of options with the action code and a short description followed by a line with just the action codes prompting the user to select an action.  After the user enters an action code, the action is performed, including output if any.  Then the line with just the action codes prompting the user to select an action is printed again to accept the next code.  The first action a user would normally perform is ‘R’ to read in the file and create an icosahedronList object.  However, the other action codes should work even if an input file has not been processed. The user may continue to perform actions until ‘Q’ is entered to quit (or end) the program.  Note that your program should accept both uppercase and lowercase action codes.       Below is output produced after printing the action codes with short descriptions followed by the prompt with the action codes waiting for the user to make a selection.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">12345678910</td>

   <td width="511">Icosahedron List System MenuR – Read File and Create Icosahedron ListP – Print Icosahedron ListS – Print SummaryA – Add IcosahedronD – Delete IcosahedronF – Find IcosahedronE – Edit IcosahedronQ – QuitEnter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

Below shows the screen after the user entered ‘r’ and then (when prompted) the file name.  Notice the output from this action was “File read in and Icosahedron List created”.  This is followed by the prompt with the action codes waiting for the user to make the next selection.  You should use the <em>icosahedron_data_1.txt </em>file from Project 5 to test your program.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">12345</td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: rFile name: icosahedron_data_1.txtFile read in and Icosahedron List created Enter Code [R, P, S, A, D, F, E, or Q]:</td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘p’ to Print Icosahedron List is shown below and next page.




<table width="625">

 <tbody>

  <tr>

   <td width="54">Line #</td>

   <td width="571">Program output</td>

  </tr>

  <tr>

   <td width="54">12345678910111213141516171819 </td>

   <td width="571">Enter Code [R, P, S, A, D, F, E, or Q]: pIcosahedron Test List Icosahedron “Small” is “blue” with 30 edges of length 0.01 units.    surface area = 0.000866 square units    volume = 0.000002 cubic units    surface/volume ratio = 396.950723 Icosahedron “Medium” is “orange” with 30 edges of length 12.3 units.surface area = 1,310.209833 square units    volume = 4,059.844212 cubic units    surface/volume ratio = 0.322724 Icosahedron “Large” is “white” with 30 edges of length 123.4 units.    surface area = 131,874.537977 square units    volume = 4,099,581.395236 cubic units    surface/volume ratio = 0.032168 Enter Code [R, P, S, A, D, F, E, or Q]: <em> </em></td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘s’ to print the summary for the list is shown below.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">1234567891011 </td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: s —– Summary for Icosahedron Test List —–Number of Icosahedrons: 3Total Surface Area: 133,184.749Total Volume: 4,103,641.239Average Surface Area: 44,394.916Average Volume: 1,367,880.413Average Surface/Volume Ratio: 132.435 Enter Code [R, P, S, A, D, F, E, or Q]: <em> </em></td>

  </tr>

 </tbody>

</table>




The result of the user selecting ‘a’ to add an icosahedron object is shown below.  Note that after ‘a’ was entered, the user was prompted for label, color, and edge.  Then after the Icosahedron object is added to the Icosahedron List, the message “*** Icosahedron added ***” was printed.  This is followed by the prompt for the next action. After you do an “add”, you should do a “print” or a “find” to confirm that the “add” was successful.




<table width="566">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="511">Program output</td>

  </tr>

  <tr>

   <td width="55">1234567 </td>

   <td width="511">Enter Code [R, P, S, A, D, F, E, or Q]: aLabel: NewIcosahedronColor: navy blueEdge: 12.5*** Icosahedron added *** Enter Code [R, P, S, A, D, F, E, or Q]: <em> </em></td>

  </tr>

 </tbody>

</table>


