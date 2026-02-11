# Fine-tuned Llama 3.2 3B Model

This document describes a Llama 3.2 3B model that has been fine-tuned for specific tasks.

## Model Overview
- **Base Model**: `unsloth/Llama-3.2-3B-Instruct`
- **Fine-tuning Framework**: Unsloth with TRL (Transformer Reinforcement Learning)
- **Dataset**: `mlabonne/FineTome-100k`
- **Quantization**: 4-bit loading for efficient inference (`load_in_4bit = True`)
- **Chat Template**: Llama-3.1

## Training Summary
- **Hardware**: Optimized for GPU acceleration.
- **Epochs/Steps**: Trained for 60 steps, with optimized batching.
- **Learning Rate**: Configured for effective convergence (2e-4).

## Usage

To utilize this model, load it with the Unsloth `FastLanguageModel` and your preferred `transformers` library components. Ensure your environment supports the specified quantization and chat template.

### Example (Conceptual)

```python
# Load model and tokenizer
# Prepare input using inference_tokenizer.apply_chat_template()
# Generate response using inference_model.generate()
```

## Directory Contents
- `adapter_config.json`: Configuration for the PEFT adapter.
- `adapter_model.safetensors`: The fine-tuned weights of the PEFT adapter.
- `README.md`: This documentation file.

For detailed usage, refer to the original training notebook or `Unsloth` documentation.
