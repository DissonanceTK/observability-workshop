---
title: Online Boutique�ł�RUM�̗��p
weight: 3
menu:
  docs:
    weight: 3
isCJKLanguage: true
---
* Online Boutique�̃A�h���X��T���܂�
* Online Boutique�̃E�F�u�V���b�v�Ŕ��������g���t�B�b�N�𐶐������܂�

---

## 1. RUM���L�������ꂽOnline Boutique��URL

�O�̃Z�N�V�����Ő��������悤�ɁARUM�z�X�g��œ��삷��Online Boutique���g�p���܂��B
RUM�݂̂̃��[�N�V���b�v�ɎQ���������́A�g�p����V�X�e���͊��ɏ�������Ă��܂��̂ŁARUM�C���X�^���X��URL���󂯎������A�Z�N�V����4 [Online Boutique���g���ăV�X�e���ɕ��ׂ�^����](./#4-Online Boutique���g���ăV�X�e���ɕ��ׂ�^����) �܂Ői�ނ��Ƃ��ł��܂��B


## 2. RUM Access Token �̓���

APM���[�N�V���b�v�ŃT�[�r�X���C���X�g�[�����܂����B���ꂩ��ARUM�@�\���f�v���C�����g�ɒǉ����Ă����܂��B

�܂��ARUM Authorization �X�R�[�v������ RUM_ACCESS_TOKEN ���擾����K�v������܂��B���[�N�V���b�v��RUM Access Token�́A **settings** ![settings](../images/setting.png) ���j���[�{�^�����N���b�N���A **Access Tokens** ��I�����邱�ƂŌ����邱�Ƃ��ł��܂��B

�u�t���g�p����悤�Ɏw������RUM���[�N�V���b�v�g�[�N���i��F **O11y-Workshop-RUM-TOKEN** �j��W�J���A **Show Token** ���N���b�N���ăg�[�N����\�����܂��B {{% labelbutton color="ui-button-grey" %}}Copy{{% /labelbutton %}} �{�^�����N���b�N���A�N���b�v�{�[�h�ɃR�s�[���Ă��������B **Default** �g�[�N���͎g�p���Ȃ��ł��������B�g�[�N����Authorization Scope��RUM�ł��邱�Ƃ��m�F���Ă��������B

![Access Token](../images/RUM-Access-Token.png)

{{% alert title="�����̃g�[�N�������Ȃ��ł�������" color="warning" %}}
���̃��[�N�V���b�v�̂��߂ɁA�F���񂪍s�����K�ɓK�����ݒ������RUM Token���쐬�����Ă��܂��B
{{% /alert %}}

�i�s���̃V�F���X�N���v�g�Ŋ��ϐ� `RUM_TOKEN` ���쐬���A�f�v���C�����g���p�[�\�i���C�Y���܂��B

{{< tabpane >}}
{{< tab header="Export Variables" lang="bash" >}}
export RUM_TOKEN=<replace_with_O11y-Workshop-RUM-TOKEN>
{{< /tab >}}
{{< /tabpane >}}

## 3. RUM��g�ݍ���Online Boutique�̃f�v���C

EC2�C���X�^���X��kubernetes�iK3s�j��Online Boutique�̃A�v���P�[�V�������f�v���C����ɂ́A���̃f�v���C�����g���폜���ARUM�p��apm config�X�N���v�g�����s���ARUM�̃f�v���C�����g��K�p���܂��B

{{< tabpane >}}
{{< tab header="Deploy Online Boutique with RUM" lang="bash" >}}
cd ~/workshop/apm
kubectl delete -f deployment.yaml
./apm-config.sh -r
kubectl apply -f deployment.yaml
{{< /tab >}}
{{< tab header="Partial Deployment Output" lang= "bash" >}}
......
Adding RUM_TOKEN to deployment
deployment.apps/recommendationservice created
service/recommendationservice created
deployment.apps/productcatalogservice created
service/productcatalogservice created
deployment.apps/cartservice created
service/cartservice created
deployment.apps/adservice created
service/adservice created
deployment.apps/paymentservice created
service/paymentservice created
deployment.apps/loadgenerator created
service/loadgenerator created
deployment.apps/shippingservice created
service/shippingservice created
deployment.apps/currencyservice created
service/currencyservice created
deployment.apps/redis-cart created
service/redis-cart created
deployment.apps/checkoutservice created
service/checkoutservice created
deployment.apps/frontend created
service/frontend created
service/frontend-external created
deployment.apps/emailservice created
service/emailservice created
deployment.apps/rum-loadgen-deployment created
{{< /tab >}}
{{< /tabpane >}}

{{% alert title="�ϐ����Z�b�g�Ɋւ��郁�b�Z�[�W���\�����ꂽ�ꍇ" color="warning" %}}
**kubectl delete -f deployment.yaml** �R�}���h�����s��APM���̃f�v���C�폜���܂��B
���ɃK�C�h�A���b�Z�[�W�ɕ\������Ă����ϐ���export����L�̃f�v���C�X�N���v�g���Ď��s���܂��B
{{% /alert %}}

## 4. Online Boutique���g���ăV�X�e���ɕ��ׂ�^����
�F����ƈꏏ��Online Boutique�ɐڑ������������V�~�����[�g���鍇�����[�U�[�����܂��B����ɂ��A�����̏ꏊ����̃g���t�B�b�N���������A��胊�A���ȃf�[�^�������܂��B

���[�N�V���b�v�u�t����URL���󂯎���Ă���͂��ł��B
�V����Web�u���E�U�𗧂��グ `http://{==RUM-HOST-EC2-IP==}:81/` �ɃA�N�Z�X�����RUM���L�������ꂽOnline Boutique���\������܂��B

![Online Boutique](../images/online-boutique.png)

## 5. �g���t�B�b�N�𔭐�������

���̉��K�̖ړI�́ARUM���L�������ꂽOnline Boutique���{�����A���܂��܂ȏ��i�Ɛ��ʂ̑g�ݍ��킹�ōw�����邱�Ƃł��B
����ɕʂ̃u���E�U��X�}�[�g�t�H������A�N�Z�X���邱�Ƃ��ł��܂��B

����ɂ�蕡���̃Z�b�V�������쐬����A�������邱�Ƃ��ł��܂��B��������Ƌᖡ���āA���낢��ȏ��i���w�����J�[�g�ɓ���Ă��������B

![Cart Online Boutique](../images/cart.png)

Home Barista Kit�悭�Ȃ��ł����H...  �V���b�s���O���y����ł��������I

![Clock](../images/Clock.gif)
