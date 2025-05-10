
# Setup

```bash
brew install uv
uv venv --python=python3.12 .venv
source .venv/bin/activate
uv pip install .[torch,testing]
```

## test

```bash
make test
py.test tests/models/bert/test_modeling_bert.py 
RUN_SLOW=1 py.test tests/models/bert/test_modeling_bert.py -k test_model_from_pretrained --pdb
```

## rest

```bash
make style
rm -rf .venv
```
