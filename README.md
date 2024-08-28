Ce repository est constitué de différents document constitue un travail sur le fine-tuning de données :

  - Les premiers fichiers sont sur le fine-tuning des dialogues entre médecins et patients (les fichiers numérotés de 1 à 5). Ces fichiers doivent être exécutés dans l'ordre afin d'obtenir à la fin un modèle fine-tuné.
  - Les seconds fichiers portent  sur le fine-tuning de résumés d'articles (summarization.ipynb).
Le fichier "GGUF" a été ajouté pour réaliser la conversion d'un modèle Huggingface en fichier GGUF, indispensable pour le faire ensuite tourner sur des applications comme JAN ou encore LM Studio.

  - Les derniers fichiers traitent la version sur les Rags. Le "rag-langchain-llama-3" constitue un RAG qui peut être utilisé avec nos modèles fine-tunés enregistrés sur Huggingface ou bien sur des modèles déjà existants comme LLaMA 3. Il y a aussi un RAG basé sur DSPY et non Langchain comme celui mentionné précédemment. Nous pouvons aussi nous appuyer sur les codes fournis dans la présentation de GitHub de DSPY sur le lien suivant : https://github.com/stanfordnlp/dspy?tab=readme-ov-file#2-documentation. 

Le fonctionnement de tous ces codes nécessite la création d'un compte sur Huggingface mais aussi d'un compte sur W&B (Weights & Biases) pour le suivi du fine-tuning.

