# Paper_work_m1


1), Download data  
  Download the SVD pathological speech dataset in [here](https://zenodo.org/records/16874898). Or download SVD at [here](https://stimmdb.coli.uni-saarland.de/)  
  Download the Perceptual Voice Qualities Database (PVQD) in [here](https://data.mendeley.com/datasets/9dz247gnyb/4).  
  Alternatively, download our prepared demo datasets for initial testing.  
  [SVD deomo OneDrive link](https://1drv.ms/u/c/c358f1155eb8fb7f/IQDZYbwfDd8aQa7jy9wwbVdZAWhkvatS5m6048bGtx2-FTc?e=KpA0eE) and [PVQD deomo OneDrive link](https://1drv.ms/u/c/c358f1155eb8fb7f/IQC-dO-LXDW7Ro8BTCu0DAPgAc_-L4EG97zash7ElppNMMI?e=t2xTGc)

2), Prepare data  
  For the `SVD` dataset, place all pathological voices in SVD into one path, ensuring that they have a sampling rate of 16k and a .wav suffix.  
    
  For the `PVQD` dataset, according to the annotations in "Demographics.xlsx", the pathological speech was selected. Each original speech contains six sentence readings and several vowel pronunciations, and each sentence reading was edited out using Adobe Audition. And ensuring that they have a sampling rate of 16k and a .wav suffix.  

3), Use conda to build an environment  
```
conda create -n PVC python=3.10
```

