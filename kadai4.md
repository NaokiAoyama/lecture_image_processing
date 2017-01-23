#課題4　画像のヒストグラム

1.課題内容  
画素の濃度ヒストグラムを生成せよ．

2.方法と実行結果  
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による白黒濃淡画像である．
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('neko.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai4-1.png?raw=true)  
図1 原画像

画像のヒストグラムを表示する．

imhist(ORG); % ヒストグラムの表示  

ヒストグラムの結果を図２に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai4-2.png?raw=true)  
図2 ヒストグラム
