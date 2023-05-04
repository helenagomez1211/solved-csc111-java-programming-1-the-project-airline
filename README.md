Download Link: https://assignmentchef.com/product/solved-csc111-java-programming-1-the-project-airline
<br>
<strong><u>Program Tasks Overview</u> </strong>

You need to write a program for Airline to manage domestic flights information. The program should enable the flights data manager to complete the following tasks:

<ul>

 <li><u>Add</u> a new flight to the flights list.</li>

 <li><u>Find </u>the information about a flight given its number.</li>

 <li><u>Print</u> all the flights.</li>

 <li><u>Print</u> all the flights having the same given date.</li>

 <li><u>Update </u>the departure and arrival time of specific flight.  <u>Print</u> the total number of flights.</li>

</ul>




<strong><u>Assumptions:</u> </strong>

<ul>

 <li><u>All flights will depart from Riyadh (King Khalid Airport).</u></li>

 <li>When adding a new flight, the<em> FlightNumber</em> must be generated automatically using a specific formula before adding the flights to the system.</li>

 <li><em>Date</em>, <em>DepartureTime</em> must be <u>checked</u> and <u>validated</u> before adding the flight.</li>

 <li>There is a counter for the number of flights, the <em>TotalFlights</em> will be incremented whenever a flight is added successfully.</li>

</ul>




For your project, you must implement and use two classes:

<ol>

 <li><strong> Class Flight: </strong></li>

</ol>

<strong> </strong>A Flight class is identified by:

<ul>

 <li>flightNumber: the flight number.</li>

 <li>destination: arriving city. There is a list of 7 cities to choose the destination, which are {dammam, jeddah, yanbu, hail, abha, tabuk, taif}  gate: the gate number for boarding the plane.</li>

 <li>date: the flight date in the format (dd/mm).</li>

 <li>departureTime: the departure time in the format (hh:mm) and 24-hours system.</li>

 <li>arrivalTime: the arrival time to the destination in the format (hh:mm) and 24-hours system.</li>

 <li><strong>totalFlights</strong>: the total number of flights in the system</li>

</ul>

The methods to be included in the Flight class are:

<strong>Flight()</strong>: A default constructor that initializes all instance variables of the class:

<ul>

 <li>Integer types are initialized to zero  Strings are initialized to null (“”)</li>

</ul>




<strong>    Flight (int destination, String date, int gate, String departure): </strong>Another constructor that initializes new flight with the initial values from the user for the following attributes : destination , gate, date and departure Time and call <strong>calculateArrivalTime</strong>() method to set the arrivalTime  .

<strong> </strong>

<strong>Setter Methods (one for each):</strong> That sets the values for (destination, date, gate, departure).




<strong>          Getter Methods (one for each): </strong>That returns the values of: (destination, date, gate, departure, arrival).

<strong>generateFlightNumber():</strong> Generates and stores a flight number in <em>FlightNumber</em>; The

<em>FlightNumber</em> is formed by the first three characters in the destination (in uppercase) followed by “00” and concatenated with the <em>TotalFlights</em> number.

<em>                    Example:</em> If the destination is <u>Dammam</u> and the current <em>TotalFlights</em> is 3 à <em>FlightNumber</em> =

DAM003

<strong>calculateArrivalTime</strong>(): Calculates the <em>ArrivalTime</em> depending on the <em>Destination </em>and the duration of the flight. The <em>ArrivalTime</em> should be in (HH:MM) format and 24-hours system. It should be checked if the arrival time will be in the next day, add (“+1”) beside the <em>ArrivalTime.</em>




<em> Example</em>: If the destination is Dammam and the<em> departureTime </em>is 02:15 à <em>ArrivalTime</em>=03:20  <em>                </em>If the destination is Jeddah and the<em> departureTime is 23:30 </em>à <em>ArrivalTime</em>=01:15+1




The duration of the time between Riyadh and each city:




<table width="291">

 <tbody>

  <tr>

   <td width="177">Dammam</td>

   <td width="113">65 minutes</td>

  </tr>

  <tr>

   <td width="177">Jeddah,Yanbu and Abha</td>

   <td width="113">105 minutes</td>

  </tr>

  <tr>

   <td width="177"> Hail</td>

   <td width="113">75 minutes</td>

  </tr>

  <tr>

   <td width="177">Tabuk</td>

   <td width="113">80 minutes</td>

  </tr>

  <tr>

   <td width="177">Taif</td>

   <td width="113">95 minutes</td>

  </tr>

 </tbody>

</table>
















<strong>printFlightInfo() :</strong> This method should print the information of a flight with 15 columns width

and should be left justified.




Flight Number:  <strong><em>flight number                   </em></strong>Gate:<strong><em> (gate) </em></strong>

Destination:<strong><em> city                                          </em></strong>Date: <strong><em>date          </em></strong>

