# DART (Full code to be released soon)
Official implementation of ICML 2024 paper "Learning to Play Atari in a World of Tokens" by  

[Pranav Agarwal](https://pranaval.github.io/), [Sheldon Andrews](https://profs.etsmtl.ca/sandrews/) and [Samira Ebrahimi Kahou](https://saebrahimi.github.io/). 

In this work, we introduce discrete abstract representations for transformer-based learning (DART), a sample-efficient method utilizing discrete representations for modeling both the world and learning behavior. DART outperforms previous state-of-the-art methods that do not use look-ahead search on the Atari 100k sample efficiency benchmark with a median human-normalized score of 0.790 and beats humans in 9 out of 26 games.

[Paper]()  [Webpage](https://pranaval.github.io/DART/)

<p align="center">
  <img width="100%" src="images/dtr.png">
</p>


## Dependencies
Create a virtual environment and install all the required files
```
python3.8 -m venv myenv
source myenv/bin/activate
pip install -r requirements.txt
```

## Overview
The main contribution of our work includes a novel approach that utilizes transformers for both world and policy modeling. Specifically, we utilize a transformer-decoder (GPT) for world modeling and a transformer-encoder (ViT) for policy learning. This represents an improvement compared to IRIS, which relies on CNNs and LSTMs for policy learning, potentially limiting its performance. We use discrete representations for policy and world modeling. These discrete representations capture abstract features, enabling our transformer-based model to focus on task-specific fine grained details. Attending to these details improves decision-making, as demonstrated by our results. To address the problem of partial observability, we introduce a novel mechanism for modeling the memory that aggregates task-relevant information from the previous time step to the next using a self-attention mechanism. Our model showcases enhanced interpretability and sample efficiency. It achieves state-of-the-art results (no-look-ahead search methods) on the Atari 100k benchmark with a median score of 0.790 and superhuman performance in 9 out of 26 games.

## Paper Associated
If you use it, please cite
```
@article{agarwal2024learning,
      title={Learning to Play Atari in a World of Tokens},
      author={Agarwal, Pranav and Andrews, Sheldon and Kahou, Samira Ebrahimi},
      booktitle={International Conference on Machine Learning (ICML)},
      year={2024}
    }
```

## Credits
* Modeling of tokens and the world is inspired from [https://github.com/eloialonso/iris](https://github.com/eloialonso/iris).
* [https://github.com/google-research/vision_transformer](https://github.com/google-research/vision_transformer)
  


