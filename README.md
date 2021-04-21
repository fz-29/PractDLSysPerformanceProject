# Practical Deep Learning System Performance Project

Distributed Training implementation of StackGAN

Submission By:

1. Feroz Ahmad (fa2581)
2. Li Cai (lc2928)

## Steps:

1. Requirements

`pip install -r requirements.txt`

2. Download text annotations and text embedding generator given by the authors of the paper

`sh getgdrive.sh 0B3y_msrWZaXLT1BZdVdycDY5TEE birds.zip`

3. Unzip above downloaded data

`unzip birds.zip  > /dev/null 2>&1`

4. Download image dataset CUB_200_2011

(If it fails, retry after some delay or manually download from Google Drive)

`sh getgdrive.sh 1hbzc_P1FuxMkcabkgn9ZKinBwW683j45 CUB_200_2011.tgz`

5. Untar above download

`tar zxvf CUB_200_2011.tgz  > /dev/null 2>&1`

7. Train

`python model.py --epochs 32 --gpu 1 --topology ms`

Topology Command-line Options:

| Topology             | Command Line option  --topology |
|----------------------|---------------------------------|
| NcclAllReduce        | (default)                       |
| ReductionToOneDevice | b                               |


---

You can find training logs in /logs directory.
