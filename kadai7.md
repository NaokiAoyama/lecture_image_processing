#�ۑ�7�@�_�C�i�~�b�N�����W�̊g�� 

1.�ۑ���e  
��f�̃_�C�i�~�b�N�����W���O����Q�T�T�ɂ���D

2.���@�Ǝ��s����  
�W���摜�uneko�v�����摜�Ƃ���D���̉摜�͏c500�摜�C��500��f�ɂ�锒���Z�W�摜�ł���D  
�{�ۑ�ł̓f�B�W�^���J���[�摜�𔒍��摜�ɕϊ����Ĉ����D

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-1.png?raw=true)  
�}1 ���摜

�摜�̃q�X�g�O������\������D

imhist(ORG); % �q�X�g�O�����̕\��  

�q�X�g�O�����̌��ʂ�}�Q�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-2.png?raw=true)  
�}2 �q�X�g�O����

�_�C�i�~�b�N�����W���g�傷��ɂ͔Z�x�l�̍ŏ�����эő�l���Z�o���ő�l����ŏ��l�����������̂Ŋ��������̂ɂ����255���|���邱�ƂŁA�_�C�i�~�b�N�����W���g�傳����D

ORG = double(ORG);  
mn = min(ORG(:)); % �Z�x�l�̍ŏ��l���Z�o  
mx = max(ORG(:)); % �Z�x�l�̍ő�l���Z�o  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�_�C�i�~�b�N�����W���g�傳�����摜�̌��ʂ�}�R�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-3.png?raw=true)  
�}3 �_�C�i�~�b�N�����W���g�傳�����摜

���Z���s���ۂɔ{���x�ldouble�ɕϊ��������̂��ŏI�I�ɕ����Ȃ�����uint8�ɕϊ����A�ۂ߂𔭐������邱�Ƃɂ��A�قړ��Ԋu�ɑS���������܂܂Ȃ��Z�x�l��������D

ORG = uint8(ORG); % ���̍s�ɂ��čl�@����  
imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��  

�q�X�g�O�����̌��ʂ�}�S�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai7-4.png?raw=true)  
�}4 �q�X�g�O����