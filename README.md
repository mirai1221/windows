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
<section>
 <div class="container">

   <a id="slide_toggle_button" href="#">トグルボタン</a>

   <ul id="slide_toggle_menu">
     <li>メニュー</li>
     <li>メニュー</li>
     <li>メニュー</li>
   </ul>

   <div class="effect-fade">
     <button id="button_scroll">ボタン</button>
   </div>
 </div>
</section>

</body>
</html>

$(function(){

  $("#slide_toggle_button").on("click", function() {
      $("#slide_toggle_menu").slideToggle();
       $("#slide_toggle_menu").toggleClass();
  });

});

$(function () {
  $(".effect-fade").hide()
  $(window).scroll(function () {
    $(".effect-fade").each(function () {
      var scroll = $(window).scrollTop(); /* スクロール位置を取得 */
      if (scroll > 80) {
        $(this).fadeIn();
      } else {
        $(this).fadeOut();
      }
    });
    $(this).on("click",function(){
      $('body,html').animate({
        scrollTop: 0
    }, 500);
    return false;
    })
  });
  jQuery(window).scroll();
});



.container{
  height: 2000px;
}

#slide_toggle_menu{
  display:none;
}

.effect-fade {
  padding-top: 500px;
}
