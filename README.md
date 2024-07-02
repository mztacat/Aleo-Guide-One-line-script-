# Aleo-Guide-One-line-script-
Using Nodeguru guide here 



-------------
## Install Using Nodeguru script for a quick installation:

```
wget -q -O aleo_snarkos3.sh https://api.nodes.guru/aleo_snarkos3.sh && chmod +x aleo_snarkos3.sh && sudo /bin/bash aleo_snarkos3.sh
```

### Once the installation is complete, the prover will start automatically, but you can stop it ```sudo systemctl stop aleo-prover``` and start the client ```sudo systemctl restart aleo-client``` .   
--------------------



## 2. Useful commands

Check your Aleo account.
!!! SAVE THESE KEYS IN A SAFE PLACE !!!

```
cat $HOME/aleo/account_new.txt
```

## Check what Aleo Private Key is used by your prover.

```
grep "PRIVATE" /etc/systemd/system/aleo-prover.service | awk -F '=' '{print $3}'
```


## Check aleo prover logs:

```
journalctl -u aleo-prover -f -o cat
```


## Check the aleo client logs if it is running:
```
journalctl -u aleo-client -f -o cat
```



## Stop the aleo prover and start the aleo client:
```
systemctl stop aleo-prover
systemctl restart aleo-client
```


### 2.5 Running the prover(Already running after installation).
```
systemctl stop aleo-client
systemctl restart aleo-prover
```


### 2.6 Remove snarkOS and all source files, including aleo miner address.
```
wget -q -O aleo_remove_snarkos.sh https://api.nodes.guru/aleo_remove_snarkos2.sh && chmod +x aleo_remove_snarkos.sh && sudo /bin/bash aleo_remove_snarkos.sh
```




















