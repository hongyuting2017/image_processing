# 課題９　メディアンフィルタと先鋭化
ORG=imread('603.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を白黒濃淡画像へ変換し，結果は図１に示す．　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai9-1.jpg)  
図1 白黒濃淡画像  

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，ノイズを添付し，結果を図２に示す．

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai9-2.jpg)  
図1 ノイズ添付した画像  


IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，ノイズを平滑化フィルタで除去し，結果を図３に示す．  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai9-3.jpg)  
図3 平滑化フィルタで雑音除去した画像  


また，メディアンフィルタで雑音除去し、結果を図4に示す．  

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示 

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai9-4.jpg)  
図4 メディアンフィルタで雑音除去した画像  

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，フィルタを設計して雑音を除去し、結果を図5に示す．
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai9-5.jpg)  
図4 フィルタを設計して雑音を除去した画像  
