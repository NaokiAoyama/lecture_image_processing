#�ۑ�2 �K�����Ƌ^���֊s

1.�ۑ���e

2�K���C4�K���C8�K���̉摜�𐶐�����D

2.���@�Ǝ��s����

�W���摜�uneko�v�����摜�Ƃ���D���̉摜�͏c500�摜�C��500��f�ɂ�鐳���`�̔����Z�W�摜�ł���D
�{�ۑ�ł̓f�B�W�^���J���[�摜�𔒍��摜�ɕϊ����Ĉ����D

ORG=imread('Lenna.png'); % ���摜�̓��� 
ORG = rgb2gray(ORG); colormap(gray); colorbar; 
imagesc(ORG); axis image; % �摜�̕\�� 

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-1.png?raw=true)  

�}1 ���摜

�K���摜�𐶐�����ɂ�臒l256���K�����Ŋ���΋��߂邱�Ƃ��ł���D
2�K���摜�𐶐�����ɂ�臒l��1�K�v�Ȃ̂�256/2=128��臒l�ɂ���D

IMG = ORG>128; 
imagesc(IMG); colormap(gray); colorbar;  axis image; 

2�K���摜�̌��ʂ�}�Q�ŕ\���D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-2.png?raw=true)
  
�}2 2�K���摜

���l��4�K���摜�𐶐�����ɂ�臒l��3�K�v�Ȃ̂�256/4=64�C�����64*1=64,64*2=128,64*3=192��臒l�ɂ���D
�����̘a���Ƃ邱�Ƃɂ��4�K���摜�𐶐������D

IMG0 = ORG>64; 
IMG1 = ORG>128; 
IMG2 = ORG>192; 
IMG = IMG0 + IMG1 + IMG2; 
imagesc(IMG); colormap(gray); colorbar;  axis image; 

4�K���摜�̌��ʂ�}�R�ŕ\���D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-3.png?raw=true)
  
�}3 4�K���摜

���l��8�K���摜�𐶐�����ɂ�臒l��7�K�v�Ȃ̂�256/8=64�C�����32*1=32,32*2=64,32*3=96,32*4=128,32*5=160,32*6=192,32*7=224��臒l�ɂ���D
�����̘a���Ƃ邱�Ƃɂ��8�K���摜�𐶐������D

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
imagesc(IMG); colormap(gray); colorbar; axis image;

8�K���摜�̌��ʂ�}�S�ŕ\���D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai2-4.png?raw=true)  

�}4 8�K���摜
