# Executor

## Setup project
### Requirements
* Ubuntu machine
* install [docker](https://docs.docker.com/engine/install/ubuntu/)


### Step 1: Clone project

```
git clone https://github.com/Datura-ai/compute-subnet.git
```

### Step 2: Install Required Tools

Run following command to install required tools: 
```shell
cd compute-subnet && chmod +x scripts/install_executor_on_ubuntu.sh && scripts/install_executor_on_ubuntu.sh
```

### Step 3: Install and Run

* Go to executor root
```shell
cd neurons/executor
```

* Add .env in the project
```shell
cp .env.template .env
```

Add the correct miner wallet hotkey for `MINER_HOTKEY_SS58_ADDRESS`.
You can change the ports for `INTERNAL_PORT`, `EXTERNAL_PORT`, `SSH_PORT` based on your need.

```
INTERNAL_PORT: internal port of your executor docker container
EXTERNAL_PORT: external expose port of your executor docker container
SSH_PORT: ssh access port of your executor docker container
MINER_HOTKEY_SS58_ADDRESS: the miner hotkey address
```

* Run project
```shell
docker compose up -d
```