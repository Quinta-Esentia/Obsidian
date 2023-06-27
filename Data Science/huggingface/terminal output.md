```
PS C:\Users\Dexter.Camison> C:/Users/Dexter.Camison/Anaconda3/Scripts/activate
PS C:\Users\Dexter.Camison> conda activate ml

CommandNotFoundError: Your shell has not been properly configured to use 'conda activate'.
If using 'conda activate' from a batch script, change your
invocation to 'CALL conda.bat activate'.


    $ conda init <SHELL_NAME>

Currently supported shells are:
  - bash
  - cmd.exe
  - fish
  - tcsh
  - xonsh
  - zsh
  - powershell

See 'conda init --help' for more information and options.

IMPORTANT: You may need to close and restart your shell after running 'conda init'.


PS C:\Users\Dexter.Camison> & C:/Users/Dexter.Camison/Anaconda3/envs/ml/python.exe
Python 3.10.11 | packaged by Anaconda, Inc. | (main, Apr 20 2023, 18:56:50) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import torch
>>> from transformers import  AutoTokenizer, AutoModelForSequenceClassification
>>> from transformers import  AutoTokenizer, AutoModelForSequenceClassification
>>>
>>> tokenizer = AutoTokenizer.from_pretrained("distilbert-base-uncased-finetuned-sst-2-english")
Traceback (most recent call last):
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py", line 703, in urlopen
    httplib_response = self._make_request(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py", line 386, in _make_request
    self._validate_conn(conn)
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py", line 1042, in _validate_conn
    conn.connect()
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connection.py", line 419, in connect
    self.sock = ssl_wrap_socket(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\util\ssl_.py", line 449, in ssl_wrap_socket
    ssl_sock = _ssl_wrap_socket_impl(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\util\ssl_.py", line 493, in _ssl_wrap_socket_impl
    return ssl_context.wrap_socket(sock, server_hostname=server_hostname)
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\ssl.py", line 513, in wrap_socket
    return self.sslsocket_class._create(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\ssl.py", line 1071, in _create
    self.do_handshake()
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\ssl.py", line 1342, in do_handshake
    self._sslobj.do_handshake()
ssl.SSLCertVerificationError: [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self signed certificate in certificate chain (_ssl.c:1007)

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\requests\adapters.py", line 440, in send
    resp = conn.urlopen(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py", line 787, in urlopen
    retries = retries.increment(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\util\retry.py", line 592, in increment
    raise MaxRetryError(_pool, url, error or ResponseError(cause))
urllib3.exceptions.MaxRetryError: HTTPSConnectionPool(host='huggingface.co', port=443): Max retries exceeded with url: /distilbert-base-uncased-finetuned-sst-2-english/resolve/main/tokenizer_config.json (Caused by SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self signed certificate in certificate chain (_ssl.c:1007)')))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\transformers\models\auto\tokenization_auto.py", line 642, in from_pretrained
    tokenizer_config = get_tokenizer_config(pretrained_model_name_or_path, **kwargs)
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\transformers\models\auto\tokenization_auto.py", line 486, in get_tokenizer_config
    resolved_config_file = cached_file(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\transformers\utils\hub.py", line 409, in cached_file
    resolved_file = hf_hub_download(
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\utils\_validators.py", line 120, in _inner_fn
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\file_download.py", line 1195, in hf_hub_download
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\utils\_validators.py", line 120, in _inner_fn
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\file_download.py", line 1532, in get_hf_file_metadata
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\file_download.py", line 407, in _request_wrapper
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\file_download.py", line 442, in _request_wrapper
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\utils\_http.py", line 212, in http_backoff
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\requests\sessions.py", line 529, in request
    resp = self.send(prep, **send_kwargs)
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\requests\sessions.py", line 645, in send
    r = adapter.send(request, **kwargs)
  File "C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\requests\adapters.py", line 517, in send
    raise SSLError(e, request=request)
requests.exceptions.SSLError: HTTPSConnectionPool(host='huggingface.co', port=443): Max retries exceeded with url: /distilbert-base-uncased-finetuned-sst-2-english/resolve/main/tokenizer_config.json (Caused by SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self signed certificate in certificate chain (_ssl.c:1007)')))
>>> '''This following code will set the CURL_CA_BUNDLE environment variable to an empty string in the Python os module'''
'This following code will set the CURL_CA_BUNDLE environment variable to an empty string in the Python os module'
>>> import os
>>> os.environ['CURL_CA_BUNDLE'] = ''
>>> tokenizer = AutoTokenizer.from_pretrained("distilbert-base-uncased-finetuned-sst-2-english")
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
Downloading (…)okenizer_config.json: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 48.0/48.0 [00:00<?, ?B/s]
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\huggingface_hub-0.14.1-py3.8.egg\huggingface_hub\file_download.py:133: UserWarning: `huggingface_hub` cache-system uses symlinks by default to efficiently store duplicated files but your machine does not support them in C:\Users\Dexter.Camison\.cache\huggingface\hub. Caching files will still work but in a degraded version that might require more space on your disk. This warning can be disabled by setting the `HF_HUB_DISABLE_SYMLINKS_WARNING` environment variable. For more details, see https://huggingface.co/docs/huggingface_hub/how-to-cache#limitations.
To support symlinks on Windows, you either need to activate Developer Mode or to run Python as an administrator. In order to see activate developer mode, see this article: https://docs.microsoft.com/en-us/windows/apps/get-started/enable-your-device-for-development
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
Downloading (…)lve/main/config.json: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 629/629 [00:00<?, ?B/s]
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
Downloading (…)solve/main/vocab.txt: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 232k/232k [00:00<00:00, 3.35MB/s]
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
>>> model = AutoModelForSequenceClassification.from_pretrained("distilbert-base-uncased-finetuned-sst-2-english")
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'huggingface.co'. Adding certificate verification 
is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
C:\Users\Dexter.Camison\Anaconda3\envs\ml\lib\site-packages\urllib3\connectionpool.py:1045: InsecureRequestWarning: Unverified HTTPS request is being made to host 'cdn-lfs.huggingface.co'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/1.26.x/advanced-usage.html#ssl-warnings
  warnings.warn(
Downloading pytorch_model.bin: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 268M/268M [01:27<00:00, 3.07MB/s]
>>> inputs = tokenizer("Hello, my dog is cute", return_tensors="pt")
>>> with torch.no_grad():
...     logits = model(**inputs).logits
...
>>> predicted_class_id = logits.argmax().item()
>>> model.config.id2label[predicted_class_id]
'POSITIVE'
>>> ens = tokenizer.encode('It was good but couldve been better. Great', return_tensors='pt')
>>> result = model(tokens)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'tokens' is not defined
>>> int(torch.argmax(result.logits))+1
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'result' is not defined
>>> tokens = tokenizer.encode('It was good but couldve been better. Great', return_tensors='pt')
>>> result = model(tokens)
>>> int(torch.argmax(result.logits))+1
2
>>> pred_class = int(torch.argmax(result.logits))+1
>>> model.config.id2label[pred_class]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 2
>>> predicted_class_id
1
>>> pred_class = int(torch.argmax(result.logits))
>>> model.config.id2label[pred_class]
'POSITIVE'
>>> inputs = tokenizer("Hello, my dog is cute", return_tensors="pt")
>>> with torch.no_grad():
...     logits = model(**inputs).logits
...
>>> predicted_class_id = logits.argmax().item()
>>> model.config.id2label[predicted_class_id]
'POSITIVE'
>>> # Method 2
>>>
>>> tokens = tokenizer.encode('It was good but couldve been better. Great', return_tensors='pt')
>>> result = model(tokens)
>>> pred_class = int(torch.argmax(result.logits))
>>> model.config.id2label[pred_class]
'POSITIVE'
>>> result
SequenceClassifierOutput(loss=None, logits=tensor([[-2.0474,  2.2883]], grad_fn=<AddmmBackward0>), hidden_states=None, attentions=None)
>>> logits
tensor([[-4.0687,  4.3669]])
>>> predicted_class_id
1
>>> cls
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'cls' is not defined
>>> clr
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'clr' is not defined. Did you mean: 'chr'?
>>> clear
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'clear' is not defined
>>> cls
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'cls' is not defined
>>>
KeyboardInterrupt
>>> logits
tensor([[-4.0687,  4.3669]])
>>> result
SequenceClassifierOutput(loss=None, logits=tensor([[-2.0474,  2.2883]], grad_fn=<AddmmBackward0>), hidden_states=None, attentions=None)
>>> pred_class
1
>>> inputs = tokenizer("Hello, my dog is cute", return_tensors="pt")
>>> with torch.no_grad():
...     logits = model(**inputs).logits
...
>>> predicted_class_id = logits.argmax().item()
>>> model.config.id2label[predicted_class_id]
'POSITIVE'
>>> # Method 2
>>>
>>> tokens = tokenizer.encode('It was good but couldve been better. Great', return_tensors='pt')
>>> result = model(tokens)
>>> pred_class = int(torch.argmax(result.logits))
>>> model.config.id2label[pred_class]
'POSITIVE'
>>> inputs = tokenizer("Hello, my dog is not cute", return_tensors="pt")
>>> with torch.no_grad():
...     logits = model(**inputs).logits
...
>>> predicted_class_id = logits.argmax().item()
>>> model.config.id2label[predicted_class_id]
'NEGATIVE'
>>> # Method 2
>>>
>>> tokens = tokenizer.encode('It was good but couldve been better. Great', return_tensors='pt')
>>> result = model(tokens)
>>> pred_class = int(torch.argmax(result.logits))
>>> model.config.id2label[pred_class]
'POSITIVE'
>>> predicted_class_id
0
>>> logits
tensor([[ 4.2309, -3.4007]])
>>> inputs = tokenizer("this company sucks, my boss is awesome but the leaders aren't.", return_tensors="pt")
>>> with torch.no_grad():
...     logits = model(**inputs).logits
...
>>> predicted_class_id = logits.argmax().item()
>>> model.config.id2label[predicted_class_id]
'NEGATIVE'
>>> logits
tensor([[ 1.6761, -1.4751]])
>>> inputs = tokenizer("this company is okay, my boss is awesome but the leaders aren't.", return_tensors="pt")
>>> inputs = tokenizer("this company is okay, my boss is awesome but the leaders aren't.", return_tensors="pt")
>>> with torch.no_grad():
...     logits = model(**inputs).logits
...
>>> logits
tensor([[ 0.7857, -0.6756]])
>>> predicted_class_id = logits.argmax().item()
>>> model.config.id2label[predicted_class_id]
'NEGATIVE'
>>> inputs = tokenizer("this company is okay, my boss is awesome but the leaders aren't so good", return_tensors="pt")
>>> with torch.no_grad():
...     logits = model(**inputs).logits
...
>>> predicted_class_id = logits.argmax().item()
>>> model.config.id2label[predicted_class_id]
'NEGATIVE'
>>> predicted_class_id
0
>>> logits.argmax()
tensor(0)
>>> logits
tensor([[ 2.7704, -2.3779]])
>>>  
```