# 課題１　

標本化間隔と空間解像度画像をダウンサンプリングして（標本化間隔を大きくして）表示せよ．

ORG=imread('Lenna.png'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai1-1.jpg)  
図1 原画像

画像を1/2倍に縮小した後，2倍に拡大するによって，原画像を1/2サンプリングする．なお，拡大する際には，単純補間するために「box」オプションを設定する．

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

1/2サンプリングの結果を図２に示す．

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai1-2.jpg)  
図2 1/2サンプリング

原画像を1/4サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大する。

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,4,'box'); % 画像の拡大

1/4サンプリングの結果を図３に示す．
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai1-3.jpg)  
図3 1/4サンプリング

原画像を1/8サンプリングするには，画像を1/2倍に縮小した後，4倍に拡大する。  

原画像を1/16サンプリングするには，画像を1/2倍に縮小した後，8倍に拡大する。

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,8,'box'); % 画像の拡大  

1/8サンプリングの結果を図5に示す．

![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai1-4.jpg)  
図5 1/16サンプリング

原画像を1/32サンプリングするには，画像を1/2倍に縮小した後，16倍に拡大する。

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,16,'box'); % 画像の拡大  

1/32サンプリングの結果を図6に示す．
![原画像](https://github.com/hongyuting2017/image_processing/blob/master/image/kadai1-4.jpg)  
図5 1/16サンプリング



