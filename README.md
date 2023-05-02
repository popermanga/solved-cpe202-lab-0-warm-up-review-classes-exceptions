Download Link: https://assignmentchef.com/product/solved-cpe202-lab-0-warm-up-review-classes-exceptions
<br>
<strong>Lab 0 – Warm up, Review, Classes, Exceptions! </strong>

Lab 0 is intended to make sure you have a working development environment, can properly define Python classes the way we will be using them in this class, can think through a logical problem, and can successfully commit and push code versions to a GitHub repository.

<h1>Part 1</h1>

<ol>

 <li>Checkout the starter code from GitHub by using the link on PolyLearn.</li>

 <li>Review the code in py. Note that there is a class definition for a Location class, and an associated __init__ method. In addition, there is code to create Location objects and print information associated with those objects.</li>

</ol>




<table width="0">

 <tbody>

  <tr>

   <td width="45"><strong>class </strong></td>

   <td width="58">Location</td>

   <td width="520">:</td>

  </tr>

  <tr>

   <td colspan="3" width="623">    <strong>def </strong>__init__(self, name, lat, long):</td>

  </tr>

 </tbody>

</table>

self.name = name    <em># string for name of location         </em>self.lat = lat      <em># latitude in degrees (-90 to 90)         </em>self.long = long    <em># longitude in degrees (-180 to 180)</em>




<ol start="3">

 <li>Without modifying the code, run location.py in whatever environment you wish (again, reference the Getting Started document if you need help in doing this)</li>

 <li>Note the information that is printed out for each Location object – you should see something like this:</li>

</ol>

Location 1: &lt;__main__.Location object at 0x000001F6A2E0C7B8&gt;

<ol start="5">

 <li>Since we haven’t provided any specific method to provide a representation for the class, Python uses a default method. What do you notice about the information for <sub>loc1</sub> and <sub>loc4</sub> ?</li>

 <li>Also note the result of the equal comparisons between the locations, in particular <sub>loc1==loc3</sub> and <sub>loc1==loc4</sub>. Make sure you understand why the results are what they are.</li>

 <li>Now modify the location.py code, adding in the methods (<sub>__eq__() and __repr__()</sub>). See the location_tests.py to figure out what the repr method should look like.</li>

 <li>Run the py code with the modifications made above.</li>

 <li>Now review the information printed out for each location. The __repr__ method of Location is now being used when printing the object.</li>

 <li>Examine the results of the equal comparisons. How are they different from before the __eq__ method is added?</li>

</ol>







<h1>Part 2</h1>




<ol>

 <li>Create a module called separator.py that has a main function that inputs numbers (integer and/or floats) from the keyboard and when the input stops (see below), outputs them on the screen in two lines:

  <ol>

   <li>The first line contains all integers in the order they were input (start the line with</li>

  </ol></li>

</ol>

“Integers: ”).

<ol>

 <li>The second line contains all non-integer numbers in the order they were input (start the line with “Floats: ”).</li>

</ol>

<ol start="2">

 <li>Allow at most N integer numbers and N non-integer numbers to be entered (<em>where N is a number obtained from a command-line argument.</em>)</li>

 <li>Stop taking input when one of the following occurs:

  <ol>

   <li>The user presses &lt;Enter&gt; after an empty line. (In this case, input returns an empty string.)</li>

   <li>An invalid value has been entered (something other than a number).</li>

   <li>An input number cannot be stored—i.e. either the (N+1)th integer or the (N+1)th float has been input.</li>

  </ol></li>

 <li><strong>Hints: </strong>isdigit(), float(), try…except…</li>

 <li><strong>No</strong> prompting should be done during this process. All output occurs after input is done.</li>

</ol>

<strong>Sample Run 1: </strong>

$ python3 separator.py 6

1 2 1.2 2.3

3

4

7.8 garbage, 12

Integers: 1 2 3 4

Floats: 1.2 2.3 7.8<strong>  </strong>

<strong> </strong>

<strong>Sample Run 2: </strong>

$ python3 separator.py 6

1 2 3 4

5 6 7 8

Integers: 1 2 3 4 5 6 Floats:




<strong> </strong>

<h1>Testing</h1>




Test your program thoroughly. Here are some examples of tests:




<ol>

 <li>The input contains only integers:

  <ol>

   <li>More than N integers</li>

   <li>Exactly N integers (followed by a blank line)</li>

   <li>Fewer than N integers (followed by a blank line)</li>

  </ol></li>

</ol>




<ol start="2">

 <li>The input contains only non-integer numbers:

  <ol>

   <li>More than N numbers</li>

   <li>Exactly N numbers (followed by a blank line)</li>

   <li>Fewer than N numbers (followed by a blank line)</li>

  </ol></li>

</ol>




<ol start="3">

 <li>The input contains only valid values (i.e. numbers of any kind):

  <ol>

   <li>More than N integers but fewer than N non-integers</li>

   <li>More than N non-integer numbers but fewer than N integers</li>

   <li>Exactly N integers and exactly N non-integers (followed by a blank line)</li>

   <li>Fewer than N integers and fewer than N non-integer numbers (followed by a blank line)</li>

  </ol></li>

</ol>




<ol start="4">

 <li>The input contains several invalid values:

  <ol>

   <li>First invalid value is preceded by more than N integers and fewer than N non-integers</li>

   <li>First invalid value is preceded by more than N non-integers and fewer than N integers</li>

   <li>First invalid value is preceded by exactly N integers and exactly N non-integers</li>

   <li>First invalid value is preceded by fewer than N integers and fewer than N non-integers</li>

  </ol></li>

</ol>




<ol start="5">

 <li>The input contains only invalid values</li>

</ol>




<ol start="6">

 <li>The input contains no values at all (blank line right away).</li>

</ol>


