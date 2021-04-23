# Practical Deep Learning System Performance Project

Distributed Training implementation of StackGAN

Submission By:

1. Feroz Ahmad (fa2581)
2. Li Cai (lc2928)

# About the project

Objective: 

To analyze and compare training speed while training StackGAN on single and multiple GPUs (2, 4, 8) on a single node instance. We intend to
study the percentage increase in speed up with increase in batch size, scaling efficiency and communication overhead with increase in GPU count.


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

6. Create logs folder

`mkdir logs`

7. Train

`python model.py --epochs 32 --gpu 1 --topology ms`

Topology Command-line Options:

| Topology             | Command Line option  --topology |
|----------------------|---------------------------------|
| NcclAllReduce        | (default)                       |
| ReductionToOneDevice | b                               |


---

You can find training logs in /logs directory.
