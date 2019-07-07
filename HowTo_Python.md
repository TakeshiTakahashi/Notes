# Python Memo

�����ł́APyson�ł�programming��tips���L�ڂ���B
�����_�ł́Apython 2.7���x�[�X�ɋL�q������̂Ƃ���B



# Python Installation

�܂��́Apyenv���C���X�g�[���B  
http://qiita.com/hiroseabook/items/e883e562fb7fddcfeec9  
��L���Q�l�ɂ��Ď��{�B�A���Aexec $SHELL�͂��܂������Ȃ��������߁Asource�R�}���h���g���Ē��ڐݒ�t�@�C����ǂ񂾁B
  ```source ~/.bash_profile```


pyenv�C���X�g�[���̓���m�F�͉��L�̃R�}���h���ǂ�  
  ```pyenv install --list```

���ۂɁA�C���X�g�[���������o�[�W������I��ŁApython���C���X�g�[��  
  ```pyenv install 3.4.6```


���p����o�[�W�������w��
  ```pyenv versions```
  ```pyenv global 3.4.6```


## Installation for Windows

### �{�̂�install

Python 2.7.13�������Ă����Ԃ���APython 3.6.5���C���X�g�[�������B
�Q�l�ɂ���URL�͉��L�̒ʂ�B  
https://web.plus-idea.net/2017/02/python2-3-venv-virtualenv/  
���ʁApy�R�}���h�𗘗p���Đ؂�ւ��\�ƂȂ����B

�y�[�W��ǂݍ���œf���o���ۂɁA���������������錻�ۂɂ��ẮA���L�����N�����đΉ�  
https://kanji.hatenablog.jp/entry/python-requests-beautifulsoup-encoding

Jupyter���C���X�g�[�����悤�Ƃ��Ă���Ƃ��ɁAAnaconda�̑��݂�m��BAnaconda�͑����̃p�b�P�[�W�����O�ɃZ�b�g�A�b�v���Ă���Ă���Python�̊��炵���B

### �K�v��library�� install

pandas�ȂǁA�K�v��library���C���X�g�[������ۂɂ́Apip�����p�B���L�̃����N���Q�l�ɂȂ�B

https://qiita.com/mojaie/items/241eb7006978e6962d05

�A���Apy�𗘗p���Ă���ۂɂ́A

```py -3 -m pip install pandas```

�̂悤�ɂȂ�_�ɒ��ӁB
�܂��A���ɂ���Ă͊Ǘ��Ҍ������������Ď��s���Ȃ��ƃG���[�ƂȂ�B




# Python Usage Guide

## Jupyter�̋N�����@ (on Windonws)

py -m notebook --notebook-dir=~


## Sample programs

import pandas as pd
from sklearn.datasets import load_iris

data=load_iris()
X=pd.DataFrame(data.data, columns=data.feature_names)
y=pd.DataFrame(data.target, columns=["Species"])
df=pd.concat([X,y], axis=1)
df.head()


## Pandas

Pandas�̓f�[�^�����̊�{�c�[���B�f�[�^�̐��`�Ȃǂ�����c�[����������Ă���͗l�B
DataFrame�́APandas�̎���{�\���ŁA�񎟌��z��Ɨ�������Ƃ悢�B



