<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
  <style>
    .hide-element {
  display: block;
}

.active {
  color: red;
}
  </style>
</head>
<body>
  
  <div>
    <a class="toggle-class" href="#">toggle element</a>
    <p class="hide-element">hode these element</p>
  </div>
  
  <div class="menu">
    <ul class="nav-menu">
      <li class="active">menu 1</li>
      <li>menu 2</li>
      <li>menu 3</li>
      <li>menu 4</li>
      <li>menu 5</li>
    </ul>
  </div>

</body>
<script src="https://code.jquery.com/jquery-3.1.0.js"></script>
<script>
  $(document).ready(function(){
      $('.toggle-class').on('click', function(e){
        $('.hide-element').toggle(250, function(){
        });
      });
      $('.nav-menu').on('click', 'LI', function(){
      	$('.nav-menu li.active').removeClass('active');
        $(this).addClass('active');
      });
 
  });
</script>
</html>
