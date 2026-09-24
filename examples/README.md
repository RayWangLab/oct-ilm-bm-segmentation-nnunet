# Sample inference data

Models and samples are available from [RayWangLab/oct-ilm-bm-segmentation-nnunet on Hugging Face](https://huggingface.co/RayWangLab/oct-ilm-bm-segmentation-nnunet). Download the samples from the [examples directory](https://huggingface.co/RayWangLab/oct-ilm-bm-segmentation-nnunet/tree/main/examples).

Download the matching sample directory and preserve this layout:

```text
examples/
├── Dataset001_OCT-Layer-2d-TR/
│   ├── images/   # 400 PNG inputs: 10241-000_0000.png ... 10241-399_0000.png
│   └── labels/   # 400 masks: 10241-000.png ... 10241-399.png
└── Dataset002_OCT-Layer-3d-TR/
    ├── images/10241_0000.nii.gz
    └── labels/10241.nii.gz
```

Each model has one sample volume. Dataset001 represents it as individual PNG B-scans; Dataset002 uses a NIfTI volume.

1. Install the matching ZIP using the [main README](../README.md).
2. Pass only the matching `images/` directory to inference, keeping filenames unchanged.
3. Save results separately, for example in `predictions/Dataset001/` or `predictions/Dataset002/`.
4. Use `labels/` for comparison after confirming alignment and label encoding.
