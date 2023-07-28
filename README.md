# Examples

Welcome to `dstack-examples`. This repository contains a collection of examples
demonstrating how to use `dstack`.

## 1. Setup

```shell
pip install "dstack[aws,gcp,azure,lambda]" -U
dstack start
```

The `dstack start` command starts the Hub server, creating the default project that runs dev environments, pipelines,
and apps locally.

## 2. Projects

To run examples in the cloud (AWS, GCP, Azure),
make sure to create the corresponding [project](https://dstack.ai/docs/guides/projects/)
via the UI.

## 3. Clone the repo

```shell
git clone https://github.com/dstackai/dstack-examples
cd dstack-examples
dstack init
```

## 4. Profiles

Every example may have different GPU and memory requirements.
Before running examples, make sure to configure a [profile](https://dstack.ai/docs/#defining-profiles) with required
resources.

## 5. Run examples

| Example                            | How to run                                                                    |
| ---------------------------------- | ----------------------------------------------------------------------------- |
| **Default dev environment**        | `dstack run .`                                                                |
| **Serving with vLLM**              | `dstack run . -f vllm/serve.dstack.yml --port 8000:8000`                      |
| **Serving with TGI**               | `dstack run . -f text-generation-inference/serve.dstack.yml --port 8000:8000` |
| **Custom dev environment for TGI** | `dstack run . -f text-generation-inference/.dstack.yml --build`               |
| **Stable Diffussion XL as API**    | `dstack run . -f stable-diffusion-xl/api.dstack.yml --port 8000:8000`         |