
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <title>P5.js 練習問題解答</title>
    <script src="https://cdn.jsdelivr.net/npm/p5@2.0.3/lib/p5.min.js">
    </script>
  </head>
  <body>
    <h1>P5.js 練習問題解答</h1>
    <script>
    function setup() {
        createCanvas(320, 180);
      }
   function draw() {
        stroke("black");
        strokeWeight(0.1);
      let numRects = 18;
let startH = 0;
let endH = 340;
let L = 0.75; // 例としてLを75%に設定
let C = 0.50; // 例としてCを50%に設定

for (let i = 0; i < numRects; i++) {
let h = map(i, 0, numRects - 1, startH, endH);
fill(h, L, C);

// 長方形のサイズを計算（徐々に小さくなる）
let rectWidth = map(i, 0, numRects - 1, width, width / numRects);
let rectHeight = map(i, 0, numRects - 1, height, height / numRects);

// 長方形の位置を計算（右下へ移動）
let x = map(i, 0, numRects - 1, 0, width - rectWidth);
let y = map(i, 0, numRects - 1, 0, height - rectHeight);

rect(x, y, rectWidth, rectHeight);
}
}
</script>
</body>
</html>



