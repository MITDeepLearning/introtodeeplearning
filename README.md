[![banner](assets/banner.png)](http://introtodeeplearning.com)

This repository contains all of the code and software labs for [MIT Introduction to Deep Learning](http://introtodeeplearning.com)! All lecture slides and videos are available on the program website.

# Instructions
MIT Introduction to Deep Learning software labs are designed to be completed at your own pace. At the end of each of the labs, there will be instructions on how you can submit your materials as part of the lab competitions. These instructions include what information must be submitted and in what format.

## Opening the labs in Google Colaboratory:

The 2025 Introduction to Deep Learning labs will be run in Google's Colaboratory, a Jupyter notebook environment that runs entirely in the cloud, so you don't need to download anything. To run these labs, you must have a Google account.

On this Github repo, navigate to the lab folder you want to run (`lab1`, `lab2`, `lab3`) and open the appropriate python notebook (\*.ipynb). Click the "Run in Colab" link on the top of the lab. That's it!

## Running the labs
Now, to run the labs, open the Jupyter notebook on Colab. Navigate to the "Runtime" tab --> "Change runtime type". In the pop-up window, under "Runtime type" select "Python 3", and under "Hardware accelerator" select "GPU". Go through the notebooks and fill in the `#TODO` cells to get the code to compile for yourself!

## Running the labs locally with uv (only for PyTorch labs)

If you prefer to run the notebooks locally you can use the project's `uv` environment tool (used in this repo). The basic workflow is:

1. Open PowerShell and change to the repository root directory:

```powershell
cd \path\to\introtodeeplearning
```

2. (Optional) Verify your Python version matches the project's `requires-python` (see `pyproject.toml`):

```powershell
python --version
```

3. Install the project dependencies into the `uv` environment. The dependencies and any custom package indexes are declared in `pyproject.toml`. To install everything at once run:

```powershell
uv sync
```

This will install all dependencies listed in `pyproject.toml` and automatically use any indexes defined there (for example, the PyTorch CUDA index declared in this repo).

Notes:
- If `cu126` is incompatible with your machine, simply edit `pyproject.toml` and change the `url` value to the desired CUDA tag. For example, to use CUDA 12.1 change the URL to:

```toml
[[tool.uv.index]]
name = "pytorch"
url = "https://download.pytorch.org/whl/cu121"
```

You can use the PyTorch get-started selector (https://pytorch.org/get-started/locally/) to find the appropriate index URL.

This keeps the index configuration in a single place and makes it easy to switch CUDA versions for all contributors.

4. Start Jupyter Notebook or JupyterLab from the `uv` environment:

```powershell
uv run jupyter notebook
# or
uv run jupyter lab
```

### MIT Deep Learning package
You might notice that inside the labs we install the `mitdeeplearning` python package from the Python Package repository:

`pip install mitdeeplearning`

This package contains convienence functions that we use throughout the course and can be imported like any other Python package.

`>>> import mitdeeplearning as mdl`

We do this for you in each of the labs, but the package is also open source under the same license so you can also use it outside the class.

## Lecture Videos

[<img src="assets/video_play.png" width="500">](https://www.youtube.com/watch?v=njKP3FqW3Sk&list=PLtBw6njQRU-rwp5__7C0oIVt26ZgjG9NI&index=1)

All lecture videos are available publicly online and linked above! Use and/or modification of lecture slides outside of MIT Introduction to Deep Learning must reference:

> © MIT Introduction to Deep Learning
>
> http://introtodeeplearning.com

## License
All code in this repository is copyright 2025 [MIT Introduction to Deep Learning](http://introtodeeplearning.com). All Rights Reserved.

Licensed under the MIT License. You may not use this file except in compliance with the License. Use and/or modification of this code outside of MIT Introduction to Deep Learning must reference:

> © MIT Introduction to Deep Learning
>
> http://introtodeeplearning.com
