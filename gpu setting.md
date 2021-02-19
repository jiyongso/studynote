Server Setting
===





## Cuda setting



아래 홈페이지를 따라 세팅함.

https://aidalab.tistory.com/68



#### Cuda 설치

NVIDIA cuda 공식 사이트를 따라함.

https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=2004&target_type=deblocal



```sh
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin
sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/11.2.0/local_installers/cuda-repo-ubuntu2004-11-2-local_11.2.0-460.27.04-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu2004-11-2-local_11.2.0-460.27.04-1_amd64.deb
sudo apt-key add /var/cuda-repo-ubuntu2004-11-2-local/7fa2af80.pub
sudo apt-get update
sudo apt-get -y install cuda
```



~/.bashrc 에 다음 설정 추가

> export PATH=/usr/local/cuda-11.2/bin${PATH:+:${PATH}}
> export LD_LIBRARY_PATH=/usr/local/cuda-11.2/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}



추가 설치 명령.

```
sudo apt install libgl1-mesa-glx libegl1-mesa libxrandr2
```



## Anaconda 설치

anaconda 설치 폴더 : /opt/anaconda3



.bashrc 에 추가해줘야 하는 설정

> export PATH=/opt/anaconda3/bin${PATH:+:${PATH}}





## GIT 설치



## Jupyter notebook/lab setting

#### jupyter notebook 설정 파일 생성

터미널에서 다음 명령을 실행한다.

``jupyter notebook --generate-config``

이렇게 되면 Home directory 아래 .jupyter 폴더에 jupyter_notebook_config.py 파일이 생성된다. .jupyter 디렉토리는 숨김 파일이므로 터미널에서 *ls -al* 등의 명령을 쳐야만 보인다. 



#### 기본 jupyter directory 

아래를 참고하여 기본 jupyter directory 를 변경한다. # 혹은 ## 로 시작하는 줄은 주석이며 수정하지 않았다. 마지막 줄이 기본 디렉도리를 설정하는 명령이다.

```
## The directory to use for notebooks and kernels.
#  Default: ''
# c.NotebookApp.notebook_dir = ''
c.NotebookApp.notebook_dir = r'/home/snunsadmin/development/jupyter'
```



## cuDNN 설치

cuDNN으로부터 3개의 deb 파일을 다운로드하였다.

libcudnn8-dev_8.1.0.77-1+cuda11.2_amd64.deb
libcudnn8-samples_8.1.0.77-1+cuda11.2_amd64.deb
libcudnn8_8.1.0.77-1+cuda11.2_amd64.deb

터미널에서 아래와 같은 명령으로 설치하였다.

```
sudo dpkg -i libcudnn8_8.1.0.77-1+cuda11.2_amd64.deb 
sudo dpkg -i libcudnn8_8.1.0.77-1+cuda11.2_amd64.deb 
sudo dpkg -i libcudnn8_8.1.0.77-1+cuda11.2_amd64.deb
```

 



## Pytorch 설치

```
pip install torch==1.7.1+cu110 torchvision==0.8.2+cu110 torchaudio===0.7.2 -f https://download.pytorch.org/whl/torch_stable.html
```

- cu110 은 cuda version을 말하는 것 같은데... 현재 11.2 version이 갈려 있어서 cu112로 하면 안될까 했지만 에러 발생. 어쟀든 cu110으로 하면 된다.





## Tensorflow 설치

```null
pip install tf-nightly
```

gpu 기동 안됨. 



## Jupyter Server

jupyter notebook 을 실행한다.



## Geant4 

geatn4 source code 를 다운로드 :

- geant4.10.07.p01.tar.gz

geant4 data file download:

- G4ABLA.3.1.tar.gz
- G4EMLOW.7.13.tar.gz
- G4ENSDFSTATE.2.3.tar.gz
- G4INCL.1.0.tar.gz
- G4NDL.4.6.tar.gz
- G4PARTICLEXS.3.1.1.tar.gz
- G4PII.1.3.tar.gz
- G4PhotonEvaporation.5.7.tar.gz
- G4RadioactiveDecay.5.6.tar.gz
- G4RealSurface.2.2.tar.gz
- G4SAIDDATA.2.0.tar.gz
- G4TENDL.1.3.2.tar.gz

```
cmake  -DCMAKE_INSTALL_PREFIX=/opt/local/geant4/10.07 -DCMAKE_BUILD_TYPE=RelWithDebInfo -DGEANT4_BUILD_MULTITHREADED=ON -DGEANT4_INSTALL_DATA=ON -DGEANT4_USE_GDML=ON -DGEANT4_USE_QT=ON -DGEANT4_USE_OPENGL_X11=ON -DGEANT4_ENABLE_TESTING=OFF ../geant4
```



설치 후 .bashrc 파일에 다음 명령어 추가

```
export LD_LIBRARY_PATH=/opt/local/Geant4/lib${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
```



## Jupyter Hub

```bash
sudo apt install -y nodejs
sudo apt install -y npm
sudo npm install -g configurable-http-proxy
```

