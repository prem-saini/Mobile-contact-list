# Mobile-contact-list
<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width,initial-scale=1.0">
 <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>My contacts</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/0.99.0/css/materialize.min.css">
<style>
    body{
        margin-top: 70px;
        background: #444;
        color: #fff;
    }
    </style>
</head>
<body>
<div class="container">
    <h1 class="center-align">
        My Contacts
    </h1>
    <input type="text" id="filterInput" placeholder="Search names...">
    <ul id="names" class="collection with-header">
        <li class="collection-header">
            <h5>A</h5>
        </li>
       
        <li class="collection-item">
            <a href="#">Ajay</a>
        </li>
        <li class="collection-item">
            <a href="#">Anita</a>
        </li>
        <li class="collection-item">
            <a href="#">Arun</a>
        </li>
        <li class="collection-header">
            <h5>B</h5>
        </li>
       
        <li class="collection-item">
            <a href="#">Banty Saini</a>
        </li>
        <li class="collection-item">
            <a href="#">Babita</a>
        </li>
        <li class="collection-item">
            <a href="#">Bhai Bhai</a>
        </li>
        <li class="collection-header">
            <h5>C</h5>
        </li>
       
        <li class="collection-item">
            <a href="#">Chanu</a>
        </li>
        <li class="collection-item">
            <a href="#">Chandan</a>
        </li>
        <li class="collection-item">
            <a href="#">Charu</a>
        </li>
        <li class="collection-header">
            <h5>D</h5>
        </li>
       
        <li class="collection-item">
            <a href="#">Dada</a>
        </li>
        <li class="collection-item">
            <a href="#">Dinesh</a>
        </li>
        <li class="collection-item">
            <a href="#">Dinesh Saini</a>
        </li>
    </ul>
</div>
<script>
// input element
let filterInput = document.getElementById('filterInput');
// Add event listener
filterInput.addEventListener('Keyup', filterNames);

function filterNames(){
    //  get value of input
    let filterValue = document.getElementById('filterInput').value.toUpperCase();
    // Get names ul
    let ul = document.getElementById('names');
    // Get lis from ul
    let li = ul.querySelectorAll('li.collection-item');

    // Loop through collection-item lis 
    for(let i = 0;i < li.length;i++){
        let a = li[i].getElementsByTagName('a')[0];
         // if  matched 
         if(a.innerHTML.toUpperCase().indexOf(filterValue) > -1){
         
            li[i].style.display = '';
             
         } else {
            li[i].style.display = 'None';
      
        }
    }
}

</script>
</body>

</html>