Voici l'ensemble des librairies qui ont été utiles à l'exécution des codes situés dans le repo GGUF, mais également ceux du repo détection d'image et du rag ikki : 
absl-py==2.1.0
accelerate==0.33.0
aiohttp==3.9.5
aiosignal==1.2.0
albumentations==1.4.7
alembic==1.13.2
annotated-types==0.6.0
anthropic==0.26.1
anyio==4.3.0
appnope==0.1.2
argon2-cffi-bindings==21.2.0
argon2-cffi==23.1.0
arrow==1.3.0
asttokens==2.0.5
async-lru==2.0.4
attrs==23.1.0
authlib==1.3.1
babel==2.15.0
backoff==2.2.1
beautifulsoup4==4.12.3
bitsandbytes==0.42.0
bleach==6.1.0
blinker==1.6.2
brotli==1.0.9
build==1.2.1
cachetools==5.3.3
certifi==2024.2.2
cffi==1.16.0
chardet==5.2.0
charset-normalizer==3.3.2
click==8.1.7
colorlog==6.8.2
comm==0.2.1
contourpy==1.2.1
cryptography==42.0.5
cycler==0.12.1
cython==3.0.10
dataclasses-json==0.6.7
datasets==2.21.0
debugpy==1.6.7
decorator==5.1.1
defusedxml==0.7.1
deprecated==1.2.14
dill==0.3.7
dirtyjson==1.0.8
distro==1.9.0
docker-pycreds==0.4.0
docstring-parser==0.16
dspy-ai==2.1.9
dspy==0.1.5
einops==0.8.0
evaluate==0.4.1
executing==0.8.3
fastjsonschema==2.19.1
filelock==3.14.0
fonttools==4.51.0
fqdn==1.5.1
frozenlist==1.4.0
fsspec==2023.10.0
gitdb==4.0.11
gitpython==3.1.43
google-ai-generativelanguage==0.6.4
google-api-core==2.19.1
google-api-python-client==2.131.0
google-auth-httplib2==0.2.0
google-auth-oauthlib==0.5.2
google-auth==2.29.0
google-cloud-core==2.4.1
google-generativeai==0.5.4
googleapis-common-protos==1.63.0
greenlet==3.0.3
grpcio-health-checking==1.64.1
grpcio-status==1.62.2
grpcio-tools==1.64.1
grpcio==1.48.2
h11==0.14.0
h5py==3.11.0
httpcore==1.0.5
httplib2==0.22.0
httpx==0.27.0
huggingface-hub==0.23.0
idna==3.7
imageio==2.34.1
ipykernel==6.28.0
ipython==8.20.0
ipywidgets==8.1.2
isoduration==20.11.0
jedi==0.18.1
jinja2==3.1.4
jiter==0.4.0
joblib==1.3.2
json5==0.9.25
jsonpatch==1.33
jsonpointer==2.4
jsonschema-specifications==2023.12.1
jsonschema==4.22.0
jupyter-client==8.6.0
jupyter-core==5.5.0
jupyter-events==0.10.0
jupyter-lsp==2.2.5
jupyter-server-terminals==0.5.3
jupyter-server==2.14.0
jupyterlab-pygments==0.3.0
jupyterlab-server==2.27.1
jupyterlab-widgets==3.0.10
jupyterlab==4.1.8
kagglehub==0.2.7
keras-nlp==0.14.0
keras==3.4.1
kiwisolver==1.4.5
langchain-anthropic==0.1.13
langchain-core==0.2.1
langchain-google-genai==1.0.5
langchain-openai==0.1.7
langchain-text-splitters==0.2.0
langchain==0.2.1
langsmith==0.1.63
lazy-loader==0.4
lightning-utilities==0.11.2
linear==0.0.dev0
llama-cloud==0.0.9
llama-index-agent-openai==0.2.8
llama-index-cli==0.1.12
llama-index-core==0.10.55
llama-index-embeddings-huggingface==0.2.2
llama-index-embeddings-openai==0.1.10
llama-index-indices-managed-llama-cloud==0.2.5
llama-index-legacy==0.9.48
llama-index-llms-openai==0.1.25
llama-index-multi-modal-llms-openai==0.1.7
llama-index-program-openai==0.1.6
llama-index-question-gen-openai==0.1.3
llama-index-readers-file==0.1.30
llama-index-readers-llama-parse==0.1.6
llama-index-vector-stores-weaviate==1.0.1
llama-index==0.10.55
llama-parse==0.4.6
mako==1.3.5
markdown-it-py==3.0.0
markdown==3.4.1
markupsafe==2.1.3
marshmallow==3.21.3
matplotlib-inline==0.1.6
matplotlib==3.8.4
mdurl==0.1.2
minijinja==2.0.1
mistune==3.0.2
ml-dtypes==0.4.0
mpmath==1.3.0
multidict==6.0.4
multiprocess==0.70.15
munkres==1.1.4
mypy-extensions==1.0.0
namex==0.0.8
nbclient==0.10.0
nbconvert==7.16.4
nbformat==5.10.4
nest-asyncio==1.6.0
networkx==3.3
ninja==1.11.1.1
nltk==3.8.1
notebook-shim==0.2.4
notebook==7.1.3
numpy==1.26.4
oauthlib==3.2.2
openai==1.35.13
opencv-python-headless==4.9.0.80
opencv-python==4.9.0.80
optim==0.1.0
optree==0.12.1
optuna==3.4.0
orjson==3.10.3
overrides==7.7.0
packaging==23.2
pandas==2.1.4
pandocfilters==1.5.1
parsimonious==0.10.0
parso==0.8.3
peft==0.12.0
pexpect==4.8.0
pickleshare==0.7.5
pillow==10.3.0
pip==24.1.2
platformdirs==3.10.0
prometheus-client==0.20.0
prompt-toolkit==3.0.43
proto-plus==1.23.0
protobuf==5.27.2
psutil==5.9.0
ptyprocess==0.7.0
pure-eval==0.2.2
pyarrow-hotfix==0.6
pyarrow==16.1.0
pyasn1-modules==0.2.8
pyasn1==0.4.8
pycocotools==2.0.6
pycparser==2.21
pydantic-core==2.14.1
pydantic==2.5.0
pygments==2.15.1
pyjwt==2.8.0
pyopenssl==24.0.0
pyparsing==3.0.9
pypdf==4.2.0
pyproject-hooks==1.1.0
pysocks==1.7.1
python-dateutil==2.9.0.post0
python-json-logger==2.0.7
pytorch-lightning==2.2.5
pytz==2024.1
pyyaml==6.0.1
pyzmq==25.1.2
referencing==0.35.1
regex==2023.10.3
requests-oauthlib==1.3.0
requests==2.32.3
responses==0.18.0
rfc3339-validator==0.1.4
rfc3986-validator==0.1.1
rich==13.7.1
rouge-score==0.1.2
rpds-py==0.18.1
rsa==4.7.2
safetensors==0.4.3
scikit-image==0.23.2
scikit-learn==1.4.2
scipy==1.13.0
send2trash==1.8.3
sentence-transformers==3.0.1
sentencepiece==0.2.0
sentry-sdk==2.13.0
setproctitle==1.3.3
setuptools==69.5.1
shtab==1.7.1
singlestoredb==1.3.1
six==1.16.0
smmap==5.0.1
sniffio==1.3.1
soupsieve==2.5
sqlalchemy==2.0.30
sqlparams==6.0.1
stack-data==0.2.0
striprtf==0.0.26
structlog==24.2.0
sympy==1.12
tenacity==8.3.0
tensorboard-data-server==0.7.0
tensorboard-plugin-wit==1.8.1
tensorboard==2.12.1
terminado==0.18.1
threadpoolctl==3.5.0
tifffile==2024.5.10
tiktoken==0.7.0
timm==1.0.3
tinycss2==1.3.0
tokenizers==0.19.1
torch==2.3.0
torchaudio==2.3.0
torchmetrics==1.4.0.post0
torchvision==0.18.0
tornado==6.3.3
tqdm==4.66.4
traitlets==5.14.3
transformers==4.41.2
trl==0.9.6
types-python-dateutil==2.9.0.20240316
typing-extensions==4.12.0
typing-inspect==0.9.0
tyro==0.8.4
tzdata==2024.1
ujson==5.8.0
uri-template==1.3.0
uritemplate==4.1.1
urllib3==2.2.1
validators==0.28.3
wandb==0.17.7
wcwidth==0.2.13
weaviate-client==4.6.5
webcolors==1.13
webencodings==0.5.1
websocket-client==1.8.0
werkzeug==3.0.3
wheel==0.43.0
widgetsnbextension==4.0.10
wrapt==1.16.0
xxhash==3.4.1
yarl==1.9.3
