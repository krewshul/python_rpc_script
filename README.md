# SIMPLE PYTHON SCRIPT TO DISPLAY COIN AND WALLET INFO ONTO A WEBPAGE



## step 1:
### CLONE THIS REPO

```git clone https://github.com/krewshul/python_rpc_script.git```

## step 2:
### INSTALL DEPENDENCIES

```sudo apt install apache2```

```cd python_rpc_script```

```pip install python-jsonrpc```

```pip install python-bitcoinrpc```

## step 3:
### CHANGE INFO AND AUTH TO MATCH YOUR INFO IN THE .CONF FILE OF YOUR WALLET

**ON LINE 6** add your rpcuser, rpcpassword, and  rpcport 

`access = AuthServiceProxy("http://RPCUSER:RPCPASSWORD@127.0.0.1:RPCPORT")`

**ON LINE 24** add your coin name

`ff.write("<h1> YOUR COINS NAME <br\></h1>")`

## step 4:
### RUN THE COMMAND

```python python_rpc_script.py```

![example](https://raw.githubusercontent.com/krewshul/testering/main/images/example.PNG)



### this will create 2 pages in '/var/www/html/' called 'index.html' and 'styles.css'

if wanting to make the page update automatically you can set a crontab timer, or use a blocknotify script in your conf file for it to update every block.  I prefer running it with 

`watch -n 300 -x python python_rpc_script.py` in a tmux screen
