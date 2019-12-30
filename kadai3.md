# 課題３　閾値処理
ORG=imread('Lenna.png');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を白黒濃淡画像へ変換し，結果は図１に示す．
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai3-1.jpg)  
図1 白黒濃淡画像

輝度値が64以上の画素を1，その他を0に変換し，結果は図２に示す．  
IMG = ORG > 64; 
imagesc(IMG); colormap(gray); colorbar;　　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai3-2.jpg)  
図2 輝度値が64以上の画素の取り出し  

輝度値が96以上の画素を1，その他を0に変換し，結果は図3に示す．  
IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai3-3.jpg)  
図3 輝度値が96以上の画素の取り出し   

輝度値が128以上の画素を1，その他を0に変換し，結果は図4に示す．  
IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai3-4.jpg)  
図4 輝度値が128以上の画素の取り出し   

輝度値が192以上の画素を1，その他を0に変換し，結果は図4に示す．  
IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai3-5.jpg)  
図5 輝度値が192以上の画素の取り出し   


 

