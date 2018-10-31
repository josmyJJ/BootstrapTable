# BootstrapTable
## Learning Objectives
* Using bootstrap table styles

## The Walkthrough

1. Create a Spring Boot Application
	* Name it BootsrapTable
	* Add the dependencies for the web and for thymeleaf
	* Hit next until you finish the wizard, and then wait until it's done.

2. Create a Controller
	* Right click on com.example.demo and click New -> Class
	* Name it HomeController.java
	* Edit it to look like this:
```java
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class HomeController {

    @RequestMapping("/")
    public String index(){
        return "index";
    }
}
```

3. Create a Template
  * Right click on templates and click New -> Html
	* Name it index.html
	* Edit it to look like this:
```html
<!DOCTYPE html>
<html lang="en" xmlns:th="www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <title>Bootstrap 101 template</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>
<body>
  <div class="container">
      <br>
      <h1>Tables</h1>
      <h2>Basic style</h2>
      <table class="table">
          <thead>
          <tr>
              <th scope="col">#</th>
              <th scope="col">First</th>
              <th scope="col">Last</th>
              <th scope="col">Handle</th>
          </tr>
          </thead>
          <tbody>
          <tr>
              <th scope="row">1</th>
              <td>Mark</td>
              <td>Otto</td>
              <td>@mdo</td>
          </tr>
          <tr>
              <th scope="row">2</th>
              <td>Jacob</td>
              <td>Thornton</td>
              <td>@fat</td>
          </tr>
          <tr>
              <th scope="row">3</th>
              <td>Larry</td>
              <td>the Bird</td>
              <td>@twitter</td>
          </tr>
          </tbody>
      </table>

      <h2>Dark Table</h2>
      <table class="table table-dark">
          <thead>
          <tr>
              <th scope="col">#</th>
              <th scope="col">First</th>
              <th scope="col">Last</th>
              <th scope="col">Handle</th>
          </tr>
          </thead>
          <tbody>
          <tr>
              <th scope="row">1</th>
              <td>Mark</td>
              <td>Otto</td>
              <td>@mdo</td>
          </tr>
          <tr>
              <th scope="row">2</th>
              <td>Jacob</td>
              <td>Thornton</td>
              <td>@fat</td>
          </tr>
          <tr>
              <th scope="row">3</th>
              <td>Larry</td>
              <td>the Bird</td>
              <td>@twitter</td>
          </tr>
          </tbody>
      </table>

      <h2>Table Head</h2>
      <table class="table table-dark">
          <thead class="thead-light">
          <tr>
              <th scope="col">#</th>
              <th scope="col">First</th>
              <th scope="col">Last</th>
              <th scope="col">Handle</th>
          </tr>
          </thead>
          <tbody>
          <tr>
              <th scope="row">1</th>
              <td>Mark</td>
              <td>Otto</td>
              <td>@mdo</td>
          </tr>
          <tr>
              <th scope="row">2</th>
              <td>Jacob</td>
              <td>Thornton</td>
              <td>@fat</td>
          </tr>
          <tr>
              <th scope="row">3</th>
              <td>Larry</td>
              <td>the Bird</td>
              <td>@twitter</td>
          </tr>
          </tbody>
      </table>

      <h2>Color Table Rows</h2>
      <table class="table">
          <thead>
          <tr class="table-secondary">
              <th scope="col">#</th>
              <th scope="col">First</th>
              <th scope="col">Last</th>
              <th scope="col">Handle</th>
          </tr>
          </thead>
          <tbody>
          <tr class="table-warning">
              <th scope="row">1</th>
              <td>Mark</td>
              <td>Otto</td>
              <td>@mdo</td>
          </tr>
          <tr class="table-primary">
              <th scope="row">2</th>
              <td>Jacob</td>
              <td>Thornton</td>
              <td>@fat</td>
          </tr>
          <tr class="table-success">
              <th scope="row">3</th>
              <td>Larry</td>
              <td>the Bird</td>
              <td>@twitter</td>
          </tr>
          </tbody>
      </table>
  </div>
</body>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
</html>
```

4. Run your application and open a browser, if you type in the URL http://localhost:8080

## What is Going On

### The Controller
Here, the default route maps to index.html.

### The View

#### table class
By adding the table class to the table tag it gives a nicely rendered and great looking table.

#### Table dark and table light
table-dark class provides light text and dark background. table-light class provides dark text and light background.

#### Head colors
thead-light will make the entire row have a light background and thead-dark will make the entire row have a dark background.

#### Color options
Type table- and then choose the color available (such as table-primary, table-success, etc...). This will change the background color of each row.
