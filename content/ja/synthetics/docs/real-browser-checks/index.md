---
title: Real Browser Check 
linkTitle: Real Browser Check 
weight: 1
description: >
  Real Browswer Check �̃X�N���v�g�Ɛݒ�
isCJKLanguage: true
---

���̃��{�ł� [Chrome Selenium IDE](https://chrome.google.com/webstore/detail/selenium-ide/mooikfkahbdckldjjndioackbalphokd?hl=en) �G�N�X�e���V�������g�p����Splunk�f���C���X�^���X�ɑ΂��鍇���g�����U�N�V�����ƁASplunk Synthetic Monitoring Real Browser Check (RBC)���쐬���܂��B

## 1. �O��

[https://monitoring.rigor.com](https://monitoring.rigor.com) �� [https://optimization.rigor.com](https://optimization.rigor.com) �Ƀ��O�C���ł��邱�Ƃ��m�F���܂��B�܂��A **O11y Workshop** �̂悤�ȃA�J�E���g�ɃA�T�C������Ă��邱�Ƃ��m�F���܂��B

Splunk Synthetic Monitoring �A�J�E���g�̌l����ҏW���A�^�C���]�[���ƃ��[���ʒm��ҏW���܂��BSplunk Synthetic Monitoring �̓f�t�H���g�Œʒm���܂����A���j�^�[�̐ݒ�Œʒm���I�t�ɂ��邱�Ƃ��ł��܂��B

![Edit Personal Information](../../images/image5.png)

[Chrome Selenium IDE](https://chrome.google.com/webstore/detail/selenium-ide/mooikfkahbdckldjjndioackbalphokd?hl=en-US) �G�N�X�e���V���������Ȃ��� **Chrome** �u���E�U�[�ɒǉ����܂��B�C���X�g�[��������A�G�N�X�e���V�������N���b�N���邱�ƂŎ��̉�ʂ��\������܂��B

![Selenium IDE](../../images/image17.png)

## 2. Selenium IDE �̎g�p

[http://splunk.o11ystore.com](http://splunk.o11ystore.com) �ɃA�N�Z�X���ASelenium IDE���g���E�F�u�g�����U�N�V�������L�^���鏀���������܂����B

**Record a new test in a new project** ���N���b�N���v���W�F�N�g���� **[���Ȃ��̃C�j�V����] - O11y Store** �i��FRWC - O11y Store�j�Ɠ��͂��܂��B

!!! ���� �uSelenium IDE�Ƃ͉��ł����H�v
    - Selenium IDE �́A�I�[�v���\�[�X�� Web �p�̋L�^�ƍĐ��̃e�X�g�������c�[���ł��B
    - Selenium��Web�A�v���P�[�V�������e�X�g���邽�߂̃|�[�^�u���ȃt���[�����[�N�ł��B
    - Selenium �̓e�X�g�X�N���v�g���� (Selenium IDE) ���w�ԕK�v�Ȃ��ɋ@�\�e�X�g���쐬���邽�߂̍Đ��c�[����񋟂��܂��B
    - C#�AGroovy�AJava�APerl�APHP�APython�ARuby�AScala�Ȃǂ̑����̈�ʓI�ȃv���O���~���O����Ńe�X�g���L�q���邽�߂̃e�X�g�h���C���ŗL�̌���iSelenese�j��񋟂��܂��B
    - �e�X�g�͂قƂ�ǂ̍ŐV��Web�u���E�U�Ŏ��s�ł��܂��B
    - Selenium�́AWindows�ALinux�AmacOS��œ��삵�܂��B
    - Apache License 2.0�̉��Ō��J����Ă���I�[�v���\�[�X�\�t�g�E�F�A�ł��B


![placeholder](../../images/image29.png)

Base URL�� [http://splunk.o11ystore.com](http://splunk.o11ystore.com) �Ɠ��͂��܂��B

![placeholder](../../images/image11.png)

Start Recording{: .label-button .sfx-ui-button-grey} ���N���b�N����� [splunk.o11ystore.com](http://splunk.o11ystore.com)  ���J���ꂽ�V�����E�C���h�E�������オ��܂��B **Vintage Camera Lens** ���N���b�N���A **Add To Cart** ���N���b�N���A���� **Place Order** ���N���b�N���܂��B

�E�C���h�E����ASelenium IDE�ɖ߂背�R�[�f�B���O���~���܂��B�Ō�Ƀe�X�g�P�[�X�ɖ��O��t���܂��B **[���Ȃ��̃C�j�V����] - Checkout Flow (Desktop)** �i��FRWC - Checkout Flow (Desktop)�j

![placeholder](../../images/image10.png)

���Ȃ���Selenium IDE�v���W�F�N�g�́A���̂悤�ɂȂ�܂��B

![placeholder](../../images/image19.png)

�Đ��{�^���������ă��R�[�f�B���O���e�X�g���A���R�[�f�B���O���g�����U�N�V�����𐳏�Ɋ������邱�Ƃ��m�F���Ă��������B

![Run](../../images/image26.png)

Selenium IDE �v���W�F�N�g���_�E�����[�h�t�H���_�� `Workshop.side` �Ƃ������O�ŕۑ����܂��B

![Save](../../images/image30.png)

![Save SIDE Project](../../images/save-side-project.png)

## 3. Real Browser Check �̍쐬

[https://monitoring.rigor.com](https://monitoring.rigor.com) ����Splunk Synthetic Monitoring�Ƀ��O�C�����܂��B **REAL BROWSER** ���N���b�N���A **+New**{: .label-button .sfx-ui-button-blue} ���N���b�N���܂��B

![placeholder](../../images/image3.png)

�u**From File**�v���N���b�N�����R�[�f�B���O�t�@�C����I�����AImport���N���b�N���܂��B

![placeholder](../../images/image1.png)

**Frequency** �� **5 Minutes** �ɃZ�b�g���܂��B

![placeholder](../../images/image15.png)

�eStep���N���b�N���A���̂悤�ɕ�����₷�����O��t���Ă����܂��B
Step 1 (Click Camera)

Step 2 (Add to Cart)

Step 3 (Place Order)


![placeholder](../../images/image6.png)

���� **+ Add Step** ���N���b�N���A�o���f�[�V�����p�̃X�e�b�v��ǉ����܂��B����̓`�F�b�N�A�E�g�������������ǂ������m���߂���̂ł��B

**Name** �� **Confirm Order** �Ɠ��͂��A **Action** �� **Wait for text present** �ɕύX���A **Value** �� **Your order is complete!** �Ɠ��͂��܂��B�����܂ł� **Start Url** ��4�̃X�e�b�v������܂����B

![placeholder](../../images/image2.png)

{{% alert title="Tip" color="info" %}}
Step�쐬���ɂ͔��ɋ��͂� [Business Transaction](https://help.rigor.com/hc/en-us/articles/360049442854-How-Do-I-Use-Business-Transactions) �@�\�̗��p�����������������B*�uBusiness Transaction�Ƃ́AReal Browser�X�N���v�g���̘A�������X�e�b�v���܂Ƃ߂����̂ł��B�����̃g�����U�N�V�����́A�t���[�̗ގ�������_���I�ɃO���[�v�����A���[�U�[�͕����̃X�e�b�v�ƃy�[�W�i�����j�̃p�t�H�[�}���X��1�̃r�W�l�X�g�����U�N�V�����ɂ܂Ƃ߂ĕ\���ł���悤�ɂ��܂��B"*
{{% /alert %}}

**Advanced** ���N���b�N���A **Viewport Size** �� **Default desktop: 1366 x 768** �ł��邱�Ƃ��m�F���܂��B

![Viewport Size](../../images/viewport-size.png)

�u**Test**�v���N���b�N�����j�^�[�ݒ���e�X�g���܂��B�e�X�g������Ɋ���������AStep 4�́u**AFTER**�v���N���b�N���A���������̃X�N���[���V���b�g���擾�ł������Ƃ��m�F���Ă��������B

![placeholder](../../images/image22.png)

**Create**{: .label-button .sfx-ui-button-blue} ���N���b�N���AReal Browser Monitor��ۑ����܂��B5����10����Ƀ��j�^�[�����삵�A�ȉ��̂悤�ȃ`�F�b�N�������\������邱�Ƃ��m�F���܂��B

![placeholder](../../images/image27.png)

{{% alert title="Tip" color="info" %}}
**Run Now** �����s���邱�ƂŃ��j�^�[�𑦍��Ɏ��s�ł��܂��B

![placeholder](../../images/image8.png)
{{% /alert %}}

**Segment by location** ���N���b�N���A�����ڂ̕ω����m�F���Ă��������B�N���b�N���邱�ƂŊe���P�[�V������on/off���\�ł��B

!!! ���ł��I
    **Response Time** ����ԒႢ���P�[�V�����͂ǂ��ł��傤���H

![placeholder](../../images/image9.png)

���������~�̂����ǂꂩ���N���b�N���A���s���ʂɃh�����_�E�����܂��B

![placeholder](../../images/image33.png)

**CONFIGURE METRICS/HIDE METRICS** �h���b�v�_�E���ŁA�擾���Ă��郁�g���N�X���m�F���Ă݂Ă��������B

![placeholder](../../images/image14.png)

�h���b�v�_�E���� **Page 2** ���N���b�N���A **Filmstrip** �� **Waterfall Chart** �܂ŃX�N���[���_�E�����Č��ʂ��m�F���Ă��������B

![placeholder](../../images/image16.png)

![Filmstrip](../../images/filmstrip.png)

![Waterfall](../../images/waterfall.png)

**Click Here to Analyze with Optimization** ���N���b�N�����Splunk Synthetic Monitoring Optimization�ւ̃��O�C�����ł��܂��B���� **���̃I�v�V�������\������Ȃ��ꍇ** �A���� [�y�[�W](https://optimization.rigor.com/s/2373818/?sh=3AF8C48AADD6D3E5F5DAA8B4B7BB7F45) �ɃA�N�Z�X���Ă��������B

![placeholder](../../images/image31.png)

�u**Best Practices Score**�v�^�u���N���b�N���܂��B�X�N���[���_�E�����A���ʂ��m�F���܂��B

![placeholder](../../images/image23.png)

![Best Practices](../../images/best-practices.png)

���Ԃ��Ƃ��āA���ʂ����r���[���Ă݂Ă��������B���̍��ڂ��N���b�N���Ă݂Ă��������B

## 4. Mobile Check �̍쐬

�쐬����RBC (Real Browser Check�j���R�s�[���܂��B

![Copy Check](../../images/copy-check.png)

���O�� **RWC - Checkout Flow (Tablet)** �̂悤�ɕύX���܂��B

![Copy Check](../../images/rename-check.png)

**Advanced** �^�u�z���ňȉ���3�̐ݒ��ύX���A�V�������o�C���p��RBC���쐬���܂��B

![placeholder](../../images/image18.png)

�V�������j�^�[�ݒ���e�X�g���m�F���܂��B

{{% alert title="Tip" color="info" %}}
Step�쐬���ɂ͔��ɋ��͂� [Business Transaction](https://help.rigor.com/hc/en-us/articles/360049442854-How-Do-I-Use-Business-Transactions) �@�\�̗��p�����������������B*�uBusiness Transaction�Ƃ́AReal Browser�X�N���v�g���̘A�������X�e�b�v���܂Ƃ߂����̂ł��B�����̃g�����U�N�V�����́A�t���[�̗ގ�������_���I�ɃO���[�v�����A���[�U�[�͕����̃X�e�b�v�ƃy�[�W�i�����j�̃p�t�H�[�}���X��1�̃r�W�l�X�g�����U�N�V�����ɂ܂Ƃ߂ĕ\���ł���悤�ɂ��܂��B"*
{{% /alert %}}

## 5. ���\�[�X

- [Getting Started With Selenium IDE](https://help.rigor.com/hc/en-us/articles/115004652007?flash_digest=b1ef7d1a07b68d5279ee5fef8adb87fb878cf010)

- [Splunk Synthetic Monitoring Scripting Guide](http://www2.rigor.com/scripting-guide)

- [How Can I Fix A Broken Script?](https://help.rigor.com/hc/en-us/articles/115004443988-How-Can-I-Fix-A-Broken-Script)

- [Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) (Document Object Model (DOM)

- [Selenium IDE](https://www.selenium.dev/selenium-ide/)
