
```
git clone git@github.com:qiqb-osaka/qube-calib.git
git clone git@github.com:quel-inc/qube_master
cd qube-calib
git update --init --recursive
cd qube-calib/adi_api_mod
make
cd ../..
ln -s qube-calib/.config
pipenv install
jupyter-lab --port=8888 --ip=\* --no-browser --NotebookApp.token=''
```
