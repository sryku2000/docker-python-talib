FROM python:3.8-slim

MAINTAINER Sryku2000 <https://github.com/sryku2000>

WORKDIR /usr/src

RUN ln -sf /usr/share/zoneinfo/Asia/Taipei /etc/localtime

RUN apt-get update \
 && apt-get install wget unzip zip gcc build-essential -y 

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

RUN pip install ta-lib
