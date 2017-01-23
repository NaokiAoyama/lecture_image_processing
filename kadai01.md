課題1 標本化間隔と空間解像度

1.課題内容
課題内容画像をダウンサンプリングして表示せよ．

2.方法と実行結果
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による正方形のディジタルカラー画像である．

ORG=imread('neko.png'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/neko.png?raw=true) 

図1 原画像



