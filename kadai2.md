# 課題２　階調数と疑似輪郭  
ORG=imread('Lenna.png'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

によって，原画像を読み込みグレースケール画像へ変換した，結果を図1に示す．  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai2-1.jpg)  
図1 グレースケール画像

２階調は1bitで２段階である。　

IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  　

によって，２階調画像を生成する．結果は図２に示す．　　
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai2-2.jpg)  
図2 ２階調画像


