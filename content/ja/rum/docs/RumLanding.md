---
title: RUM�����f�B���O�y�[�W�̊m�F
linkTitle: RUM�����f�B���O�y�[�W�̊m�F
weight: 1
isCJKLanguage: true
---

* RUM�����f�B���O�y�[�W�ɃA�N�Z�X���A�A�v���P�[�V�����T�}���[�_�b�V���{�[�h�i���o�C������уE�F�u�x�[�X�j��RUM�Ή��A�v���P�[�V�������ׂẴp�t�H�[�}���X�̊T�v���m�F���܂��B

---

## 1. RUM�����f�B���O�y�[�W�ɃA�N�Z�X

Splunk IMT/APM/RUM �E�F�u�T�C�g�Ƀ��O�C�����܂��B�����̃��j���[�o�[���� **RUM** ��I�����܂� ![RUM-ico](../../images/RUM_ico.png) �BRUM�̃����f�B���O�y�[�W���\������܂��B

���̃y�[�W�̖ړI�́A�A�v���P�[�V�����̌��S���A�p�t�H�[�}���X�A���ݓI�ȃG���[��1�̃y�[�W�Ŗ��m�Ɏ����AWeb�y�[�W/�A�v���P�[�V����������W�������[�U�[�Z�b�V�����Ɋւ���������[���@�艺���邱�Ƃ��ł���悤�ɂ��邱�Ƃł��B�A�N�e�B�u��RUM�A�v���P�[�V�������ƂɃy�C�����\������܂��B(�ȉ��̃r���[�́A�f�t�H���g�̊g���r���[�ł��B�j

![RUM-App-sum](../../images/Applicationsummarydashboard.png)

�����̃A�v���P�[�V����������ꍇ�iRUM���[�N�V���b�v�̎Q���ґS����������ec2�C���X�^���X���g�p����ꍇ�j�A�ȉ��̂悤�Ƀy�C����܂肽���ނ��ƂŎ����I�Ƀy�C���r���[���k�������ꍇ������܂��B

![RUM-App-sum-collapsed](../../images/multiple_apps_collapsed.png)

�A�v���P�[�V�������̑O�ɂ��鍶���̐Ԃ����ŋ�������Ă��� ![RUM-browser](../../images/browser.png) �܂��� ![RUM-mobile](../../images/mobile.png) �A�C�R��(�A�v���P�[�V�����̎�ނ� *���o�C��* �� *�u���E�U�[* ���ɂ��j���N���b�N����ƁARUM Application Summry�r���[���t���_�b�V���{�[�h�ɓW�J���邱�Ƃ��\�ł��B
 
�܂��A���[�N�V���b�v�Ɏg�p����K�؂ȃA�v���P�[�V�����������܂��B

�P�Ƃ�RUM���[�N�V���b�v�ɎQ������ꍇ�A���[�N�V���b�v�u�t���g�p����A�v���P�[�V�����̖��O�������Ă���܂��B�������[�N�V���b�v�̏ꍇ�AIMT��APM�Ŏg�p���������K���ɏ]���A��̃X�N���[���V���b�g�̈�ԍŌ�ɕ\������Ă���悤�ɁA **jmcj-rum-app** �̂悤�Ƀ��j�[�NID�Ƃ���EC2�m�[�h�̖��O�ɏ]���܂��B

## 2. RUM Application Summary �_�b�V���{�[�h �̃w�b�_�[�Z�N�V������ݒ肷��

RUM Application Summary �_�b�V���{�[�h��5�̎�v�ȃZ�N�V�����ō\������Ă��܂��B��ڂ͑I���w�b�_�[�ŁA�����̃I�v�V������ݒ�/�t�B���^�����O���邱�Ƃ��ł��܂��B

* �\���Ώێ��Ԃ̂��߂� **�^�C���E�E�B���h�E** �h���b�v�_�E���i�f�t�H���g�ł͉ߋ�15���ԁj
* **Environment**[^1] ��I�����邽�߂̃h���b�v�_�E���B����ɂ��A���̊��ɑ�����A�v���P�[�V�����̃T�u�Z�b�g�݂̂Ƀt�H�[�J�X���邱�Ƃ��ł��܂��B
* �Ď��Ώۂ̂��܂��܂� **Apps** ���܂ރh���b�v�_�E�����X�g�B���[�N�V���b�v�u�t�ɂ���Ē񋟂��ꂽ���̂��g�p���邩�A���Ȃ����g�̂��̂�I�����邱�Ƃ��ł��܂��B����ɂ��A1�̃A�v���P�[�V�����Ƀt�H�[�J�X���邱�Ƃ��ł��܂��B
* **Source** �A **Browser** �A **Mobile** �A�v���P�[�V������I�����邽�߂̃h���b�v�_�E���B���[�N�V���b�v�̏ꍇ�́A *All* ��I�������܂܂ɂ��Ă��������B
* �w�b�_�[�̉E���ɂ���n���o�[�K�[���j���[�ŁASplunk RUM �A�v���P�[�V�����̂������̐ݒ���s�����Ƃ��ł��܂�(����ɂ��ẮA��̃Z�N�V�����Ő������܂�)�B

![RUM-SummaryHeader](../../images/RUM_SummaryHeader.png)

���̃Z�N�V�����ł́uApplication Summary�v��ʂ����[���@�艺���Đ������܂��B
[Check Health Browser Application](../browserapp-summary/)

---

[^1]: �f�v���C�����g���iEnvironment�j�́A�V�X�e���܂��̓A�v���P�[�V�����̌ʂ̃f�v���C�����g�ł���A�����A�v���P�[�V�����̑��̃f�v���C�����g�̐ݒ�Əd�����Ȃ��悤�ɐݒ���s�����Ƃ��ł��܂��B�J���A�X�e�[�W���O�A�{�ԂȂǁA�J���v���Z�X�̒i�K���ƂɕʁX�̃f�v���C�����g�����g�p���邱�Ƃ��悭����܂��B
</br></br>
��ʓI�ȃA�v���P�[�V�����̃f�v���C�����g�p�^�[���Ƃ��āA�݂��ɒ��ډe��������Ȃ������̈قȂ�A�v���P�[�V�������������A���������ׂ� Splunk APM �܂��� RUM �ŊĎ����邱�Ƃ�����܂��B���Ƃ��΁A�i���ۏ� (QA) ���Ɩ{�Ԋ��A�܂��͈قȂ�f�[�^�Z���^�[�A�n��A�N���E�h�v���o�C�_�[�ł̕����̈قȂ�f�v���C�����g���������܂��B