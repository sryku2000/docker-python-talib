FROM python:3.8-alpine

MAINTAINER Olivier TASSEL <https://github.com/otassel>

WORKDIR /usr/src

RUN ln -sf /usr/share/zoneinfo/Asia/Taipei /etc/localtime

RUN apk update
RUN apk add musl-dev wget git build-base make automake gcc g++ subversion python3-dev

RUN pip install --upgrade pip
RUN pip install cython
RUN ln -s /usr/include/locale.h /usr/include/xlocale.h
RUN pip install numpy mplfinance pandas shioaji load_dotenv bokeh==2.4.3 backtesting 

# TA-Lib
RUN wget http://prdownloads.sourceforge.net/ta-lib/ta-lib-0.4.0-src.tar.gz && \
  tar -xvzf ta-lib-0.4.0-src.tar.gz && \
  cd ta-lib/ && \
  ./configure --prefix=/usr && \
  make && \
  make install
RUN git clone https://github.com/mrjbq7/ta-lib.git /ta-lib-py && cd ta-lib-py && python setup.py install

RUN pip install ta-lib

RUN apk del musl-dev wget git build-base make automake gcc g++ subversion python3-dev