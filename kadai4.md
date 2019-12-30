# 課題４　画像のヒストグラム
ORG=imread('Lenna.png');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を白黒濃淡画像へ変換し，結果は図１に示す．　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai4-1.jpg)  
図1 白黒濃淡画像

imhist(ORG);  
により，ORGのヒストグラムを表示する．結果を図2に示す．　　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai4-2.jpg)  
図2 画像のヒストグラム
