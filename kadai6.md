#�ۑ�6�@�摜�̓�l��

1.�ۑ���e  
�摜���l������D

2.���@�Ǝ��s����  
�W���摜�uneko�v�����摜�Ƃ���D���̉摜�͏c500�摜�C��500��f�ɂ�锒���Z�W�摜�ł���.  
�{�ۑ�ł̓f�B�W�^���J���[�摜�𔒍��摜�ɕϊ����Ĉ����D

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai6-1.png?raw=true)  
�}1 ���摜

���摜���l������ɂ�臒l�̋P�x�l��128�ɐݒ肷��D

IMG = ORG>128; % 128�ɂ���l��  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

���摜���l�������摜�̌��ʂ�}�Q�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai6-2.png?raw=true)  
�}2 ���摜���l�������摜

���摜���f�B�U�@�œ�l������D

imhist(ORG); % �q�X�g�O�����̕\��  

�f�B�U�@�ɂ���l���̉摜�̌��ʂ�}�R�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai6-2.png?raw=true)  
�}3 �f�B�U�@�ɂ���l���̉摜
