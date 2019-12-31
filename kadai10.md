# 課題１０　画像のエッジ抽出 
ORG=imread('603.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を白黒濃淡画像へ変換し，結果は図１に示す．　

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai10-1.jpg)  
図1 白黒濃淡画像  

プレウィット法によるエッジ抽出の結果は図２に示す．

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai10-2.jpg)  
図2 プレウィット法によるエッジ抽出

ソベル法キャニー法によるエッジ抽出の結果は図3に示す．

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai10-3.jpg)  
図３ ソベル法によるエッジ抽出

キャニー法によるエッジ抽出の結果は図4に示す．

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai10-4.jpg)  
図4 キャニー法によるエッジ抽出



