
課題5　判別分析法

1.課題内容
判別分析法を用いて画像二値化せよ．

2.方法と実行結果
標準画像「neko」を原画像とする．この画像は縦500画像，横500画素による白黒濃淡画像である．
本課題ではディジタルカラー画像を白黒画像に変換して扱う．

ORG=imread('Lenna.png'); % 原画像の入力 
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換 

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai5-1.png?raw=true)  
図1 原画像

判別式は以下の式で表せる．  
　 ①全画素の濃度の平均値をμ_rとする。  
 　②濃度tで分けたときのクラスiの分散を?σ^2?_i , 平均値をμ_i , 画素数をn_i とする。  
 　③クラス内分散　?σ^2?_w=(n_1 ?σ^2?_1+n_2 ?σ^2?_2)/(n_1+n_2) を求める。  
 　④クラス間分散　?σ^2?_B={n_1 (μ_1-μ_r )^2+n_2 (μ_2-μ_r )^2}/(n_1+n_2) を求める。  
 　⑤?σ^2?_B/?σ^2?_wを最大とするようにtを定める。  

これをプログラムにすると以下のである．  

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納  
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;  
 
 
IMG = ORG > max_thres;  
imagesc(IMG); colormap(gray); colorbar;  

判別式を用いた二値化の画像の結果を図２に示す．

![原画像](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai5-2.png?raw=true)  
図2 判別式を用いた二値化の画像