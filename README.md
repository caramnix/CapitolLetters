# Capitol Letters: Detecting Differential Attitudes in Legislator Communications Using NLP

Repo contains code/figures created for my master's thesis which looked at legislator comunication through one-minute pseeches from the House floor and on Twitter. 

## Description

This repo contains code necessary for end-to-end workflow for scraping and analyzing one-minute speech data using gpt-3.5-turbo. 

First, I provide code to collect all links to C-SPAN videos which mention a given phrase, in this analysis that phrase is "one-minute" (scrape 117th one minute speeches.ipynb). I also provide the code I used to isolate just the one-minute speeches from the transcript data, since the transcripts contains other House session communication (clean_transcript_data_11*.ipynb). The result fo this cleaning can be found in the folder, One Minute Congresional Speech Data. After cleaning the transcript data the goal is to then  score these speeches for valece, arousal, confidence, empathy and smypathy. This is done using open ai's gpt-3.5-turbo (openapi_getVACES_115.ipynb). Similar scoring is done for 116th and 117th congresses. The resulting scores are availible in the VACES output directory, which has each spceech, the speaker, the party identification of the speaker as well as it's score for each VACES measure. 

The goal of this project was to explore differntial emotion by Members of Congress, so KS-testing is done on the distributions by party to determine if the distrubtions differ (ks-testing VAC_11*.ipynb). Figures of the dsitributions are also created and combined in 'make kde-figure-115-116-117.ipynb.' 


One could use this code to expand the work done here to analyze House Session transcripts on any topic. 


### Components of repo

* scraping and cleaning code
     * scrape 117th one minute speeches.ipynb, program which uses selenium to scrape the links to all CSPAN house sessions which mention one-minute as well as scraping the transcripts of those House sessions using  link to the CSPAN video. Similar collection was done for 115th and 116th Congresses. 
     * clean_transcript_data_115.ipynb, code which isolates just one-minute speeches from House session transcripts for 115th Congress
     * clean_transcript_data_116.ipynb, code which isolates just one-minute speeches from House session transcripts for 116th Congress
     * clean_transcript_data_117.ipynb, code which isolates just one-minute speeches from House session transcripts for 117th Congress
* One Minute Congresional Speech Data
      * cleaned_transcript_data_115th.csv, cleaned_transcript_data_116th.csv, cleaned_transcript_data_117th.csv resulting output from cleaning pipeline above. 
* open ai code
     * openapi_getVACES_115.ipynb, code which scores one-minute speeches using 
* VACES output
     * Contains collected one-minute speeches for 115th, 116th and 117th Congresses as well as their Valence, Arousal, Confidence, Empathy and Sympathy which was scored using OpenAI                      gpt-3.5-turbo in openapi_getVACES_115.ipynb
* figure and ks code
    * kde figures and ks testing
         * ks-testing VAC_115.ipynb, ks testing for 115th Congress and figure generation
         * ks-testing VAC_116.ipynb, ks testing for 116th Congress and figure generation
         * ks-testing VAC_117.ipynb, ks testing for 117th Congress and figure generation
         * make kde-figure-115-116-117.ipynb, combine figures into one.
     * sentiment figures
          * cleaning_and_sentiment_scoring_116.ipynb, cleans Tweets and scores sentiment for 116th Congress
          * cleaning_and_sentiment_scoring_117.ipynb, cleans Tweets and scores sentiment for 117th Congress 


## Twitter Analysis Replication

I can't provide the raw tweet data due to the Twitter Academic API usage agreement. Instead, I provide a file which contains the date of the tweet, the sentiment score of a tweet as scored by VADER, and the corresponding political party of the tweets author. This is found in the folder CapitolLetters/twitter sentiment data, tweets_115.csv, tweets_116.csv, and tweets_117.csv. This then is enough to replicate the figures found in my thesis, i.e. 

figure and ks code/sentiment figures/cleaning_and_sentiment_scoring_115.ipynb

figure and ks code/sentiment figures/cleaning_and_sentiment_scoring_116.ipynb

figure and ks code/sentiment figures/cleaning_and_sentiment_scoring_117.ipynb


## VACES Analysis Replication




## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Cara Nix, nix.39@osu.edu 

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release


