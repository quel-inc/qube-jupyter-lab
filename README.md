
## Setup Environment

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
```
## Setup to Run

- Power QuBEs up
- Run setup scripts for QuBEs - `TARGET_ADDR=10.5.0.14 ./qube_calib/adi_api_mod/setup.sh`
- Run ipynb scripts
- Enter pipenv env - `pipenv shell`
- Start Jupyter Lab - `jupyter-lab --port=8888 --ip=\* --no-browser --NotebookApp.token=''`

## Examples

- SimpleSendRecv.ipynb - sends defined wave and receives it.
- SimpleSendRecvMulti.ipynb - sends defined waves and receive them triggerd by SimpleMasterKick.
- SimpleMasterKick.ipynb - makes registration of sequences to kick SimpleSendRecvMulti.
