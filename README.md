# PractDLSysPerformanceProject



## Steps:

1. Requirements

`pip install -r requirements.txt`

2. 

`sh getgdrive.sh 0B3y_msrWZaXLT1BZdVdycDY5TEE birds.zip`

3. 

`unzip birds.zip  > /dev/null 2>&1`

4.

`sh getgdrive.sh 1hbzc_P1FuxMkcabkgn9ZKinBwW683j45 CUB_200_2011.tgz`

5.
`tar zxvf CUB_200_2011.tgz  > /dev/null 2>&1`

6.

`python model.py`

7. Train

`python model.py --epochs 32 --gpu 1 --topology ms`


Topology Options:

| Topology             | Command Line option  --topology |
|----------------------|---------------------------------|
| MirroredStrategy     | ms                              |
| NcclAllReduce        | ar                              |
| ReductionToOneDevice | b                               |