## Acknowledgments

Inspiration, code snippets, etc.
* [awesome-readme](https://github.com/matiassingers/awesome-readme)

### Packages in conda enviornment w/ versions

```
absl-py                   2.1.0                    pypi_0    pypi
aiofiles                  22.1.0          py311hca03da5_0  
aiosqlite                 0.18.0          py311hca03da5_0  
annotated-types           0.6.0                    pypi_0    pypi
anyio                     3.5.0           py311hca03da5_0  
appnope                   0.1.2           py311hca03da5_1001  
argon2-cffi               21.3.0             pyhd3eb1b0_0  
argon2-cffi-bindings      21.2.0          py311h80987f9_0  
asttokens                 2.0.5              pyhd3eb1b0_0  
astunparse                1.6.3                    pypi_0    pypi
attrs                     22.1.0          py311hca03da5_0  
babel                     2.11.0          py311hca03da5_0  
backcall                  0.2.0              pyhd3eb1b0_0  
beautifulsoup4            4.12.2          py311hca03da5_0  
bleach                    4.1.0              pyhd3eb1b0_0  
blis                      0.7.11                   pypi_0    pypi
bokeh                     3.3.4                    pypi_0    pypi
brotli                    1.1.0                    pypi_0    pypi
brotlipy                  0.7.0           py311h80987f9_1002  
bzip2                     1.0.8                h620ffc9_4  
ca-certificates           2023.08.22           hca03da5_0  
cachetools                5.3.2                    pypi_0    pypi
catalogue                 2.0.10                   pypi_0    pypi
certifi                   2023.7.22       py311hca03da5_0  
cffi                      1.15.1          py311h80987f9_3  
charset-normalizer        2.0.4              pyhd3eb1b0_0  
clean-text                0.6.0                    pypi_0    pypi
cleantext                 1.1.4                    pypi_0    pypi
click                     8.1.7                    pypi_0    pypi
cloudpathlib              0.16.0                   pypi_0    pypi
cloudpickle               3.0.0                    pypi_0    pypi
colorcet                  3.0.1                    pypi_0    pypi
comm                      0.1.2           py311hca03da5_0  
confection                0.1.4                    pypi_0    pypi
contourpy                 1.2.0                    pypi_0    pypi
cryptography              41.0.3          py311hd4332d6_0  
cycler                    0.12.1                   pypi_0    pypi
cymem                     2.0.8                    pypi_0    pypi
cyrus-sasl                2.1.28               h9131b1a_1  
dask                      2024.1.1                 pypi_0    pypi
datashader                0.16.0                   pypi_0    pypi
debugpy                   1.6.7           py311h313beb8_0  
decorator                 5.1.1              pyhd3eb1b0_0  
defusedxml                0.7.1              pyhd3eb1b0_0  
emoji                     1.7.0                    pypi_0    pypi
entrypoints               0.4             py311hca03da5_0  
exceptiongroup            1.1.3                    pypi_0    pypi
executing                 0.8.3              pyhd3eb1b0_0  
ffmpeg                    1.4                      pypi_0    pypi
flatbuffers               23.5.26                  pypi_0    pypi
fonttools                 4.47.2                   pypi_0    pypi
fsspec                    2024.2.0                 pypi_0    pypi
ftfy                      6.1.3                    pypi_0    pypi
gast                      0.5.4                    pypi_0    pypi
gettext                   0.21.0               h13f89a0_1  
giflib                    5.2.1                h80987f9_3  
glib                      2.69.1               h514c7bf_2  
google-auth               2.27.0                   pypi_0    pypi
google-auth-oauthlib      1.2.0                    pypi_0    pypi
google-pasta              0.2.0                    pypi_0    pypi
grpcio                    1.60.1                   pypi_0    pypi
gst-plugins-base          1.14.1               h313beb8_1  
gstreamer                 1.14.1               h80987f9_1  
h11                       0.14.0                   pypi_0    pypi
h5py                      3.10.0                   pypi_0    pypi
holoviews                 1.18.2                   pypi_0    pypi
icu                       68.1                 hc377ac9_0  
idna                      3.4             py311hca03da5_0  
imageio                   2.33.1                   pypi_0    pypi
importlib-metadata        7.0.1                    pypi_0    pypi
ipykernel                 6.25.0          py311hb6e6a13_0  
ipython                   8.15.0          py311hca03da5_0  
ipython_genutils          0.2.0              pyhd3eb1b0_1  
ipywidgets                8.0.4           py311hca03da5_0  
jedi                      0.18.1          py311hca03da5_1  
jinja2                    3.1.2           py311hca03da5_0  
joblib                    1.3.2                    pypi_0    pypi
jpeg                      9e                   h80987f9_1  
json5                     0.9.6              pyhd3eb1b0_0  
jsonschema                4.17.3          py311hca03da5_0  
jupyter                   1.0.0           py311hca03da5_8  
jupyter_client            7.4.9           py311hca03da5_0  
jupyter_console           6.6.3           py311hca03da5_0  
jupyter_core              5.3.0           py311hca03da5_0  
jupyter_events            0.6.3           py311hca03da5_0  
jupyter_server            1.23.4          py311hca03da5_0  
jupyter_server_fileid     0.9.0           py311hca03da5_0  
jupyter_server_ydoc       0.8.0           py311hca03da5_1  
jupyter_ydoc              0.2.4           py311hca03da5_0  
jupyterlab                3.6.3           py311hca03da5_0  
jupyterlab_pygments       0.1.2                      py_0  
jupyterlab_server         2.22.0          py311hca03da5_0  
jupyterlab_widgets        3.0.5           py311hca03da5_0  
keras                     2.15.0                   pypi_0    pypi
kiwisolver                1.4.5                    pypi_0    pypi
krb5                      1.20.1               hf3e1bf2_1  
langcodes                 3.3.0                    pypi_0    pypi
lazy-loader               0.3                      pypi_0    pypi
lerc                      3.0                  hc377ac9_0  
libclang                  16.0.6                   pypi_0    pypi
libclang13                14.0.6          default_h24352ff_1  
libcxx                    14.0.6               h848a8c0_0  
libdeflate                1.17                 h80987f9_0  
libedit                   3.1.20221030         h80987f9_0  
libffi                    3.4.4                hca03da5_0  
libiconv                  1.16                 h1a28f6b_2  
libllvm14                 14.0.6               h7ec7a93_3  
libpng                    1.6.39               h80987f9_0  
libpq                     12.15                h02f6b3c_1  
libsodium                 1.0.18               h1a28f6b_0  
libtiff                   4.5.1                h313beb8_0  
libwebp                   1.3.2                ha3663a8_0  
libwebp-base              1.3.2                h80987f9_0  
libxml2                   2.10.4               h372ba2a_0  
libxslt                   1.1.37               habca612_0  
linkify-it-py             2.0.3                    pypi_0    pypi
llvm-openmp               14.0.6               hc6e5704_0  
llvmlite                  0.42.0                   pypi_0    pypi
locket                    1.0.0                    pypi_0    pypi
lxml                      4.9.3           py311h50ffb84_0  
lz4-c                     1.9.4                h313beb8_0  
markdown                  3.5.2                    pypi_0    pypi
markdown-it-py            3.0.0                    pypi_0    pypi
markupsafe                2.1.1           py311h80987f9_0  
matplotlib                3.8.2                    pypi_0    pypi
matplotlib-inline         0.1.6           py311hca03da5_0  
mdit-py-plugins           0.4.0                    pypi_0    pypi
mdurl                     0.1.2                    pypi_0    pypi
mistune                   0.8.4           py311h80987f9_1000  
ml-dtypes                 0.2.0                    pypi_0    pypi
multipledispatch          1.0.0                    pypi_0    pypi
murmurhash                1.0.10                   pypi_0    pypi
mutagen                   1.47.0                   pypi_0    pypi
mysql                     5.7.24               ha71a6ea_2  
nbclassic                 0.5.5           py311hca03da5_0  
nbclient                  0.5.13          py311hca03da5_0  
nbconvert                 6.5.4           py311hca03da5_0  
nbformat                  5.9.2           py311hca03da5_0  
ncurses                   6.4                  h313beb8_0  
nest-asyncio              1.5.6           py311hca03da5_0  
networkx                  3.2.1                    pypi_0    pypi
nltk                      3.8.1                    pypi_0    pypi
notebook                  6.5.4           py311hca03da5_1  
notebook-shim             0.2.2           py311hca03da5_0  
numba                     0.59.0                   pypi_0    pypi
numpy                     1.26.0                   pypi_0    pypi
oauthlib                  3.2.2                    pypi_0    pypi
openssl                   3.0.10               h1a28f6b_2  
opt-einsum                3.3.0                    pypi_0    pypi
outcome                   1.2.0                    pypi_0    pypi
packaging                 23.1            py311hca03da5_0  
pandas                    2.1.0                    pypi_0    pypi
pandocfilters             1.5.0              pyhd3eb1b0_0  
panel                     1.3.8                    pypi_0    pypi
param                     2.0.2                    pypi_0    pypi
parso                     0.8.3              pyhd3eb1b0_0  
partd                     1.4.1                    pypi_0    pypi
pcre                      8.45                 hc377ac9_0  
pexpect                   4.8.0              pyhd3eb1b0_3  
pickleshare               0.7.5           pyhd3eb1b0_1003  
pillow                    10.2.0                   pypi_0    pypi
pip                       23.2.1          py311hca03da5_0  
platformdirs              3.10.0          py311hca03da5_0  
ply                       3.11            py311hca03da5_0  
preshed                   3.0.9                    pypi_0    pypi
prometheus_client         0.14.1          py311hca03da5_0  
prompt-toolkit            3.0.36          py311hca03da5_0  
prompt_toolkit            3.0.36               hd3eb1b0_0  
protobuf                  4.23.4                   pypi_0    pypi
psutil                    5.9.0           py311h80987f9_0  
ptyprocess                0.7.0              pyhd3eb1b0_2  
pure_eval                 0.2.2              pyhd3eb1b0_0  
pyasn1                    0.5.1                    pypi_0    pypi
pyasn1-modules            0.3.0                    pypi_0    pypi
pycparser                 2.21               pyhd3eb1b0_0  
pycryptodomex             3.19.0                   pypi_0    pypi
pyct                      0.5.0                    pypi_0    pypi
pydantic                  2.5.3                    pypi_0    pypi
pydantic-core             2.14.6                   pypi_0    pypi
pygments                  2.15.1          py311hca03da5_1  
pynndescent               0.5.11                   pypi_0    pypi
pyopenssl                 23.2.0          py311hca03da5_0  
pyparsing                 3.1.1                    pypi_0    pypi
pyqt                      5.15.7          py311h313beb8_0  
pyqt5-sip                 12.11.0         py311h313beb8_0  
pyrsistent                0.18.0          py311h80987f9_0  
pysocks                   1.7.1           py311hca03da5_0  
python                    3.11.5               hb885b13_0  
python-dateutil           2.8.2              pyhd3eb1b0_0  
python-fastjsonschema     2.16.2          py311hca03da5_0  
python-json-logger        2.0.7           py311hca03da5_0  
pytz                      2023.3.post1    py311hca03da5_0  
pyviz-comms               3.0.1                    pypi_0    pypi
pyyaml                    6.0             py311h80987f9_1  
pyzmq                     23.2.0          py311h313beb8_0  
qt-main                   5.15.2               h9b4df51_9  
qt-webengine              5.15.9               h2903aaf_7  
qtconsole                 5.4.2           py311hca03da5_0  
qtpy                      2.2.0           py311hca03da5_0  
qtwebkit                  5.212                h19f419d_5  
readline                  8.2                  h1a28f6b_0  
regex                     2023.12.25               pypi_0    pypi
requests                  2.31.0          py311hca03da5_0  
requests-oauthlib         1.3.1                    pypi_0    pypi
rfc3339-validator         0.1.4           py311hca03da5_0  
rfc3986-validator         0.1.1           py311hca03da5_0  
rsa                       4.9                      pypi_0    pypi
scikit-image              0.22.0                   pypi_0    pypi
scikit-learn              1.4.0                    pypi_0    pypi
scipy                     1.12.0                   pypi_0    pypi
seaborn                   0.13.1                   pypi_0    pypi
selenium                  4.12.0                   pypi_0    pypi
send2trash                1.8.0              pyhd3eb1b0_1  
setuptools                68.0.0          py311hca03da5_0  
sip                       6.6.2           py311h313beb8_0  
six                       1.16.0             pyhd3eb1b0_1  
smart-open                6.4.0                    pypi_0    pypi
sniffio                   1.2.0           py311hca03da5_1  
sortedcontainers          2.4.0                    pypi_0    pypi
soupsieve                 2.4             py311hca03da5_0  
spacy                     3.7.2                    pypi_0    pypi
spacy-legacy              3.0.12                   pypi_0    pypi
spacy-loggers             1.0.5                    pypi_0    pypi
sqlite                    3.41.2               h80987f9_0  
srsly                     2.4.8                    pypi_0    pypi
stack_data                0.2.0              pyhd3eb1b0_0  
tensorboard               2.15.1                   pypi_0    pypi
tensorboard-data-server   0.7.2                    pypi_0    pypi
tensorflow                2.15.0                   pypi_0    pypi
tensorflow-estimator      2.15.0                   pypi_0    pypi
tensorflow-hub            0.16.1                   pypi_0    pypi
tensorflow-io-gcs-filesystem 0.36.0                   pypi_0    pypi
tensorflow-macos          2.15.0                   pypi_0    pypi
termcolor                 2.4.0                    pypi_0    pypi
terminado                 0.17.1          py311hca03da5_0  
tf-keras                  2.15.0                   pypi_0    pypi
thinc                     8.2.2                    pypi_0    pypi
threadpoolctl             3.2.0                    pypi_0    pypi
tifffile                  2024.1.30                pypi_0    pypi
tinycss2                  1.2.1           py311hca03da5_0  
tk                        8.6.12               hb8d0fd4_0  
toml                      0.10.2             pyhd3eb1b0_0  
toolz                     0.12.1                   pypi_0    pypi
tornado                   6.3.2           py311h80987f9_0  
tqdm                      4.66.1                   pypi_0    pypi
traitlets                 5.7.1           py311hca03da5_0  
trio                      0.22.2                   pypi_0    pypi
trio-websocket            0.10.4                   pypi_0    pypi
typer                     0.9.0                    pypi_0    pypi
typing-extensions         4.7.1           py311hca03da5_0  
typing_extensions         4.7.1           py311hca03da5_0  
tzdata                    2023.3                   pypi_0    pypi
uc-micro-py               1.0.2                    pypi_0    pypi
umap                      0.1.1                    pypi_0    pypi
umap-learn                0.5.5                    pypi_0    pypi
undetected-chromedriver   3.5.3                    pypi_0    pypi
urllib3                   1.26.16         py311hca03da5_0  
vadersentiment            3.3.2                    pypi_0    pypi
vectorizers               0.2                      pypi_0    pypi
wasabi                    1.1.2                    pypi_0    pypi
wcwidth                   0.2.13                   pypi_0    pypi
weasel                    0.3.4                    pypi_0    pypi
webencodings              0.5.1           py311hca03da5_1  
websocket-client          0.58.0          py311hca03da5_4  
websockets                11.0.3                   pypi_0    pypi
werkzeug                  3.0.1                    pypi_0    pypi
wheel                     0.38.4          py311hca03da5_0  
widgetsnbextension        4.0.5           py311hca03da5_0  
wrapt                     1.14.1                   pypi_0    pypi
wsproto                   1.2.0                    pypi_0    pypi
xarray                    2024.1.1                 pypi_0    pypi
xyzservices               2023.10.1                pypi_0    pypi
xz                        5.4.2                h80987f9_0  
y-py                      0.5.9           py311ha6e5c4f_0  
yaml                      0.2.5                h1a28f6b_0  
youtube-dl                2021.12.17               pypi_0    pypi
ypy-websocket             0.8.2           py311hca03da5_0  
yt-dlp                    2023.10.7                pypi_0    pypi
zeromq                    4.3.4                hc377ac9_0  
zipp                      3.17.0                   pypi_0    pypi
zlib                      1.2.13               h5a0b063_0  
zstd                      1.5.5                hd90d995_0  
```

