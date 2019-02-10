# riot-image-slider

画像のスライダーを簡単に作成できる、Riot.jsのカスタムタグです。  
Riot.js以外は入れる必要はなく、画像をカスタムタグで挟むだけで利用できます。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <!-- riot.jsの導入 -->
  <script src="https://cdn.jsdelivr.net/npm/riot@3.13.2/riot+compiler.min.js"></script>
  <!-- カスタムタグの導入 -->
  <script type="riot/tag" src="image-slider.tag.html"></script>
</head>
<body>
  <image-slider>
    <img>
    <img>
  </image-slider>
  <!-- カスタムタグのマウント -->
  <script>riot.mount('image-slider')</script>
</body>
</html>
```

# 機能
- Chrome, Edge, IE11の動作
- 画像表示までのローディング機能
- 親タグの大きさに合わせる機能
- 画像の大きさによる、Padding調整機能
- 矢印によるスライダー機能
- 矢印の非表示機能
- インジケータ機能
- インジケータの非表示機能
- オートスライド機能
- オートスライドをOFFにする機能
- オートスライドの秒数設定機能
- スライドの速度調整機能
- スライドを止める機能
- スライドを止めるボタンの非表示機能
- 背景色の変更機能
- カスタムタグ内で複数使用可能
- Riot.js以外のライブラリ不必要

# 設定
マウント時のオプションで設定する方法
```js
riot.mount('image-slider', {
  arrow: false, //矢印非表示
  sliderIndicator: false //インジケータ非表示
  autoSlider: false //自動的にスライドしないように設定
  sliderIntervalTime: 5000 //5秒後にスライドするように設定
  slideSpeed: 30 //スライドの速度を変更
  stopButton: false //ストップボタンを非表示
  background: #dbdbdb //背景色を変更
})
```

カスタムタグにデータを記載する方法
```js
<image-slider arrow='false'></image-slider>
```
