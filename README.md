# Targeted Dropout

## Requirements
- Python 3
- Tensorflow 1.8

## Quick Start
1. Train a model: `python -m targeted-dropout.train --hparams=resnet_default`
2. Prune that model: `python -m targeted-dropout.scripts.prune.eval --hparams=resnet_default --prune_percent 0.0,0.25,0.5,0.75,0.95`

### Flags
- `--env`: one of `local`, `gcp` (GPU instances), or `tpu` (TPU instances). Feel free to add more if necessary.
- `--hparams`: the hparam set you want to run.
- `--hparam_override`: manually specify hparams to be overridden (e.g `--hparam_override 'drop_rate=0.66'`)
