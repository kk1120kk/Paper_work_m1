# Paper_work_m1  

## `Tutorial`: data prepare, inference with pretrained models, and metric computation.


### 1), Download data  
  Download the SVD dataset in [here](https://zenodo.org/records/16874898). Or download SVD at [here](https://stimmdb.coli.uni-saarland.de/)  
  Download the Perceptual Voice Qualities Database (PVQD) in [here](https://data.mendeley.com/datasets/9dz247gnyb/4).  
  Alternatively, download our prepared demo datasets for initial testing.[SVD deomo](https://1drv.ms/u/c/c358f1155eb8fb7f/IQDZYbwfDd8aQa7jy9wwbVdZAWhkvatS5m6048bGtx2-FTc?e=KpA0eE) and [PVQD deomo](https://1drv.ms/u/c/c358f1155eb8fb7f/IQC-dO-LXDW7Ro8BTCu0DAPgAc_-L4EG97zash7ElppNMMI?e=t2xTGc)  
  Alternatively, download our pre-processed data to run full inference.[full SVD processed data](https://1drv.ms/u/c/c358f1155eb8fb7f/IQD6fhILg-snQ4PXjW-Au6LlAaIm0BlTaIdBAzdw-qCgWoE?e=Gm1RTO) and [full PVQD processed data](https://1drv.ms/u/c/c358f1155eb8fb7f/IQDUuoKCIq1USLbZ4Ea68zrzASDJel6r2OWCouGQlj0N3hc?e=NHMQTb)

### 2), Prepare data  
  `For the SVD dataset`, place all pathological voices in SVD into one path, ensuring that they have a sampling rate of 16k and a .wav suffix.  
  `For the PVQD dataset`, according to the annotations in "Demographics.xlsx", the pathological speech was selected. Each original speech contains six sentence readings and several vowel pronunciations, and each sentence reading was edited out using Adobe Audition. And ensuring that they have a sampling rate of 16k and a .wav suffix.  

### 3), Use conda to build an environment  
```
conda create -n PVC python=3.10
conda activate PVC

pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126
pip3 install transformers
pip3 install librosa
pip install coqui-tts==0.25.3
pip insatll datasets
pip install torchcodec
```
### 4), Download pretrained models.  
Download whisper-large-v3 in huggingface:   
```
hf download openai/whisper-large-v3 --local-dir ./pretrain_models/openai/whisper-large-v3 
```
Or, download it manually via [Huggingface website](https://huggingface.co/openai/whisper-large-v3). And put all files in "./pretrain_models/openai/whisper-large-v3 "  
If you are unable to connect to Hugging Face, try the following command:
```
export HF_ENDPOINT=https://hf-mirror.com
```
