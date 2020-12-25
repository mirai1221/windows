<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="./css/style.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
  <script src=".\js/sample.js"></script>
  <title>Document</title>
</head>
<body>

<a id="slidetoggle_button" href="#">トグルボタン</a>

<ul id="slidetoggle_menu">
  <li>メニュー</li>
  <li>メニュー</li>
  <li>メニュー</li>
</ul>

</body>
</html>

$(function(){

  $("#slidetoggle_button").on("click", function() {
      $("#slidetoggle_menu").slideToggle();
      // $("#slidetoggle_menu").toggleClass("active");
  });

});


#slidetoggle_menu{

  display:none;

}
