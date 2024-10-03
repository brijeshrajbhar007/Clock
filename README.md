# Clock

HTML Structure:
Navigation Bar (ul, li, a):
The webpage has a navigation bar with links for Home, News, Contact, and About sections.
These are styled using CSS to float the links horizontally and change the background color when hovered.
Clock and Time Display:
JavaScript Section:
The script dynamically updates the current time and date on the webpage every second (setInterval is set to 1000 milliseconds).
It fetches the current time using the Date() object and formats it as hours, minutes, and seconds.
The current date is displayed using the toLocaleDateString() method, with options to show the weekday, year, month, and day.
This information is inserted into the <span id='time'> element in the HTML.
Styling:
CSS Styling:
Basic styling for the navigation bar is included to hide list-style bullets, center-align the text, and add hover effects.
A dark background color (#333) is applied to the navbar, and the text changes to a lighter shade when hovered over (#111).
Bootstrap:
Jumbotron and Button:
The page includes a Bootstrap jumbotron component with a heading that shows the dynamic time and date.
There's also a button labeled "Browse Times," styled using Bootstrap's default button classes.
Overall, this is a basic page that uses a combination of HTML, CSS, JavaScript, and Bootstrap to create a simple time display application.
