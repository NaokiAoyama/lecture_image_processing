#課題8　ラベリング

1.課題内容  
二値化された画像の連結成分にラベルをつけよ．

2.方法と課題内容  
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による白黒濃淡画像である．  
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('Lenna.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai8-1.png?raw=true)   
図1 原画像

原画像を二値化するには閾値の輝度値を128に設定する．

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

原画像を二値化した画像の結果を図２に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai8-2.png?raw=true)  
図2 原画像を二値化した画像

ラベリングをした画像を表示する．

IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示 

ラベリングした画像の結果を図３に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai8-3.png?raw=true)  
図3 原画像を二値化した画像
