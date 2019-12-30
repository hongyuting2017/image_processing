# 課題２　階調数と疑似輪郭  
ORG=imread('Lenna.png'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

によって原画像を読み込みグレースケール画像へ変換，表示した結果を図1に示す．
