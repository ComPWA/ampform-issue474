# Contributing

To contribute to this repository, all you need to install is [`uv`](https://docs.astral.sh/uv). Once you have that installed, here are some useful commands you can run:

- Start Jupyter Lab
  ```shell
  uv run jupyter lab docs
  ```
- Build a local version of the Jupyter Lite server:
  ```shell
  uv run \
    --group test \
    --no-dev \
    pytest docs/psi-to-phi-k-k.ipynb
  ```
  ```shell
  uv run \
    --group lite \
    --no-dev \
    jupyter lite build \
      --contents docs/constraints.txt \
      --contents docs/psi-to-phi-k-k-lite.ipynb \
      --contents docs/phsp.zarr.zip \
      --output-dir lite
  ```
- Run all notebooks
  ```shell
  uv run --group test --no-dev pytest docs/psi-to-phi-k-k.ipynb
  uv run --group test --no-dev pytest docs/psi-to-phi-k-k-lite.ipynb
  ```
