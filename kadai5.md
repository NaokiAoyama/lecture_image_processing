
�ۑ�5�@���ʕ��͖@

1.�ۑ���e
���ʕ��͖@��p���ĉ摜��l������D

2.���@�Ǝ��s����
�W���摜�uneko�v�����摜�Ƃ���D���̉摜�͏c500�摜�C��500��f�ɂ�锒���Z�W�摜�ł���D
�{�ۑ�ł̓f�B�W�^���J���[�摜�𔒍��摜�ɕϊ����Ĉ����D

ORG=imread('Lenna.png'); % ���摜�̓��� 
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ� 

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}�P�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai5-1.png?raw=true)  
�}1 ���摜

���ʎ��͈ȉ��̎��ŕ\����D  
�@ �@�S��f�̔Z�x�̕��ϒl����_r�Ƃ���B  
 �@�A�Z�xt�ŕ������Ƃ��̃N���Xi�̕��U��?��^2?_i , ���ϒl����_i , ��f����n_i �Ƃ���B  
 �@�B�N���X�����U�@?��^2?_w=(n_1 ?��^2?_1+n_2 ?��^2?_2)/(n_1+n_2) �����߂�B  
 �@�C�N���X�ԕ��U�@?��^2?_B={n_1 (��_1-��_r )^2+n_2 (��_2-��_r )^2}/(n_1+n_2) �����߂�B  
 �@�D?��^2?_B/?��^2?_w���ő�Ƃ���悤��t���߂�B  

������v���O�����ɂ���ƈȉ��̂ł���D  

H = imhist(ORG); %�q�X�g�O�����̃f�[�^���x�N�g��E�Ɋi�[  
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %�q�X�g�O������2�̃N���X�ɕ�����  
C2 = H(i+1:256);  
n1 = sum(C1); %��f���̎Z�o  
n2 = sum(C2);  
myu1 = mean(C1); %���ϒl�̎Z�o  
myu2 = mean(C2);  
sigma1 = var(C1); %���U�̎Z�o  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %�N���X�����U�̎Z�o  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %�N���X�ԕ��U�̎Z�o  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;  
 
 
IMG = ORG > max_thres;  
imagesc(IMG); colormap(gray); colorbar;  

���ʎ���p������l���̉摜�̌��ʂ�}�Q�Ɏ����D

![���摜](https://github.com/NaokiAoyama/lecture_image_processing/blob/master/image/kadai5-2.png?raw=true)  
�}2 ���ʎ���p������l���̉摜