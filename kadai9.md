#�ۑ�9�@���f�B�A���t�B���^�Ɛ�s��

1.�ۑ���e  
���f�B�A���t�B���^�[��K�p���C�m�C�Y������̌�����D 

2.���@�Ǝ��s����  
�W���摜�uneko�v�����摜�Ƃ���D���̉摜�͏c500�摜�C��500��f�ɂ�锒���Z�W�摜�ł���D  
�{�ۑ�ł̓f�B�W�^���J���[�摜�𔒍��摜�ɕϊ����Ĉ����D

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-1.png?raw=true)  
�}1 ���摜

�摜�Ƀm�C�Y��Y�t����B

ORG = imnoise(ORG,'salt & pepper',0.02); % �m�C�Y�Y�t  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�m�C�Y��Y�t�����̉摜�̌��ʂ�}�Q�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-2.png?raw=true)   
�}2 �m�C�Y��Y�t�����摜

�������t�B���^�ŎG����������D

IMG = filter2(fspecial('average',3),ORG); % �������t�B���^�ŎG������  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

�������t�B���^�ŎG�������̉摜�̌��ʂ�}�R�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-3.png?raw=true)  
�}3 �������t�B���^�ł̎G�������̉摜

���f�B�A���t�B���^�ŎG����������D

IMG = medfilt2(ORG,[3 3]); % ���f�B�A���t�B���^�ŎG������  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

���f�B�A���t�B���^�ŎG�������̉摜�̌��ʂ�}�S�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-4.png?raw=true)  
�}4 ���f�B�A���t�B���^�ł̎G�������̉摜

�t�B���^�̐݌v���s���D

f=[0,-1,0;-1,5,-1;0,-1,0]; % �t�B���^�̐݌v  
IMG = filter2(f,IMG,'same'); % �t�B���^�̓K�p  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

�t�B���^�݌v���s�����摜�̌��ʂ�}�T�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai9-5.png?raw=true)  
�}5 �t�B���^�݌v���s�����摜
