---
title: Splunk RUM �� APM �o�b�N�G���h�T�[�r�X�̑���
linkTitle: RUM �� APM�̑���
weight: 13
isCJKLanguage: true
---

* RUM UI��RUM Session�̏��𑱂��܂�
* APM & Log Observer UI �ő��ւ��� APM �g���[�X�ƃ��O���m�F���܂�

---

## 1. �o�b�N�G���h�T�[�r�X�̖��𔭌�

![RUM-JS](../../images/RUM-JS-Error.png) ���N���b�N���āASpan�r���[����܂��B
���ɉ��ɃX�N���[�����A **POST /cart/checkout** �̍s�������܂��B

![RUM-APM-Click](../../images/RUM-APM-Click.png)

�F�� ![RUM-APM-BLUE](../../images/RUM-APM.png) �����N���N���b�N����ƁA�G���h���[�U���s�����`�F�b�N�A�E�g����̈ꕔ�ł���o�b�N�G���h�T�[�r�X�Ɋւ�����������_�C�A���O���|�b�v�A�b�v�\������܂��B

![RUM-APM-Trace](../../images/RUM-Trace.png)

���̃|�b�v�A�b�v�ł͕����̃Z�N�V�������p�ӂ���Ă���A�o�b�N�G���h�T�[�r�X�̋�����f�����c�����邱�Ƃ��ł��܂��B�Ⴆ�΁APerformance Summary�Z�N�V�����ł́A�o�b�N�G���h�̌Ăяo�����ɂǂ��Ɏ��Ԃ���₳�ꂽ����m�邱�Ƃ��ł��܂��B

![RUM-APM-Trace-perf](../../images/RUM-Trace-Performance.png)

��L�̗�ł�77.9%�ȏオ�O���T�[�r�X�ɔ�₳��Ă��邱�Ƃ��킩��܂��B

�_�C�A���O�̈�ԉ��܂ŃX�N���[������ƁA���}�̂悤�ȁu�g���[�X�ƃT�[�r�X�v�Z�N�V�������\������܂��B

![RUM-APM-Trace-services](../../images/RUM-Trace-Services.png)

**Checkout** �T�[�r�X�� **Payment** �T�[�r�X���A�����Ƃ��Z���ԐF�ŕ\������Ă��܂��B�����Ԃ̓G���[���󂯎�������Ƃ��Ӗ����A�Z���Ԃ͂��̃T�[�r�X���甭�������G���[���Ӗ����܂��B


![RUM-APM-Trace-services-detail](../../images/RUM-Trace-Services-Detail.png)

�܂�A���łɃo�b�N�G���h�̃T�[�r�X�ɖ�肪���邱�Ƃ͖����Ȃ̂ł��B

�������Ă݂܂��傤�I

## 2.  Backend�T�[�r�X�܂ł̃g���[�X�����ǂ�

Trace Id�����N���N���b�N���邱�Ƃ��ł��܂��B

![RUM-APM-Trace-link](../../images/RUM-Trace-url.png)

����ɂ��A�o�b�N�G���h�T�[�r�X�ւ̌Ăяo���ŉ����N�����������ڍׂɎ����E�H�[�^�[�t�H�[��APM�r���[���\������܂��B
�E���ɂ́ATrace ID�ƁA�O�Ɍ����悤�ɁAPerformance Summury���\������Ă��܂��B
�E�H�[�^�[�t�H�[���ł́A�t�����g�G���h����̌Ăяo���̈ꕔ�ł���l�X�ȃo�b�N�G���h�T�[�r�X����肷�邱�Ƃ��ł��܂��B


�����̂悤�ɁA **Checkout** �T�[�r�X�� **Payment** �T�[�r�X�̑O�ɐԂ��G���[�C���W�P�[�^  ![RUM-APM-error-flag](../../images/APM_Error_Flag.png) �������܂��B

![RUM-APM-waterfall](../../images/RUM-APM-Waterfall.png)

**paymentservice: grpc.hipstershop.PaymentService/Charge** �̍s�̌�ɂ��� ![RUM-APM-error-flag](../../images/APM_Error_Flag.png) ���N���b�N���Ă��������B

![RUM-payment-click](../../images/payment-click.png)

Span�̏ڍ׃y�[�W���\������A���̃T�[�r�X�R�[���̏ڍ׏�񂪕\������܂��B
**401** �G���[�R�[�h�A�܂� *Invalid Request* ���Ԃ��ꂽ���Ƃ��m�F�ł��܂��B

## 3.  �֘A���郍�O���m�F

Splunk Observability Cloud�́A�g���[�X���g���N�X�ƃ��O�������I�Ɋ֘A�t���邽�߁A�y�[�W�����̊֘A�R���e���c�o�[�ɁA���̃g���[�X�ɑΉ����郍�O���\������܂��B

![RUM-payment-related-content](../../images/log-corelation.png)

Log�̃����N���N���b�N����ƁA���O���\������܂��B

���O���\�����ꂽ��A�y�[�W�̏㕔�ɂ���t�B���^�[�ɃN���b�N����Trace ID���Z�b�g����A���̃g���[�X�Ɋ֘A���郍�O���\������Ă��邱�Ƃɒ��ӂ��Ă��������B
����Payment�T�[�r�X�̃G���[�������s��1��I������ƉE���Ƀ��O���b�Z�[�W���\������܂��B

������Payment�T�[�r�X�����s�������R�����m�Ɏ�����Ă��܂��B�T�[�r�X�ɑ΂��Ė����ȃg�[�N�����g�p���Ă���̂ł��B 

***Failed payment processing through ButtercupPayments: Invalid API Token (test-20e26e90-356b-432e-a2c6-956fc03f5609)**

![RUM-logs](../../images/RUM-LogObserver.png)

## 4. �܂Ƃ�

RUM���g���N�X���g�p����Web�T�C�g�̃p�t�H�[�}���X�𒲍����܂����B
Tag Profile���g�p���āA�����̃Z�b�V�������������A�Z�b�V�����E�H�[�^�[�t�H�[�����g�p���āA2�̖�����肵�܂����B

* JavaScript�̃G���[�ɂ��A���i�̌v�Z�� 0 �ɂȂ��Ă��܂����B
* �x�����o�b�N�G���h�T�[�r�X�ɖ�肪����x�����Ɏ��s���邱�Ƃ�����܂����B

RUM�̃g���[�X�ƃo�b�N�G���hAPM�̃g���[�X����у��O���֘A�t����@�\���g�p���āA�x�������s�̌����𔭌����܂����B
