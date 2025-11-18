# AI-IMAGE-ENHANCEMENT AND FILE RECOVERY

Deep learning framework for recovering deleted images and restoring visual quality through intelligent enhancement.

## Overview

This project combines low-level disk scanning with advanced AI models to recover deleted images and automatically restore degraded quality. The system performs signature-based file carving and applies neural networks for classification and enhancement.

**Key Features:**
- Raw disk scanning for JPEG/PNG recovery
- AI-powered quality classification (ResNet-50)
- Intelligent restoration for noisy/blurry images (MPRNet)
- Automated pipeline with GUI interface

## Architecture

```
Raw Disk Scan → File Recovery → Quality Classification → Selective Restoration
                (Signatures)    (ResNet-50)            (MPRNet)
```

## Capabilities

- **Recovery**: Signature-based carving (95%+ success rate)
- **Classification**: 3-class quality detection (97% accuracy)
- **Restoration**: Multi-stage denoising and deblurring
- **Reporting**: Automated HTML reports with integrity checks

## Requirements

- Python 3.x
- PyTorch
- PyQt5
- Pre-trained models (ResNet-50, MPRNet)

## Quick Start

**1. Run recovery:**
```bash
python recovery_tool.py --mode disk_scan --output ./recovered
```

**2. Classify and restore:**
```bash
python enhance.py --input ./recovered --model mprnet
```

## Results

- File recovery: 95.17% average success rate
- Classification accuracy: 97%
- Restoration quality: Significant visual improvement on degraded images

## Datasets Used

Training data sourced from:
- SIDD (real-world noise)
- DIV2K (high-resolution)
- GoPro (motion blur)
- Blur Dataset (synthetic degradation)

## Future Work

- Extended format support (BMP, TIFF, WEBP)
- Fragmented file reassembly
- Mobile deployment
- Compression artifact removal
