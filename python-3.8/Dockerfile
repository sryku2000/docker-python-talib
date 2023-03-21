FROM python:3.8

MAINTAINER Olivier TASSEL <https://github.com/otassel>

WORKDIR /usr/src

RUN ln -sf /usr/share/zoneinfo/Asia/Taipei /etc/localtime

RUN pip install numpy mplfinance pandas shioaji load_dotenv bokeh==2.4.3 backtesting 

RUN ta-lib

