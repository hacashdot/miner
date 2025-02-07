# Hacash GPU Miner

Hacash GPU miner for **Nvidia GPUs**.

## Download
Select the appropriate build based on your Nvidia GPU:

| GPU Series | CUDA Architecture | Models |
|------------|------------------|--------|
| **RTX 2000 series (Turing)** | `sm_75` | RTX 2060, 2070, 2080 |
| **RTX 3000 series (Ampere)** | `sm_86` | RTX 3060, 3070, 3080, 3090 |
| **RTX 4000 series (Ada)** | `sm_89` | RTX 4060, 4070, 4080, 4090 |

## Usage
Run the miner with the following command:

```sh
./hacashdot_miner_89 --wallet YOUR_WALLET_ADDRESS --gpus 0,1,2
```

### Arguments
- `--wallet` **(Required)**: Your Hacash wallet address.
- `--gpus` **(Required)**: Specify GPU numbers. Use comma-separated values for multiple GPUs.

### Examples
For **single GPU**:
```sh
./hacashdot_miner_89 --wallet 1Pojc73Gw9qt6k2iRbgVzvfygEKax7n9Ks --gpus 0
```
For **8 GPU mining rig**:
```sh
./hacashdot_miner_89 --wallet 1Pojc73Gw9qt6k2iRbgVzvfygEKax7n9Ks --gpus 0,1,2,3,4,5,6,7
```

## Pool Dashboard
Monitor your mining performance:

- **Pool Dashboard:** [https://ha.cash](https://ha.cash)
- **Miner Statistics:** `https://ha.cash/miner/YOURWALLET`  
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
    libjsoncpp-dev
```

### CUDA Symbolic Links
Ensure CUDA libraries are properly linked:
```sh
sudo ln -s /usr/local/cuda/lib64/libcudart_static.a /usr/lib/libcudart_static.a
sudo ln -s /usr/local/cuda/lib64/libcudart.so /usr/lib/libcudart.so
```

## License
This project is open-source under the **MIT License**.

## Support
For issues and contributions, please open an issue on the [GitHub repository](https://github.com/hacashdot/miner).
