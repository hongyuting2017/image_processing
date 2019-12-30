課題８　ラベリング
ORG=imread('Lenna.png');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を白黒濃淡画像へ変換し，結果は図１に示す．　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai8-1.jpg)  
図1 白黒濃淡画像  

IMG = ORG > 128; % 閾値128で二値化   
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，画像二値化した結果を図２に示す．  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai8-2.jpg)  
図2  閾値128で二値化した画像 

また，二値化した画像をラベリングして表示した結果を図3に示す．  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai8-3.jpg)  
図3  二値化した画像のラベリング 
