---
title: RUM Session�̕���
linkTitle: RUM Session�̕���
weight: 11
isCJKLanguage: true
---

* RUM UI��RUM Session�̏��𒲍�����
* ���[�U�[�C���^���N�V������Span��Javascript�̃G���[����肷��

---

## 1. cart URL���ĂёI��

�^�C���Z���N�^�Ŏ��ԑт�I��������A�ȉ��̂悤�� **Url Name**�r���[���� *cart* URL���đI������K�v������܂��B

![RUM-Cart-3](../../images/RUM-Cart-All.png)

��̗�ł� `http://34.246.124.162:81/cart` ��I�����܂����B

## 2. Sessions�Ƀh�����_�E��

Tag Spotlight�ŏ��𕪐͂��A�g���[�X�̃T�u�Z�b�g���h�����_�E��������A�G���h���[�U�[�̃u���E�U�[�Ŏ��s���ꂽ���ۂ̃Z�b�V������\�����邱�Ƃ��ł��܂��B

�ȉ��̂悤�� **Example Sessions** �Ƃ��������N���N���b�N���邱�Ƃōs���܂��B

![RUM-Header](../../images/RUM-ExampleSessions.png)

����ɂ��A���ԃt�B���^�ƃ^�O�v���t�@�C���őI�������T�u�Z�b�g�̗����Ɉ�v����Z�b�V�����̃��X�g���\������܂��B

�Z�b�V����ID���N���b�N���܂��B�ł��������ԁi700 �~���b�ȏオ�]�܂����j�̂��̂�I������Ƃ悢�ł��傤�B

![RUM-Header](../../images/RUM-Session-Selected.png)

�Z�b�V������I������ƁA�Z�b�V�����̏ڍ׃y�[�W���\������܂��B�Z�b�V�����̈ꕔ�ł������̃A�N�V������I�����Ă��邽�߁A�Z�b�V�������̂ǂ����̃C���^���N�V�����ɂ��ǂ蒅���\���������ł��B
��قǑI������URL `http://34.246.124.162:81/cart` ���A�Z�b�V�����X�g���[���Ńt�H�[�J�X���Ă���ꏊ�ł��邱�Ƃ��킩��܂��B

![RUM-Session-Tag](../../images/Session-Tag.png)

�y�[�W���������ɃX�N���[������ƁA�ȉ��̂悤�ɑ���̏I��肪�\������܂��B

![RUM-Session-info](../../images/Session-Tag-2.png)

�G���h���[�U�[�ɂ͌��o����Ȃ��������A�܂��͕\������Ȃ������\���̂��邢������JavaScript Console�G���[���������Ă��邱�Ƃ��킩��܂��B�����̃G���[���ڂ������ׂ�ɂ́A�^�񒆂̃G���[ **Cannot read properties of undefined (reading 'Prcie')** ���N���b�N���Ă��������B

![RUM-Session-info](../../images/Session-Tag-3.png)

����ɂ���ăy�[�W���W�J����A���̃C���^���N�V������Span�̏ڍׂ��\������܂��B���̃y�[�W�ɂ́A�����������邽�߂ɊJ���҂ɓn�����Ƃ��ł���ڍׂ� *error.stack* ���܂܂�܂��BOnline Boutique�ŏ��i���w�������ہA�ŏI�I�ȍ��v���z�����0�h���ł��邱�Ƃɂ��C�Â��ł��傤���B

![RUM-Session-info](../../images/Session-Tag-4.png)
