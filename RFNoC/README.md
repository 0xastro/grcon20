### Ubuntu 20.04 Dependencies:
```
sudo apt install git cmake g++ libboost-all-dev libgmp-dev swig \
python3-numpy python3-mako python3-sphinx python3-lxml \
doxygen libfftw3-dev libsdl1.2-dev libgsl-dev libqwt-qt5-dev \
libqt5opengl5-dev python3-pyqt5 liblog4cpp5-dev libzmq3-dev \
python3-yaml python3-click python3-click-plugins python3-zmq \
python3-scipy python3-gi python3-gi-cairo gobject-introspection \
gir1.2-gtk-3.0 build-essential libusb-1.0-0-dev python3-docutils \
python3-setuptools python3-ruamel.yaml python-is-python3
```

> Getting Vivado 2019.1 to work in Ubuntu 20.04:
```
sudo apt install libtinfo5 libncurses5
```

### Installing software:

> UHD 4.0:
```
git clone --branch UHD-4.0 https://github.com/ettusresearch/uhd.git uhd
mkdir uhd/host/build; cd uhd/host/build; cmake ..
make -j4; sudo make install
```

> GNU Radio 3.8:
```
git clone --branch maint-3.8 --recursive https://github.com/gnuradio/gnuradio.git gnuradio
mkdir gnuradio/build; cd gnuradio/build; cmake ..
make -j4; sudo make install
```

> gr-ettus:
```
git clone --branch maint-3.8-uhd4.0 https://github.com/ettusresearch/gr-ettus.git gr-ettus
mkdir gr-ettus/build; cd gr-ettus; cmake -DENABLE_QT=True ..
make -j4; sudo make install
```
