#課題9　メディアンフィルタと先鋭化

1.課題内容  
メディアンフィルターを適用し，ノイズ除去を体験せよ． 

2.方法と実行結果  
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による白黒濃淡画像である．  
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('Lenna.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-1.png?raw=true)  
図1 原画像

画像にノイズを添付する。

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

ノイズを添付したの画像の結果を図２に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-2.png?raw=true)   
図2 ノイズを添付した画像

平滑化フィルタで雑音除去する．

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

平滑化フィルタで雑音除去の画像の結果を図３に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-3.png?raw=true)  
図3 平滑化フィルタでの雑音除去の画像

メディアンフィルタで雑音除去する．

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

メディアンフィルタで雑音除去の画像の結果を図４に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-4.png?raw=true)  
図4 メディアンフィルタでの雑音除去の画像

フィルタの設計を行う．

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

フィルタ設計を行った画像の結果を図５に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-5.png?raw=true)  
図5 フィルタ設計を行った画像
