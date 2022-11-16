---
title: RUM���g���N�X�̕���
linkTitle: RUM���g���N�X�̕���
weight: 7
isCJKLanguage: true
---

* RUM UI��RUM���g���N�X�ƃZ�b�V������������
* RUM & APM UI�ő��ւ���APM�g���[�X������

---

## 1. RUM Overview Pages

RUM Application Summary�_�b�V���{�[�h�̉E���̃g���v���h�b�g ![trippleburger](../../images/trippleburger.png) ���j���[���� *Open Application Overview* ��I�����邩�A�A�v���P�[�V�������̃����N�i�ȉ��̗�ł� *jmcj-rum-app* �j���N���b�N���� Application Overview�y�[�W���J���A�ڍ׏����m�F���邱�Ƃ��ł��܂��B

![RUM-SummaryHeader](../../images/summaryHeader.png)

�ȉ��̂悤�� RUM Application Overview �y�[�W���\������܂��B

![RUM-1](../../images/RUM-1.png)

## 2. RUM Browser�̊T�v

### 2.1. �w�b�_�[

RUM��UI�́A�傫��6�̃Z�N�V�����ō\������Ă��܂��B��ڂ͑I���w�b�_�[�ŁA�����̃I�v�V������ݒ�/�t�B���^�����O���邱�Ƃ��ł��܂��B

* ���r���[���鎞�ԃE�B���h�E��I������h���b�v�_�E���i���̏ꍇ�͉ߋ�15���j�B
* ��r�E�B���h�E��I�����邽�߂̃h���b�v�_�E���i���݂̃p�t�H�[�}���X�����[�����O�E�B���h�E�Ŕ�r���܂� - ���̏ꍇ��1���ԑO�Ɣ�r�j�B
* Environment��I������h���b�v�_�E�� (���[�N�V���b�v�u�t���񋟂�����́A�܂��͂��̗�̂悤�� *All* ��I���j�B
* �l�X��Web�A�v���̃h���b�v�_�E���i���[�N�V���b�v�u�t���񋟂�����̂��A *All* ���g�p�j�B
* ***�I�v�V����*** �u���E�U�܂��̓��o�C�����g���N�X��I������h���b�v�_�E���i*���[�N�V���b�v�ł͋��炭���p�ł��܂���*)
![RUM-Header](../../images/RUM-Header.png)

### 2.2. �T�v�y�C��

�y�[�W�̍����ɂ���T�v�y�C���ł́A���[�h���Ԃ������Ȃ����y�[�W�̊T�v���m�F���邱�Ƃ��ł��܂��B

���̗�ł� **checkout** �� **cart** �y�[�W�ɉ��F�̎O�p�`�ŃG���[�������Ă���A���[�h���Ԃ� 2.38 �b���� 5.50 �b�ɑ����������Ƃ��킩��܂��B

<!-- ![RUM-Top](../../images/RUM-TOP.png) -->

![RUM-Top](../../images/RUM-Page-Load-Times.png)

�܂��A1���������Frontend Error��Backend Errors�̌����̊T�v���\������A���̃T�C�g�ł�3��ނ�JavaScript�G���[���������Ă��邱�Ƃ�������܂��B

![RUM-Top](../../images/RUM-JS-Errors.png)

�Ō��2�̃y�C���ł́A**Top Page Views** �� **Top Network Requests** ���\������܂��B

![RUM-Top](../../images/RUM-Page-Views-Network.png)

### 2.3. Key Metrics�y�C��

Key Metrics�y�C���ł́A������ **JavaScript Errors** �� **Network Errors** �̌����A�܂� **Backend/Resource Request Duration** ���m�F�ł��܂��B�����̃��g���N�X�̓T�C�g�Ŗ�肪���������ꍇ�ɁA����������肷��̂ɔ��ɕ֗��ł��B

![RUM-KeyMetrics](../../images/RUM-Key-Metrics.png)

### 2.4. Web Vitals�y�C��

Web Vitals�y�C���́AWeb Vital�̃��g���N�X�Ɋ�Â��ăG���h���[�U�[�ɒ񋟂��Ă���G�N�X�y���G���X�Ɋւ��铴�@�𓾂����ꍇ�Ɏg�p����ꏊ�ł��B
Web Vital�́A�E�F�u��ŗD�ꂽ���[�U�[�G�N�X�y���G���X��񋟂��邽�߂ɕs���ȕi���V�O�i���̓���K�C�_���X��񋟂���Google�̃C�j�V�A�`�u�ł���A3�̎�v�ȃp�����[�^�[�ɏœ_�𓖂ĂĂ��܂��B

* **Largest Contentful Paint (LCP)** �i�ő�R���e���c�̕`��j�F�ǂݍ��݂̃p�t�H�[�}���X�𑪒肷����̂ł��B�ǂ����[�U�[�G�N�X�y���G���X��񋟂��邽�߂ɁALCP�̓y�[�W���ǂݍ��܂�Ă���2.5�b�ȓ��ɔ�������K�v������܂��B
* **First Input Delay (FID)** �i������͂܂ł̒x�����ԁj�F�C���^���N�e�B�u����]��������̂ł��B�ǂ����[�U�[�G�N�X�y���G���X��񋟂��邽�߂ɁA�y�[�W��FID��100�~���b�ȉ��ł���ׂ��ł��B
* **Cumulative Layout Shift (CLS)** �i�ݐσ��C�A�E�g�V�t�g���j�F���o�I�Ȉ��萫�𑪒肵�܂��B�ǂ����[�U�[�G�N�X�y���G���X��񋟂��邽�߂ɂ́ACLS�� 0.1 �ȉ��ňێ�����K�v������܂��B

![RUM-WebVitals](../../images/RUM-Web-Vitals.png)

### 2.5. Other Metrics�y�C��

Other Metrics�y�C���ł́A�y�[�W�̏������[�h���Ԃ⊮���܂łɎ��Ԃ������肷���Ă���^�X�N�Ȃǂ𒆐S�ɁA���̑��̃p�t�H�[�}���X���g���N�X���m�F���邱�Ƃ��ł��܂��B

* **Time To First Byte (TTFB)** �F�N���C�A���g�̃u���E�U�[���T�[�o�[���烌�X�|���X�̍ŏ��̃o�C�g����M����܂ł̎��Ԃ𑪒肵�܂��B�T�[�o�[�����N�G�X�g���������A���X�|���X�𑗐M����܂ł̎��Ԃ������قǁA�K��҂̃u���E�U�[���y�[�W��\������ۂ̑��x���x���Ȃ�܂��B
* **Long Task Duration** �F�J���҂����[�U�[�G�N�X�y���G���X�����𗝉����邽�߂Ɏg�p�ł���p�t�H�[�}���X���g���N�X�ł���A���̒���ł���\��������܂��B
* **Long Task Count** �F�����^�X�N�̔����p�x���������g���N�X�ŁA��������[�U�[�G�N�X�y���G���X�̒�������̌��o�Ɏg�p����܂��B

![RUM-Other](../../images/RUM-Other.png)

### 2.6. Custom Event�y�C��

Custom Event�y�C���ł́A�Ď����Ă���E�F�u�y�[�W�Ɏ����Œǉ������C�x���g�̃��g���N�X���\������܂��B

RUM��L���������T�C�g�Ō����悤�ɁA�ȉ���2�s��ǉ����Ă��܂��B

```javascript
const Provider = SplunkRum.provider;
var tracer=Provider.getTracer('appModuleLoader');
```

�����̍s�́A���ׂĂ̐V�����y�[�W�ɑ΂��Ď����I�ɃJ�X�^���C�x���g���쐬���܂��B�܂��A�t���[�����[�N��쐬�����C�x���g�̈ꕔ�ł͂Ȃ��J�X�^���R�[�h�ɂ�����ǉ����邱�ƂŁA�A�v���P�[�V�����̃t���[�����ǂ��������邱�Ƃ��ł��܂��B
**Custom Event Requests** �A **Custom Event Error Rates** �A **Custom Event Latency** ���T�|�[�g���Ă��܂��B

![RUM-CustomMetrics](../../images/RUM-Custom-Events.png)
