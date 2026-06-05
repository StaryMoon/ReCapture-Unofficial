# ReCapture-Unofficial

> Unofficial PyTorch implementation starter for **ReCapture: Generative Video Camera Controls for User-Provided Videos using Masked Video Fine-Tuning** (CVPR 2025).
>
> If this repo saves you reading / reproduction time, please star it and follow [@StaryMoon](https://github.com/StaryMoon). I am building honest open reproduction starters for recent CVPR papers.

## Status

This repository is an **independent, unofficial, work-in-progress starter**.

- Paper: [ReCapture: Generative Video Camera Controls for User-Provided Videos using Masked Video Fine-Tuning](https://openaccess.thecvf.com/content/CVPR2025/html/Zhang_ReCapture_Generative_Video_Camera_Controls_for_User-Provided_Videos_using_Masked_CVPR_2025_paper.html)
- Venue: CVPR 2025
- Reproduction status: **benchmarks are not reproduced yet**
- Relationship to authors: this repo is not official and is not affiliated with the paper authors.

## What Is Implemented

This v0.1.0 starter implements a compact, readable scaffold inspired by the paper:

- temporal token encoder
- text/control token fusion
- cross-attention video block
- toy denoising objective
- smoke-test script

The goal is to make the high-level idea easy to inspect, fork, and improve.

## What Is Not Implemented Yet

- full video diffusion model
- VAE or latent video tokenizer
- large-scale training recipe
- generation-quality reproduction

## Quick Start

```bash
git clone https://github.com/StaryMoon/ReCapture-Unofficial.git
cd ReCapture-Unofficial
pip install -r requirements.txt
python scripts/smoke_test.py
```

Expected output includes:

```text
loss: ...
video: torch.Size([2, 8, 16, 64])
```

## Minimal Usage

```python
import torch
from recapture_unofficial import UnofficialStarter

image = torch.rand(2, 3, 64, 64)
model = UnofficialStarter(kind="video")
out = model(image)
```

## Roadmap

- [ ] Replace toy modules with a closer implementation of the paper.
- [ ] Add dataset loader and config files.
- [ ] Add metric scripts and visualization.
- [ ] Reproduce a small benchmark or ablation table.
- [ ] Add pretrained weights once experiments are stable.

## Search Tags

cvpr-2025, camera-control, video-generation, masked-finetuning, pytorch, unofficial-implementation

## Citation

Please cite the original paper if you use the method. This repo is only an unofficial starter and does not replace the paper.

## License

MIT License. The original paper and official materials remain owned by their respective authors / publishers.
