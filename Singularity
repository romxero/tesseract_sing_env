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
  apt-get -ym install wget curl gcc gfortran python python3 python3-pip tar bzip2 make cmake tesseract-ocr build-essential
  apt-get -ym poppler-utils libturbojpeg libsdl2-dev
  pip3 install --upgrade pip
  pip3 install request pytesseract numpy pandas nltk spacy 
  pip3 install bs4 pdf2image
 
%environment
  export IMAGE_NAME="tesseract_container"
%runscript
