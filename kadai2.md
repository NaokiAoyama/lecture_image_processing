#課題2 階調数と疑似輪郭

1.課題内容

2階調，4階調，8階調の画像を生成せよ．

2.方法と実行結果

標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による正方形の白黒濃淡画像である．
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('Lenna.png'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-1.png?raw=true)  

図1 原画像

階調画像を生成するには閾値256を階調数で割れば求めることができる．
2階調画像を生成するには閾値が1つ必要なので256/2=128を閾値にする．

IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  

2階調画像の結果を図２で表す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-2.png?raw=true)
  
図2 2階調画像

同様に4階調画像を生成するには閾値が3つ必要なので256/4=64，よって64×1=64,64×2=128,64×3=192を閾値にする．

これらの和をとることにより4階調画像を生成される．

IMG0 = ORG>64; 

IMG1 = ORG>128; 

IMG2 = ORG>192; 

IMG = IMG0 + IMG1 + IMG2; 

imagesc(IMG); colormap(gray); colorbar;  axis image; 

4階調画像の結果を図３で表す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-3.png?raw=true)
  
図3 4階調画像

同様に8階調画像を生成するには閾値が7つ必要なので256/8=64，よって32*1=32,32*2=64,32*3=96,32*4=128,32*5=160,32*6=192,32*7=224を閾値にする．
これらの和をとることにより8階調画像を生成される．

IMG0 = ORG>32;

IMG1 = ORG>64;

IMG2 = ORG>96;

IMG3 = ORG>128;

IMG4 = ORG>160;

IMG5 = ORG>192;

IMG6 = ORG>224;

IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;

imagesc(IMG); colormap(gray); colorbar; axis image;

8階調画像の結果を図４で表す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-4.png?raw=true)  

図4 8階調画像
