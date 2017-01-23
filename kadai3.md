#課題3　閾値処理

1.実験内容  
閾値を4パターン設定し,閾値処理た画像を示せ． 

2.方法と実験内容  
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による白黒濃淡画像である．
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('Lenna.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換 

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-1.png?raw=true)  
図1 原画像

原画像の閾値の輝度値を64に設定する．

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  

原画像の閾値の輝度値を64に設定した画像の結果を図２に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-2.png?raw=true)  
図2 原画像の閾値の輝度値を64に設定した画像

原画像の閾値の輝度値を96に設定する．

IMG = ORG > 96; % 輝度値が96以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  

原画像の閾値の輝度値を96に設定した画像の結果を図３に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-3.png?raw=true)   
図３ 原画像の閾値の輝度値を96に設定した画像

原画像の閾値の輝度値を128に設定する．

IMG = ORG > 128; % 輝度値が128以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  

原画像の閾値の輝度値を128に設定した画像の結果を図４に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-4.png?raw=true)  
図4 原画像の閾値の輝度値を128に設定した画像

原画像の閾値の輝度値を192に設定する．

IMG = ORG > 192; % 輝度値が192以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  

原画像の閾値の輝度値を192に設定した画像の結果を図５に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-5.png?raw=true)  
図5 原画像の閾値の輝度値を192に設定した画像