Download Link: https://assignmentchef.com/product/solved-cs205-assignment-1-basic-input-output
<br>
You are asked to write a simple program that, as you will see, may not be as simple to write in C as it looks if you want to write robust programs. It will allow you to learn about basic input/output.

This program must prompt the user for the name of a first city, then its latitude and longitude, then for the name of a second city with its latitude and longitude, then compute the flying distance between the two and display. For example,

The first city: Shenzhen

The latitude and longitude of first city: 22.55 114.1

The second city: Beijing

The latitude and longitude of second city: 39.9139 116.3917

The distance between Shenzhen and Beijing is <em>&lt;result&gt; </em>km

“Thefirstcity:”, “Thelatitudeandlongitudeofsecondcity”,Thesecondcity:” and “The latitudeandlongitudeofsecondcity:” are prompt information.

Your program should print prompt information to tell user enter the information of city.

User will enter city name first (in the first line). Then user enters two floating numbers : latitude and longitude of city(in the second line)<strong>.If user’s input format is not correct. Your program should not crash and tell user the format is incorrect and exit. </strong>&lt;result&gt; is the distance calculated by your program.

Here is the formula for computing the distance (adapted from mathforum.org, provided by Doctor Rob):

Assume the Earth is a perfect sphere. Let all angles be measured in signed degrees (negative latitude means South; negative longitude means West).

<strong>phi = 90 – latitude</strong>

The North Pole has phi = 0, the South Pole has phi = 180, and 0 &lt;= phi &lt;= 180.

<strong>theta = longitude</strong>

Greenwich, England, has theta = 0, and -180 &lt;= theta &lt;= 180.

Let the angles for the two points be (phi1, theta1) and (phi2, theta2). Then compute <strong>c = sin(phi1) * sin(phi2) * cos(theta1-theta2) +cos(phi1) * cos(phi2)</strong>

<strong>Note: phi and theta should be in radians.</strong>

Then the shortest great circle distance between the two points is

<strong>d = R*arccos(c)</strong>

where R is the radius of the earth in kilometers, and the arccosine is taken between 0 and 180 degrees, inclusive. Earth radius: 6,371 km

<strong>Some cities for testing:</strong>

<table width="553">

 <tbody>

  <tr>

   <td width="184"><strong>city</strong></td>

   <td width="184"><strong>latitude</strong></td>

   <td width="185"><strong>longitude</strong></td>

  </tr>

  <tr>

   <td width="184">Shenzhen</td>

   <td width="184">22.55</td>

   <td width="185">114.1</td>

  </tr>

  <tr>

   <td width="184">Beijing</td>

   <td width="184">39.9139</td>

   <td width="185">116.3917</td>

  </tr>

  <tr>

   <td width="184">New York, USA</td>

   <td width="184">40.7127</td>

   <td width="185">-74.0059</td>

  </tr>

  <tr>

   <td width="184">San Francisco, USA</td>

   <td width="184">37.7833</td>

   <td width="185">-122.4167</td>

  </tr>

  <tr>

   <td width="184">London, UK</td>

   <td width="184">51.5072</td>

   <td width="185">-0.1275</td>

  </tr>

  <tr>

   <td width="184">Paris, France</td>

   <td width="184">48.8567</td>

   <td width="185">2.3508</td>

  </tr>

  <tr>

   <td width="184">Kolkata, India</td>

   <td width="184">22.567</td>

   <td width="185">88.367</td>

  </tr>

  <tr>

   <td width="184">Moscow, Russia</td>

   <td width="184">55.7500</td>

   <td width="185">37.6167</td>

  </tr>

  <tr>

   <td width="184">Rio de Janeiro, Brazil</td>

   <td width="184">-22.9083</td>

   <td width="185">-43.1964</td>

  </tr>

  <tr>

   <td width="184">Sydney, Australia</td>

   <td width="184">-33.865</td>

   <td width="185">151.209444</td>

  </tr>

 </tbody>

</table>

For checking out if your results are roughly correct: http://www.webflyer.com/travel/mileage_calculator/

<strong>Note: you must input the city name in English, and the city name should not appear unreasonable symbols, such as @, ￥, %, etc</strong>