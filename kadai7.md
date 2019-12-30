# 課題７　ダイナミックレンジの拡大
ORG=imread('Lenna.png');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を白黒濃淡画像へ変換し，結果は図１に示す．　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai7-1.jpg)  
図1 白黒濃淡画像

imhist(ORG);  
によって，濃度ヒストグラムを表示し，結果を図2に示す．

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai7-1.jpg)  
図2 濃度ヒストグラム　　

ORG = double(ORG);　　
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  　
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
　
によって、画素のダイナミックレンジを0~255に拡大する．結果を図3に示す．  
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai7-3.jpg)  
図3 ダイナミックレンジを拡大した画像  

ORG = uint8(ORG); % 演算を行う際に倍精度値doubleに変換するため，ORGを8ビットの符号なし整数uint8に変換する
imhist(ORG); % 濃度ヒストグラムを生成、表示  

によって、ダイナミックレンジを拡大した画像の濃度ヒストグラム を表示する。結果を図4に示す．  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai7-4.jpg)  
図4 ダイナミックレンジを拡大した画像の濃度ヒストグラム 
