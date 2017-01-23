#課題7　ダイナミックレンジの拡大 

1.課題内容  
画素のダイナミックレンジを０から２５５にせよ．

2.方法と実行結果  
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による白黒濃淡画像である．  
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('Lenna.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-1.png?raw=true)  
図1 原画像

画像のヒストグラムを表示する．

imhist(ORG); % ヒストグラムの表示  

ヒストグラムの結果を図２に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-2.png?raw=true)  
図2 ヒストグラム

ダイナミックレンジを拡大するには濃度値の最小および最大値を算出し最大値から最小値を引いたもので割ったものにさらに255を掛けることで、ダイナミックレンジを拡大させる．

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

ダイナミックレンジを拡大させた画像の結果を図３に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-3.png?raw=true)  
図3 ダイナミックレンジを拡大させた画像

演算を行う際に倍精度値doubleに変換したものを最終的に符号なし整数uint8に変換し、丸めを発生させることにより、ほぼ等間隔に全く成分を含まない濃度値が見られる．

ORG = uint8(ORG); % この行について考察せよ  
imhist(ORG); % 濃度ヒストグラムを生成、表示  

ヒストグラムの結果を図４に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-4.png?raw=true)  
図4 ヒストグラム