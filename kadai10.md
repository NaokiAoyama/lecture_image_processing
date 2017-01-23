#課題10　画像のエッジ抽出

1.課題内容  
エッジ抽出を実行せよ．

2.方法と実行結果  
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による白黒濃淡画像である．  
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('Lenna.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-1.png?raw=true)  
図1 原画像

プレウィット法でエッジ抽出した画像を表示する．

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

プレウィット法でエッジ抽出した画像の結果を図２に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-2.png?raw=true)  
図2 プレウィット法でエッジ抽出した画像

ソルベ法でエッジ抽出した画像を表示する．

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

ソルベ法でエッジ抽出した画像の結果を図３に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-3.png?raw=true)  
図3 ソルベ法でエッジ抽出した画像

キャニー法でエッジ抽出した画像を表示する．

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

キャニー法でエッジ抽出した画像の結果を図４に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-4.png?raw=true)  
図4 キャニー法でエッジ抽出した画像