# 課題６　画像の二値化　　
ORG=imread('603.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を白黒濃淡画像へ変換し，結果は図１に示す．　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai6-1.jpg)  
図1 白黒濃淡画像

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，128以上を１，それ以下を０として，128による二値化した画像を図２に示す．  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai6-2.jpg)  
図2 128による二値化した画像

IMG = dither(ORG); % ディザ法による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

によって，ディザ法による二値化した画像を図３に示す．

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai6-2.jpg)  
図3 ディザ法による二値化した画像　　

図２と図3により，128による２値化とディザ法による二値化の結果は異なっていることを確認できた．
