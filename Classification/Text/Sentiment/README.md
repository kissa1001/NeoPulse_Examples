# Introduction
These sample .nml files are for training a classification model using Text data in [NeoPulse™ AI Studio](https://aws.amazon.com/marketplace/pp/B074NDG36S/ref=vdr_rf).

# Data
The data for this task can be found at: http://ai.stanford.edu/~amaas/data/sentiment
To run this example, first you will need to download and pre-process the raw data for the task using the included ```build_csv.py``` script:

```bash
$ python build_csv.py
```

If the script fails, make sure that you have installed all the package dependencies of this script which are: `shutil, tarfile, pathlib, pandas, requests, natsort, and sklearn`.

Missing packages can be installed using pip:
```bash
$ pip install <package_name>
```

Once you've downloaded and pre-processed the data, you can start training using any of the NML scripts provided. To begin training:
```bash
$ neopulse train -p <project_name> -f /DM-Dash/NeoPulse_Examples/Classification/Text/Sentiment/sentiment_full_auto.nml
```
The paths in the NML scripts in this directory assume that you have cloned this repository into the /DM-Dash directory of your machine. If you have put it somewhere else, you'll need to move the NML files into a location under the /DM-Dash directory, and change the path in the line:
```bash
bind = "/DM-Dash/NeoPulse_Examples/Classification/Text/S
entiment/training_data.csv" ;
```

# Tutorial Files
**build_csv.py:** Script creates list of training files and writes training full image paths and corresponding labels to a training CSV file.

**sentiment_full_auto.nml:** Features full use of the auto keyword to automatically generate the entire architecture.

**sentiment_call_auto.nml:** Features the use of auto to automatically select an architecture later.

**sentiment_choice_auto.nml:** Features use of auto keyword to automatically select from range of values for a given parameter.

**sentiment_dist_auto.nml:** Features use of the auto keyword to automatically select a value from a specified distribution of values (e.g. gaussian).

**sentiment_multi-GPU.nml:** Features use of the auto keyword to automatically select a value from a specified distribution of values (e.g. gaussian).

# Tutorial Videos and Guides
Tutorial videos are available in the *Tutorials & Guides* section of the [DimensionalMechanics™ Developer Portal](https://dimensionalmechanics.com/ai-developer-portal)

For more information on using the AudioDataGenerator visit the [Data section] of the NeoPulse™ AI Studio Documentation(https://docs.neopulse.ai/NML-source/#data)

# License
Tutorial materials are published under the MIT license. See license for commercial, academic, and personal use.