Departure Time: <strong><em>departure</em></strong>                        Arrival Time:  <strong><em>arrival </em></strong>

<strong><em> </em></strong>

<ol start="2">

 <li><strong> Class Airline: </strong></li>

</ol>

This class represents the Airline application.  Class Airline contains a <u>list of 100 flights, FlightsList[].</u>

This is the class you use to test your program. The methods’ prototypes and behaviors are defined as follows (all public):

o <strong><u>main: </u></strong>The main method that includes a <u>menu</u> for the user asking him what he would like to do, as follows:

<ul>

 <li>Add a Flight</li>

 <li>Find a flight</li>

 <li>List all flights</li>

 <li>List flights for a given date</li>

 <li>Update Departure &amp; Arrival Time</li>

 <li>Total number of flights (7) Exit</li>

 <li><strong><u>Add flight:</u></strong> Creates a new flight and add it in the first available space of the array FlightsList[] , this method returns true if the add operation was completed successfully, and false otherwise. <u>The flight is</u> <u>successfully added if it’s date, departure and arrival time has the correct format, if the flight is not</u> <u>already in </u>FlightsList<u> []., and if number of flights doesn’t exceed 100</u></li>

</ul>




<ul>

 <li>Method name: addFlight</li>

 <li>Method type: Boolean</li>

 <li>Formal parameters: destination, date, gate, departure</li>

</ul>




<ul>

 <li><strong><u>Find flight:</u></strong> Returns the index of a given flight number if the flight is in the flights list, or -1 if the flight is not already in the flights list</li>

</ul>

o

<ul>

 <li>Method name: findFlight</li>

 <li>Method type: int</li>

 <li>Formal parameters: FlightNumber</li>

</ul>




<ul>

 <li><strong><u>List all flights :</u></strong> Prints all the flights’ information in the flights list. Nothing will be printed if there is no flight.

  <ul>

   <li>Method name: printAll</li>

   <li>Method type: void</li>

   <li>Formal parameters: non</li>

  </ul></li>

</ul>




<ul>

 <li><strong><u>List all flights for a given date:</u></strong> Prints all the flights’ information in the flights list that have the same date. Nothing will be printed if there is no flights in the same date.</li>

</ul>




<ul>

 <li>Method name: printAll</li>

 <li>Method type: void</li>

 <li>Formal parameters: date</li>

</ul>




<ul>

 <li><strong><u>Update departure &amp; arrival time:</u></strong> Updates the departure time of specific flights by using FlightNumber, then prints that flight information after updated.

  <ul>

   <li>Method name: updateTime</li>

   <li>Method type: void</li>

   <li>Formal parameters: FlightNumber, departure</li>

  </ul></li>

</ul>




<ul>

 <li><strong><u>Total number of flights:</u></strong> Returns the total number of flights in the flights list</li>

</ul>

<strong> </strong>

<ul>

 <li>Method name: getNumberOfFlights</li>

 <li>Method type: int</li>

 <li>Formal parameters: none</li>

</ul>







<strong><u>Requirements:</u>  </strong>

<ul>

 <li>You must define the classes Flight and Airline.</li>

 <li>Same as all programming assignments:</li>

 <li>Use meaningful variable name and good indentation.</li>

 <li>You must avoid code duplication, by calling appropriate methods (rather than cutting and pasting code).</li>

 <li><u>Don’t change</u> the names of any class, attribute or method.</li>

 <li>Submit your project even if you are not able to complete all the functions, however, for the methods of Flight class that you couldn’t implement provide a shell (empty body, just a header) for the method. This will allow us to compile your program and test the components you have implemented.</li>

</ul>













<strong><u>The project has two phases :</u></strong>

<strong> </strong>

<strong><u>Phase 1:</u></strong> (Upload UML on LMS before <strong>Friday 23/11/2018 -11:59 p.m.)</strong>

Deign the UML for the classes (<strong>flight and Airline</strong>). Please make it <u>nice and neat.</u>

Note: you can use <em><u>www.gliffy.com</u></em>to draw the UML

ON Saturday 24/11/2018 the correct UML will be available on LMS and you will use it to implement your classes (you will implement the correct one).

You will need to finish mapping the UML to the correct code (class, attributes and method headers).

<strong><u>Phase 2:</u> </strong>

1) Complete the implementation of all methods bodies. 2) Test your code using the following test cases.

<table width="625">

 <tbody>

  <tr>

   <td width="208">Flight 1</td>

   <td width="217">Flight 2</td>

   <td width="199">Flight 3</td>

  </tr>

  <tr>

   <td width="208">Destination: DammamDate: 25/11Gate:12Departure Time: 03:15<strong> </strong></td>

   <td width="217">Destination: AbhaDate: 04/12Gate:3Departure Time: 23:00</td>

   <td width="199">Destination: DammamDate: 15/12Gate:1Departure Time: 16:45</td>

  </tr>

 </tbody>

</table>

<strong> </strong>