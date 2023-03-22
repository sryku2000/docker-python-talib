# Work directory
This image workdir is /usr/src

# Main Libraries
The main libraries include **Talib** and **Shioaji API**.

# Other Libraries Used for Calculation
Other libraries used for calculation are:
```
numpy mplfinance pandas shioaji load_dotenv bokeh==2.4.3 backtesting
```
# Execution Method
The execution method is as follows:
```
docker run -v {host directory}:{container directory} -t -i --rm sryku2000/python-3.8-talib-shioaji {bash command}
```
## example
```
docker run -v /home/user/example_python:/usr/src -t -i --rm sryku2000/python-3.8-talib-shioaji python main.py
```

# Github Link
https://github.com/sryku2000/docker-python-talib
