# Getting Started

### Installation

Install the latest version via pip...

```bash
pip install be-great
```

... or download the source code from GitHub

```bash
git clone https://github.com/kathrinse/be_great.git
```

### Requirements

GReaT requires Python 3.9 (or higher) and the following packages:

- datasets >= 2.5.2
- numpy >= 1.23.1
- pandas >= 1.4.4
- scikit_learn >= 1.1.1
- torch >= 1.10.2
- tqdm >= 4.64.1
- transformers >= 4.22.1


### Quickstart

In the example below, we show how the GReaT approach is used to generate synthetic tabular data for the California Housing dataset.
```python
from be_great import GReaT
from sklearn.datasets import fetch_california_housing

data = fetch_california_housing(as_frame=True).frame

model = GReaT(llm='distilgpt2', epochs=50)
model.fit(data)
synthetic_data = model.sample(n_samples=100)
```

See Examples to find more details.
