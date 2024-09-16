# Master thesis: Comparison of the scholarly impact of CLEF and TREC
**Information**

- First examiner: Prof. Dr. Philipp Schaer
- Second examiner: Dr. Timo Breuer  

- Student: Andreas Kruff

Title:
  
```
Comparison of the scholarly impact of CLEF and TREC
```
 
**Keywords:** TREC, CLEF, scientometric analysis, scholarly impact, bibliometry


## Overview

The repository contains the following folders:

- **code:** Contains the separated folders which contain the code for the data acquisition and the analysis
- **data:** Contains the necessary data that were gathered for this analysis. PDF files and transformed XML files are not included
- **images:** Contains the images, that were created for the analysis of the scholarly impact of the two campaigns

In order to overcome the Github file size restrictions some files were compressed as .zip files and need to be decompressed first. This includes:

- data/OpenAlex_CEUR_citing_doc.json
- data/OpenAlex_LNCS_citing_doc.json
- data/OpenAlex_TREC_citing_doc.json
- data/SemanticScholar_CEUR_additional_metadata.json
- data/author_metadata.json


## Setup the Environment:

For creating the necessary environment to be able to use this Repository a requirements.txt is provided to install the necessary libararies in your environment 

For installing the dependencies use:

```shell 

pip install -r requirements.txt

```

## Setup GROBID:

For pulling the docker image of GROBID you could either pull the complete model (Deep Learning and CRF image):

```shell 

docker pull grobid/grobid:${latest_grobid_version}

```

Or the smaller model (CRF Image):

```shell 

docker pull lfoppiano/grobid:${latest_grobid_version}

```

Latest version is currently 0.8.0 for both.


To run the docker image you could use

```shell 

docker run --rm --gpus all --init --ulimit core=0 -p 8080:8070 grobid/grobid:${latest_grobid_version}

```

or 

```shell 

docker run --rm --init --ulimit core=0 -p 8070:8070 lfoppiano/grobid:${latest_grobid_version}

```

For more informations regarding GROBID visit the [documentation](https://grobid.readthedocs.io/en/latest/) or the [Github Repository](https://github.com/kermitt2/grobid).


For the usage of the ollama Llama3 LLM follow the instructions on the official [website](https://ollama.com/).

For acquiring the PDF's yourself you can use the iniative websites for TREC under [Publications](https://trec.nist.gov/proceedings/proceedings.html) or the [CLEF website](https://www.clef-initiative.eu/) in order to use the further links.

