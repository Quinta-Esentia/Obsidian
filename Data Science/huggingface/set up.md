
1. Create Conda Env
In anaconda prompt
`conda create -n ml python=3.10`
`conda activate ml`

2. Install pytorch
https://pytorch.org/get-started/locally/
`conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia`

3. Install huggingface transformers
`conda install -c huggingface transformers`

4. Install pandas and numpy
`conda install pandas numpy`

5. Install requests
`conda install requests`


## Troubleshooting

1. When trying to load AutoTokenizer or Model, got error:
   `requests.exceptions.SSLError: HTTPSConnectionPool(host='huggingface.co', port=443): Max retries exceeded with url: /distilbert-base-uncased/resolve/main/vocab.txt (Caused by SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self signed certificate in certificate chain (_ssl.c:1007)')))`

Solution (not idea?)
https://stackoverflow.com/questions/75110981/sslerror-httpsconnectionpoolhost-huggingface-co-port-443-max-retries-exce

https://stackoverflow.com/questions/71692354/facing-ssl-error-with-huggingface-pretrained-models

1. `conda install requests==2.27.1`
2. ```python
	import os
	os.environ['CURL_CA_BUNDLE'] = ''



# Saved models
location:
C:\Users\Dexter.Camison\.cache\huggingface\hub
C:\Users\Dexter.Camison\.cache\huggingface\hub