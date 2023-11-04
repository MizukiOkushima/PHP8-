### 練習4.1
#### 1.条件分岐構文を使って、90点以上であれば「優」、70点以上であれば「良」、50点以上であれば「可」、それ以下の場合は「不可」と表示するためのコードを作成してください。また点数が75点で合った場合の結果を表示されてみましょう。
```PHP
<?php
$point = 75;
if ($point >= 90) {
  print '良';
} elseif ($point >= 70) {
  print '良';
} elseif ($point >= 50){
  print '可';
} else {
  print '不可';
}
?>
```
#### 2.条件式「!X && !Y」を「!(X || Y)」に置き換えられることを、ベン図を使って証明してください。
<img width="774" alt="スクリーンショット 2023-11-04 18 56 53" src="https://github.com/MizukiOkushima/PHP8BeginnerExam/assets/95268598/a008bd04-2dbc-4942-9986-5d7a7d9ccf90">
