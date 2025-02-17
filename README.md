# Hacash GPU Miner

Hacash GPU miner for **Nvidia GPUs**. 

Supported cards 2000, 3000, 4000 series

## Usage
Run the miner with the following command:

```sh
./hacashdot_miner --wallet YOUR_WALLET_ADDRESS --gpus 0,1,2
```

### Arguments
- `--wallet` **(Required)**: Your Hacash wallet address.
- `--gpus` **(Required)**: Specify GPU numbers. Use comma-separated values for multiple GPUs.

### Examples
For **single GPU**:
```sh
./hacashdot_miner --wallet 1Pojc73Gw9qt6k2iRbgVzvfygEKax7n9Ks --gpus 0
```
For **8 GPU mining rig**:
```sh
./hacashdot_miner --wallet 1Pojc73Gw9qt6k2iRbgVzvfygEKax7n9Ks --gpus 0,1,2,3,4,5,6,7
```

## Pool Dashboard
Monitor your mining performance:

- **Pool Dashboard:** [http://ha.cash](http://ha.cash)
- **Miner Statistics:** `http://ha.cash/miner/YOURWALLET`  
  *(Replace `YOURWALLET` with your wallet address.)*

## Hashrate Calculation
Hashrate is calculated using an **average 1-minute rolling window**.

## Dependencies
Before running the miner, install the required dependencies:
```sh
sudo apt-get update
sudo apt-get install -y \
    build-essential \
    cuda-toolkit \
    libcurl4-openssl-dev \
    libjsoncpp-dev \
    libssl-dev
```

### CUDA Symbolic Links
Ensure CUDA libraries are properly linked:
```sh
sudo ln -s /usr/local/cuda/lib64/libcudart_static.a /usr/lib/libcudart_static.a
sudo ln -s /usr/local/cuda/lib64/libcudart.so /usr/lib/libcudart.so
```

### Hashrate

| GPU Model    | Hashrate (MH/s) |
|-------------|---------------|
| **RTX 4090** | 100           |
| **RTX 4070** | 55            |
| **RTX 4070 Ti** | 60        |
| **RTX 4060 Ti** | 32        |
| **RTX 3090** | 46            |
| **RTX 3080 Ti** | 46        |
| **RTX 3080** | 40            |
| **RTX 3070** | 29            |
| **RTX 3070 Ti** | 31        |
| **RTX 3060** | 19            |
| **RTX 3060 Ti** | 25        |
| **RTX 2060** | 16            |
| **RTX 2070** | 17            |
| **RTX 2080** | 24            |
| **RTX 2080 Ti** | 31        |


## License
This project is open-source under the **MIT License**.

## Support
For issues and contributions, please open an issue on the [GitHub repository](https://github.com/hacashdot/miner).
