#�ۑ�3�@臒l����

1.�������e  
臒l��4�p�^�[���ݒ肵,臒l�������摜�������D 

2.���@�Ǝ������e  
�W���摜�uneko�v�����摜�Ƃ���D���̉摜�͏c500�摜�C��500��f�ɂ�锒���Z�W�摜�ł���D
�{�ۑ�ł̓f�B�W�^���J���[�摜�𔒍��摜�ɕϊ����Ĉ����D

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ� 

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-1.png?raw=true)  
�}1 ���摜

���摜��臒l�̋P�x�l��64�ɐݒ肷��D

IMG = ORG > 64; % �P�x�l��64�ȏ�̉�f��1�C���̑���0�ɕϊ�  
imagesc(IMG); colormap(gray); colorbar;  

���摜��臒l�̋P�x�l��64�ɐݒ肵���摜�̌��ʂ�}�Q�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-2.png?raw=true)  
�}2 ���摜��臒l�̋P�x�l��64�ɐݒ肵���摜

���摜��臒l�̋P�x�l��96�ɐݒ肷��D

IMG = ORG > 96; % �P�x�l��96�ȏ�̉�f��1�C���̑���0�ɕϊ�  
imagesc(IMG); colormap(gray); colorbar;  

���摜��臒l�̋P�x�l��96�ɐݒ肵���摜�̌��ʂ�}�R�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-3.png?raw=true)   
�}�R ���摜��臒l�̋P�x�l��96�ɐݒ肵���摜

���摜��臒l�̋P�x�l��128�ɐݒ肷��D

IMG = ORG > 128; % �P�x�l��128�ȏ�̉�f��1�C���̑���0�ɕϊ�  
imagesc(IMG); colormap(gray); colorbar;  

���摜��臒l�̋P�x�l��128�ɐݒ肵���摜�̌��ʂ�}�S�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-4.png?raw=true)  
�}4 ���摜��臒l�̋P�x�l��128�ɐݒ肵���摜

���摜��臒l�̋P�x�l��192�ɐݒ肷��D

IMG = ORG > 192; % �P�x�l��192�ȏ�̉�f��1�C���̑���0�ɕϊ�  
imagesc(IMG); colormap(gray); colorbar;  

���摜��臒l�̋P�x�l��192�ɐݒ肵���摜�̌��ʂ�}�T�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai3-5.png?raw=true)  
�}5 ���摜��臒l�̋P�x�l��192�ɐݒ肵���摜