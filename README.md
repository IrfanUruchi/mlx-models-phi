# MLX Models: Phi (Apple Silicon)

MLX-ready **Phi** instruct models converted and quantized for fast **on-device inference** on Apple Silicon using **mlx-lm**.

> Benchmarks shown below were measured on **MacBook Pro (M3 Pro)**.  
> Performance on other Apple devices (including iPhone/iPad) will vary.

---

## Available Models (Hugging Face)

- **Phi-4-mini-instruct (4-bit)**  
  https://huggingface.co/Irfanuruchi/Phi-4-mini-instruct-MLX-4bit

- **Phi-4-mini-instruct (8-bit)**  
  https://huggingface.co/Irfanuruchi/Phi-4-mini-instruct-MLX-8bit

---

## Quick Specs (M3 Pro)

| Model | Quant | Disk | Peak RAM | Notes |
|------|------:|-----:|---------:|------|
| Phi-4-mini | 4-bit | ~2.0 GB | ~2.22 GB | Best efficiency/quality |
| Phi-4-mini | 8-bit | ~3.8 GB | ~4.15 GB | Higher fidelity, more RAM |

---

## Installation

```bash
python3 -m venv mlx-env
source mlx-env/bin/activate
pip install -U mlx-lm
```

---

## Usage Examples

### Phi-4-mini (4-bit)
```bash
mlx_lm.generate   --model Irfanuruchi/Phi-4-mini-instruct-MLX-4bit   --prompt "Give me 5 short offline assistant tips."   --max-tokens 120
```

### Phi-4-mini (8-bit)
```bash
mlx_lm.generate   --model Irfanuruchi/Phi-4-mini-instruct-MLX-8bit   --prompt "Write a 1-paragraph plan for learning Spanish in 30 days."   --max-tokens 160
```

---

## Conversion Notes

Models were converted and quantized using `mlx_lm.convert`

---

## License

This repository contains **documentation only**.  
Each model follows the **original Phi license** as specified in its respective Hugging Face repository.
