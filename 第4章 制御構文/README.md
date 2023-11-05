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

### 練習4.2
#### 1.while命令とdo〜while命令との違いを説明してください。
while命令は条件式を前置判定するのに対して、do〜while命令は後置判定します。<br>
その性質上、条件式が最小からfalseである場合、while命令はループを一度も処理しませんが、do〜while命令はいかなる場合も一度はループ処理を実行します。
#### 2.for命令を利用して、図4.Aのような九九表を作成してみましょう。
<img width="512" alt="スクリーンショット 2023-11-05 18 22 57" src="https://github.com/MizukiOkushima/PHP8BeginnerExam/assets/95268598/d349f402-f489-4772-90b1-60c432adff7b"><br>
```PHP
<?php
for ($i = 1; $i <= 9; $i++){
  for ($j = 1; $j <=9; $j++) {
    $result = $i * $j;
    print "{$result} &nbsp;";
  }
  print'<br />';
}
?>
```
このスクリプトのように、for命令はネストすることができます。<br>
その場合、ループ変数名はそれぞれで異なるものを使用しなければならない点に注意してください。<br>

### 練習4.3
#### 1.現在の周回をスキップする命令、現在のループを脱出する命令を、それぞれ答えてください。
スキップ：continue命令<br>
脱出：break命令<br>
continue、breakはいずれもfor、while、do〜whileなどの繰り返し構文の中で使用できる命令です。<br>
その性質上、continue、break命令はif命令などの条件分岐と組み合わせて利用するのが一般的です。<br>
#### 2.リスト4.32のコードをwhile命令で書き換えてみましょう。
```PHP
<?php
$sum = 0;
for ($i = 1; $i <= 100; $i++) {
  if ($i % 2 !== 0) { continue; }
  $sum += $i;
}
print "合計値は{$sum}です。";
```
```PHP
<?php
$sum = 0;
$i = 0;
while ($i <=100) {
  $i++;
  if ($i % 2 !== 0) { continue; }
  $sum += $i;
}
print "合計値は{$sum}です。";  // 結果：合計値は2550です。
?>
```
while命令では、カウンター変数$iをインクリメントするタイミングを謝ると無限ループになる可能性があります。<br>
