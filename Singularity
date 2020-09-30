Bootstrap: docker
From: ubuntu:bionic

%labels
Author "Randall Cab White - rcwhite@stanford.edu"


##########
#%setup
##########

#Downlaod packages
%post
  apt-get -ym update
    ln -fs /usr/share/zoneinfo/America/Los_Angeles /etc/localtime
    apt-get install -y tzdata
    dpkg-reconfigure --frontend noninteractive tzdata

  apt-get -ym install wget curl gcc gfortran python python3 python3-pip tar bzip2 make cmake tesseract-ocr build-essential
  apt-get -ym install libturbojpeg libsdl2-dev libpoppler-cil poppler-utils
  pip3 install --upgrade pip
  python3 -m pip install pytesseract numpy pandas nltk spacy
  python3 -m pip install bs4 pdf2image

%environment
  export IMAGE_NAME="tesseract_container"
%runscript
