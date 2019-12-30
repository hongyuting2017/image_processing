# 課題２　階調数と疑似輪郭  
ORG=imread('Lenna.png'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

によって，原画像を読み込みグレースケール画像へ変換した，結果を図1に示す．  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai2-1.jpg)  
図1 グレースケール画像

２階調は1bitで2段階である．　

IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  　

によって，２階調画像を生成する．結果は図２に示す．　　
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai2-2.jpg)  
図2 ２階調画像

4階調は2bitで2段階である．　

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;   
IMG = IMG0 + IMG1 + IMG2;   
imagesc(IMG); colormap(gray); colorbar;  axis image  

によって，4階調画像を生成する．結果は図3に示す．　　
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai2-3.jpg)  
図3 4階調画像

8階調は3bitで2段階である．　

IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>120;  
IMG3 = ORG>168;  
IMG4 = ORG>192;  
IMG5 = ORG>224;  
IMG6 = ORG>256;  
IMG = IMG0 + IMG1 + IMG2 +IMG3 + IMG4 + IMG5 +IMG6;  
imagesc(IMG); colormap(gray); colorbar;  axis image;   　

によって，8階調画像を生成する．結果は図4に示す．　　
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai2-4.jpg)  
図4 8階調画像  
