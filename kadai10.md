#�ۑ�10�@�摜�̃G�b�W���o

1.�ۑ���e  
�G�b�W���o�����s����D

2.���@�Ǝ��s����  
�W���摜�uneko�v�����摜�Ƃ���D���̉摜�͏c500�摜�C��500��f�ɂ�锒���Z�W�摜�ł���D  
�{�ۑ�ł̓f�B�W�^���J���[�摜�𔒍��摜�ɕϊ����Ĉ����D

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-1.png?raw=true)  
�}1 ���摜

�v���E�B�b�g�@�ŃG�b�W���o�����摜��\������D

IMG = edge(ORG,'prewitt'); % �G�b�W���o�i�v���E�B�b�g�@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��  

�v���E�B�b�g�@�ŃG�b�W���o�����摜�̌��ʂ�}�Q�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-2.png?raw=true)  
�}2 �v���E�B�b�g�@�ŃG�b�W���o�����摜

�\���x�@�ŃG�b�W���o�����摜��\������D

IMG = edge(ORG,'sobel'); % �G�b�W���o�i�\�x���@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��  

�\���x�@�ŃG�b�W���o�����摜�̌��ʂ�}�R�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-3.png?raw=true)  
�}3 �\���x�@�ŃG�b�W���o�����摜

�L���j�[�@�ŃG�b�W���o�����摜��\������D

IMG = edge(ORG,'canny'); % �G�b�W���o�i�L���j�[�@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��  

�L���j�[�@�ŃG�b�W���o�����摜�̌��ʂ�}�S�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai10-4.png?raw=true)  
�}4 �L���j�[�@�ŃG�b�W���o�����摜