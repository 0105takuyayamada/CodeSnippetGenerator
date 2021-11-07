<!DOCTYPE html>
<head>
<meta charset="utf-8">
<title>CodeSnippetGenerator</title>
<link rel="stylesheet" href="style.css">
  
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script type="text/javascript" src="main.js">
// 追加
$('#liternal-plus').on('click', function(){
  var inputCount = $('#demo-area .unit').length;
  if (inputCount < maxCount){
    var element = $('#liternal-area .unit:last-child').clone(true);// 末尾をイベントごと複製
    // 複製したinputのクリア
    var inputList = element[0].querySelectorAll('input[type="text"], textarea');
    for (var i = 0; i < inputList.length; i++) {
      inputList[i].value = "";
    }
    $('#liternal-area .unit').parent().append(element);// 末尾追加
  }
});
// 削除
$('.liternal-minus').on('click', function(){// イベントごと複製しているのでonのselectorは未設定
  var inputCount = $('#liternal-area .unit').length;
  if (inputCount > minCount){
    $(this).closest('.unit').remove();
  }
});
</script>
</head>
<body>
<header>

## Basic Infomation

<table>
  <tr>
    <th>Title</th>
    <th><input type="text" id="title" name="title"></td>
  </tr>
  <tr>
    <td>Shortcut</td>
    <td><input type="text" id="shortcut" name="shortcut"></td>
  </tr>
  <tr>
  <td>Author</td>
  <td><input type="text" id="author" name="author"></td>
  </tr>
</table>

## Code
<textarea id="code" name="code"></textarea>

## Liternals

<div id="input_pluralBox">
    <div id="input_plural">
        <input type="text" class="form-control" placeholder="サンプルテキストサンプルテキストサンプルテキスト">
        <input type="button" value="＋" class="add pluralBtn">
        <input type="button" value="－" class="del pluralBtn">
    </div>
</div>

## Imports
<textarea id="imports" name="imports"></textarea>

</body>
</html>
