
## Pre-requirements

Using pyenv is recommended and install related libraries for Python before building environment.

```
# Example for Ubuntu 20.04
sudo apt install libsqlite3-dev \
                 libreadline6-dev \
                 libbz2-dev \
                 libssl-dev \
                 libsqlite3-dev \
                 libncursesw5-dev \
                 libffi-dev \
                 libdb-dev \
                 libexpat1-dev \
                 zlib1g-dev \
                 liblzma-dev \
                 libgdbm-dev \
                 libmpdec-dev
```

## Setup Environment

```
git submodule update --init
pushd ./adi_api_mod
make
popd
pipenv sync
```
## Setup to Run
(In case target QuBE has `10.5.0.14` as the peripheral control network port)

- Power QuBEs up
- Run setup scripts for QuBEs - `TARGET_ADDR=10.5.0.14 ./adi_api_mod/setup.sh`
- Run ipynb scripts
- Enter pipenv env - `pipenv shell`
- Start Jupyter Lab - `jupyter-lab --port=8888 --ip=\* --no-browser --NotebookApp.token=''`

## Examples

- SimpleSendRecv.ipynb - sends defined wave and receives it.
- SimpleSendRecvMulti.ipynb - sends defined waves and receive them triggerd by SimpleMasterKick.
- SimpleMasterKick.ipynb - makes registration of sequences to kick SimpleSendRecvMulti.
