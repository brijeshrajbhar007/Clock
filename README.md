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
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111;
}
</style>
</head>
<body>

<ul>
  <li><a class="active" href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>

      <div class="container my-4">
        <div class="jumbotron">
            <h1 class="display-4">Current Time Is: <span id='time'></span></h1>
            <p><b>Time might be visible to you</b></p>
            <hr class="my-4">
            <p><b>Thank you for watching</b></p>
            <a class="btn btn-primary btn-lg" href="#" role="button">Browse Times</a>
        </div>
      </div>
      <script>
        let a;
        let date;
        let time;
        const options = {weekday: 'long', year: 'numeric', month: 'long',day:'numeric'};
        setInterval(() => {
            a = new Date();
            date = a.toLocaleDateString(undefined,options);
            time = a.getHours() + ':' + a.getMinutes() + ':' + a.getSeconds();
            document.getElementById('time').innerHTML = time + " <br>ON " + date;
        }, 1000);
      </script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
  </body>
</html>
