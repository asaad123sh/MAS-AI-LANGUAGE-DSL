# 🚀 MAS AI Language - Complete User Guide

<div align="center">

![Version](https://img.shields.io/badge/Version-MAS%2F1-brightgreen?style=for-the-badge&logo=codacy)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10%2B-yellow?style=for-the-badge&logo=python)

**Transform AI Model Development with Simplicity & Power**

[🚀 Quick Start](#installation) • [📚 Documentation](#core-commands) • [💡 Examples](#examples) • [🐛 Support](#troubleshooting)

</div>

---

## 📋 Table of Contents

- [🎯 Introduction](#introduction)
- [📦 Installation](#installation)
- [📂 File Structure](#file-structure)
- [🔤 Syntax Overview](#syntax-overview)
- [⚙️ Core Commands](#core-commands)
- [🎓 Advanced Features](#advanced-features)
- [💼 Examples](#examples)
- [🔧 CLI Commands](#cli-commands)
- [🚨 Troubleshooting](#troubleshooting)
- [📖 Best Practices](#best-practices)
- [📚 Additional Resources](#additional-resources)

---

## 🎯 Introduction

> **MAS (Master Artificial Structured AI Language)** is a revolutionary domain-specific language (DSL) designed to simplify AI model creation, training, and deployment.

With MAS, you can build sophisticated AI models using simple, human-readable commands instead of complex Python code. No more wrestling with framework complexities—focus on what matters! ✨

### ✨ Key Features

<table>
<tr>
<td>

🚀 **Simple Syntax**
Python-like syntax that's intuitive and easy to learn

</td>
<td>

🧠 **Multiple Model Types**
Support for LLMs, image generation, video, audio, and more

</td>
</tr>
<tr>
<td>

🔧 **Auto Configuration**
Intelligent validation and compatibility checking

</td>
<td>

📦 **Dependency Management**
Automatic installation of required packages

</td>
</tr>
<tr>
<td>

💾 **Smart Sharding**
Automatic model splitting for large models

</td>
<td>

🔥 **Hardware Protection**
Heat sensing and intelligent resource management

</td>
</tr>
<tr>
<td>

🎯 **LoRA Support**
Efficient fine-tuning with Low-Rank Adaptation

</td>
<td>

🔗 **Multi-Model Orchestration**
Connect and run multiple models together seamlessly

</td>
</tr>
</table>

---

### 🤖 Supported Model Types

<table>
<tr>
<td align="center">

**Text Models**
- 🗣️ LLM (Large Language Models)
- 📊 Text Classification
- 🏷️ Token Classification
- 🔍 Embedding Models

</td>
<td align="center">

**Vision Models**
- 🎨 Image Generation
- 🖼️ Image-to-Image
- 👁️ Image Classification
- 🎯 Object Detection

</td>
<td align="center">

**Media Models**
- 🎬 Video Generation
- 🎤 Speech-to-Text
- 🔊 Text-to-Speech
- 🎵 Audio Generation

</td>
<td align="center">

**Advanced**
- 🔀 Segmentation
- 🌐 Multimodal

</td>
</tr>
</table>

---

## 📦 Installation

> Choose the installation method that best fits your needs

### 🐍 Method 1: Python Package Installation (For Developers)

<details open>
<summary><b>Click to expand/collapse</b></summary>

```bash
# Clone or download the project
cd MAS-project-folder

# Install in development mode
python -m pip install -e .
```

</details>

---

### 🪟 Method 2: Windows Installer (For End Users)

<details open>
<summary><b>Click to expand/collapse</b></summary>

1. 📥 Download either `MAS-AI-Language-Setup-<version>.exe` or `MAS-AI-Language-Setup-<version>.msi`
2. ▶️ Run the installer wizard
3. ✅ Check "Add MAS command to system PATH"
4. 🖥️ Open a new terminal and verify installation:

```powershell
mas --help
```

</details>

---

### ✔️ Verify Installation

After installation, verify everything is working:

```bash
mas --help
```

You should see a list of available commands. If you get any errors, check the **[Troubleshooting](#troubleshooting)** section.

---

## 📂 File Structure

### 📄 .MASAI File Format

> MAS programs are written in files with the `.MASAI` extension (case-insensitive: `.masai` or `.MASAI`)

**Basic Structure:**

```python
# MAS/1
# Your MAS commands go here

MAKE_MODLE(
    name="my_model",
    model_type="llm",
    architecture="transformer_decoder",
    # ... more parameters
)
```

---

### ⚠️ Important Rules

<table>
<tr>
<td>

> 🔴 **MUST DO**
> - First line must be `# MAS/1` (MAS version signature)
> - File extension must be `.MASAI` or `.masai`
> - Use `#` for single-line comments
> - Only literal values allowed (strings, numbers, booleans, lists, dicts)

</td>
<td>

> 🔵 **MUST NOT DO**
> - ❌ Don't forget the `# MAS/1` header
> - ❌ Don't use wrong file extension (.mas, .msa, etc.)
> - ❌ Don't use Python variables or expressions
> - ❌ Don't use complex logic or loops

</td>
</tr>
</table>

---

## 🔤 Syntax Overview

### 🔗 Basic Command Structure

```python
COMMAND_NAME(
    parameter_name="value",
    another_parameter=123,
    boolean_param=True,
    list_param=["item1", "item2"],
    dict_param={"key": "value"}
)
```

---

### 📊 Data Types Reference

| 🏷️ Type | 📝 Example | 🎯 Usage | 💡 Notes |
|:---:|:---:|:---:|:---|
| **String** | `"hello"` | Names, paths, types | Enclosed in quotes |
| **Integer** | `42` | Counts, dimensions | Whole numbers only |
| **Float** | `0.0003` | Learning rates | Decimal numbers |
| **Boolean** | `True` / `False` | Flags, toggles | Enable/disable |
| **List** | `["a", "b"]` | Multiple values | Order preserved |
| **Dictionary** | `{"key": "val"}` | Complex configs | Key-value pairs |

---

### 📋 Naming Conventions

```
Model Names   → lowercase_with_underscores   (e.g., my_llm_model)
Parameters    → snake_case                   (e.g., learning_rate, num_layers)
Commands      → UPPERCASE                    (e.g., MAKE_MODLE, TRAIN_MODEL)
```

---

## ⚙️ Core Commands

> All commands follow consistent structure and parameter naming

### 1️⃣ MAKE_MODLE / MAKE_MODEL

**🎯 Purpose:** Create a new AI model blueprint

**💬 Syntax:**
```python
MAKE_MODLE(
    name="model_name",
    model_type="type",
    architecture="architecture_name",
    # ... additional parameters
)
```

**✅ Required Parameters:**

| Parameter | Type | Description |
|:---:|:---:|---|
| `name` | string | Unique identifier for your model |
| `model_type` | string | Category of AI model |
| `architecture` | string | Neural network structure |

**📋 Common Optional Parameters:**

| Parameter | Type | Description | Example |
|:---:|:---:|---|:---:|
| `vocab_size` | int | 📚 Vocabulary size (text models) | `32000` |
| `num_layers` | int | 🏗️ Network layers | `8` |
| `hidden_size` | int | 🧠 Hidden state size | `512` |
| `num_heads` | int | 🎯 Attention heads | `8` |
| `intermediate_size` | int | 🔗 Feed-forward layer size | `2048` |
| `learning_rate` | float | 📈 Training LR | `0.0003` |
| `batch_size` | int | 📦 Batch size | `4` |
| `epochs` | int | 🔄 Training epochs | `10` |
| `optimizer` | string | ⚙️ Optimizer type | `"adamw"` |
| `dtype` | string | 💾 Data precision | `"bfloat16"` |
| `device_target` | string | 🖥️ Hardware | `"cpu"` / `"cuda"` |
| `train_dataset_path` | string | 📂 Training data path | `"data/train.jsonl"` |
| `max_context_length` | int | 📏 Max input length | `2048` |
| `tokenizer_type` | string | 🔤 Tokenizer | `"bpe"` |
| `save_format` | string | 💾 Save format | `"safetensors"` / `"pt"` |
| `parts` | bool | 🔀 Enable sharding | `True` |
| `max_ram_allocation` | float | 🐏 Max RAM (GB) | `2.0` |
| `auto_install_dependencies` | bool | 📦 Auto-install packages | `True` |

---

### 2️⃣ TRAIN_MODEL / TRAIN_MODLE

**🎯 Purpose:** Train an existing model

**💬 Syntax:**
```python
TRAIN_MODEL(
    name="model_name",
    epochs=10,
    learning_rate=0.0003,
    # ... override training parameters
)
```

**✅ Key Parameters:**
- `name` ⭐ **[REQUIRED]** - Name of the model to train
- Any parameter from `MAKE_MODLE` can be overridden here

**🎨 Special Values:**
- `dataset_path="userinput"` - Opens GUI file picker for dataset
- `save_path="userinput"` - Opens GUI folder picker for output

---

### 3️⃣ LOAD_MODLE / LOAD_MODEL

**🎯 Purpose:** Load a model into memory for inference

**💬 Syntax:**
```python
LOAD_MODLE(
    name="model_name",
    device="cpu"
)
```

**✅ Parameters:**
- `name` ⭐ **[REQUIRED]** - Name of the model to load
- `device` (optional) - `"cpu"` or `"cuda"` (default: `"cpu"`)

---

### 4️⃣ RUN_MODEL

**🎯 Purpose:** Run inference with a loaded model

**💬 Syntax:**
```python
RUN_MODEL(
    name="model_name",
    prompt="Your prompt here",
    max_tokens=150
)
```

**✅ Parameters:**
- `name` ⭐ **[REQUIRED]** - Name of the loaded model
- `prompt` (optional) - Input text/data
- `max_tokens` (optional) - Maximum generation length

---

### 5️⃣ MAKE_LORA

**🎯 Purpose:** Create a LoRA adapter for fine-tuning

**💬 Syntax:**
```python
MAKE_LORA(
    name="lora_adapter_name",
    base_model="base_model_name",
    rank=16,
    alpha=32
)
```

**✅ Parameters:**
- `name` ⭐ **[REQUIRED]** - Name for the LoRA adapter
- `base_model` ⭐ **[REQUIRED]** - Name of the base model
- `rank` (optional) - LoRA rank (default: 8)
- `alpha` (optional) - LoRA alpha scaling (default: 16)

---

### 6️⃣ TRAIN_LORA

**🎯 Purpose:** Train a LoRA adapter

**💬 Syntax:**
```python
TRAIN_LORA(
    name="lora_adapter_name",
    epochs=3,
    learning_rate=0.0001
)
```

---

### 7️⃣ RUN_LORA

**🎯 Purpose:** Run inference with a LoRA adapter

**💬 Syntax:**
```python
RUN_LORA(
    name="lora_adapter_name",
    prompt="Your prompt here"
)
```

---

### 8️⃣ CONNECT_MODELS

**🎯 Purpose:** Group multiple models for orchestration

**💬 Syntax:**
```python
CONNECT_MODELS(
    group="group_name",
    models=["model1", "model2", "model3"]
)
```

**✅ Parameters:**
- `group` ⭐ **[REQUIRED]** - Name for the model group
- `models` ⭐ **[REQUIRED]** - List of model names to connect

---

### 9️⃣ LOAD_MULTIMODLES

**🎯 Purpose:** Load all models in a group

**💬 Syntax:**
```python
LOAD_MULTIMODLES(
    group="group_name",
    device="cuda"
)
```

---

### 🔟 RUN_ALL_MODLES

**🎯 Purpose:** Run inference on all models in a group

**💬 Syntax:**
```python
RUN_ALL_MODLES(
    group="group_name",
    prompt="Your prompt for all models"
)
```

---

## 🎓 Advanced Features

### 1️⃣ Automatic Dependency Management

MAS automatically installs required packages based on model type - **no manual pip commands needed!**

**✅ To use automatic installation:**
```python
MAKE_MODLE(
    name="my_model",
    model_type="llm",
    auto_install_dependencies=True  # This is the default
)
```

**❌ To disable:**
```python
auto_install_dependencies=False
```

**🔧 Manual dependency installation using MAS CLI:**

```bash
# 📦 Install dependencies for .pt models on CPU
mas -get .pt --cpu

# 🎮 Install dependencies for safetensors on GPU
mas -get .st --gpu

# 🔗 Install all dependencies
mas -get .bin --full

# 👁️ Preview what would be installed (dry run)
mas -get .pt --cpu --dry-run

# 🗑️ Remove dependencies
mas -remove .pt --cpu
```

---

### 2️⃣ Model Sharding

For large models, enable automatic sharding to **handle memory constraints gracefully**:

```python
MAKE_MODLE(
    name="large_model",
    parts=True,  # Enable sharding
    max_ram_allocation=2.0  # Max 2GB RAM
)
```

> ℹ️ **What it does:** Splits the model into multiple files for safer loading and efficient memory usage.

---

### 3️⃣ Hardware Heat Sensing

MAS monitors system temperature and **throttles execution** to prevent overheating and hardware damage:

```python
MAKE_MODLE(
    name="my_model",
    device_target="cuda",
    max_gpu_allocation=4.0  # Max 4GB GPU memory
)
```

> 🌡️ **Smart Protection:** Automatic throttling ensures your hardware stays safe!

---

### 4️⃣ Interactive File Pickers

Use `"userinput"` to open **GUI file/folder pickers** - no command-line navigation needed:

```python
TRAIN_MODEL(
    name="my_model",
    dataset_path="userinput",  # Opens folder picker
    save_path="userinput"      # Opens folder picker
)
```

> 🖱️ **User-Friendly:** Perfect for non-technical users!

---

### 5️⃣ Parameter Estimation

MAS automatically estimates model parameters based on target size:

```python
MAKE_MODLE(
    name="my_model",
    parameter_size="1B"  # Target 1 billion parameters
)
```

> 🤖 **Smart Scaling:** Automatically scales `num_layers`, `hidden_size`, etc. to match your target!

---

## 💼 Examples

### 📝 Example 1: Basic Language Model

<details open>
<summary><b>File: <code>baby_llm.masai</code> - A small language model for learning</b></summary>

```python
# MAS/1
# A small language model for learning

MAKE_MODLE(
    name="baby_llm",
    model_type="llm",
    architecture="transformer_decoder",
    dtype="bfloat16",
    optimizer="adamw",
    learning_rate=0.0003,
    batch_size=8,
    epochs=10,
    train_dataset_path="data/train.jsonl",
    vocab_size=32000,
    tokenizer_type="bpe",
    max_context_length=2048,
    num_layers=8,
    hidden_size=512,
    num_heads=8,
    intermediate_size=2048,
    loss_function="cross_entropy",
    save_format="safetensors",
    auto_install_dependencies=True
)
```

**▶️ Run it:**
```bash
mas run baby_llm.masai
```

</details>

---

### 🎨 Example 2: Text Classification Model

<details>
<summary><b>File: <code>sentiment_classifier.masai</code> - Sentiment analysis classifier</b></summary>

```python
# MAS/1
# Sentiment analysis classifier

MAKE_MODLE(
    name="sentiment_model",
    model_type="text_classification",
    architecture="bert_classifier",
    num_labels=3,  # positive, negative, neutral
    vocab_size=30000,
    num_layers=6,
    hidden_size=384,
    num_heads=6,
    learning_rate=0.00005,
    batch_size=16,
    epochs=5,
    train_dataset_path="data/sentiment_train.csv",
    dtype="float32",
    device_target="cuda"
)
```

</details>

---

### 🖼️ Example 3: Image Generation Model

<details>
<summary><b>File: <code>image_generator.masai</code> - Diffusion model for image generation</b></summary>

```python
# MAS/1
# Diffusion model for image generation

MAKE_MODLE(
    name="my_image_gen",
    model_type="image_gen",
    architecture="unet",
    image_size=512,
    num_layers=12,
    hidden_size=768,
    learning_rate=0.0001,
    batch_size=4,
    epochs=100,
    train_dataset_path="data/images/",
    dtype="float16",
    device_target="cuda",
    save_format="safetensors"
)
```

</details>

---

### 🔀 Example 4: Multi-Model Pipeline

<details>
<summary><b>File: <code>multimodal_pipeline.masai</code> - Pipeline combining multiple models</b></summary>

```python
# MAS/1
# Pipeline combining multiple models

CONNECT_MODELS(
    group="assistant_stack",
    models=["llm_master", "image_gen_worker", "video_gen_worker"]
)

LOAD_MULTIMODLES(
    group="assistant_stack",
    device="cuda"
)

RUN_ALL_MODLES(
    group="assistant_stack",
    prompt="Create a short video showing a sunset over mountains"
)
```

</details>

---

### 🔧 Example 5: LoRA Fine-Tuning

<details>
<summary><b>File: <code>lora_finetune.masai</code> - Fine-tune a model with LoRA</b></summary>

```python
# MAS/1
# Fine-tune a model with LoRA

# First, create the base model
MAKE_MODLE(
    name="base_llm",
    model_type="llm",
    architecture="transformer_decoder",
    vocab_size=32000,
    num_layers=12,
    hidden_size=768,
    num_heads=12,
    lora_enabled=True  # Enable LoRA support
)

# Create a LoRA adapter
MAKE_LORA(
    name="chat_adapter",
    base_model="base_llm",
    rank=16,
    alpha=32
)

# Train the adapter
TRAIN_LORA(
    name="chat_adapter",
    epochs=3,
    learning_rate=0.0001,
    dataset_path="data/chat_data.jsonl"
)

# Load and run
LOAD_MODLE(
    name="base_llm",
    device="cuda"
)

RUN_LORA(
    name="chat_adapter",
    prompt="Hello! How can you help me today?"
)
```

</details>

---

### 🎮 Example 6: Training with GUI Picker

<details>
<summary><b>File: <code>interactive_training.masai</code> - Training with interactive file selection</b></summary>

```python
# MAS/1
# Training with interactive file selection

MAKE_MODLE(
    name="my_model",
    model_type="llm",
    architecture="transformer_decoder",
    vocab_size=32000,
    num_layers=8,
    hidden_size=512
)

TRAIN_MODEL(
    name="my_model",
    dataset_path="userinput",  # Opens folder picker
    save_path="userinput",     # Opens folder picker
    epochs=10
)
```

</details>

---

### 💾 Example 7: Large Model with Sharding

<details>
<summary><b>File: <code>large_model.masai</code> - Large model with automatic sharding</b></summary>

```python
# MAS/1
# Large model with automatic sharding

MAKE_MODLE(
    name="large_llm",
    model_type="llm",
    architecture="transformer_decoder",
    parameter_size="7B",  # 7 billion parameters
    dtype="bfloat16",
    parts=True,  # Enable automatic sharding
    max_ram_allocation=8.0,  # 8GB RAM limit
    max_gpu_allocation=12.0,  # 12GB GPU limit
    save_format="safetensors",
    optimizer="adamw",
    learning_rate=0.0001,
    batch_size=2,
    gradient_checkpointing=True  # Save memory
)
```

</details>

```python
# MAS/1
# Large model with automatic sharding

MAKE_MODLE(
    name="large_llm",
    model_type="llm",
    architecture="transformer_decoder",
    parameter_size="7B",  # 7 billion parameters
    dtype="bfloat16",
    parts=True,  # Enable automatic sharding
    max_ram_allocation=8.0,  # 8GB RAM limit
    max_gpu_allocation=12.0,  # 12GB GPU limit
    save_format="safetensors",
    optimizer="adamw",
    learning_rate=0.0001,
    batch_size=2,
    gradient_checkpointing=True  # Save memory
)
```

---

## 🔧 CLI Commands

### ▶️ Running MAS Files

```bash
# 🚀 Run a .masai file directly
mas run examples/baby_llm.masai

# 🔧 Compile to bytecode first (faster for repeated runs)
mas compile examples/baby_llm.masai

# ⚡ Run compiled bytecode
mas runc examples/baby_llm.masc
```

---

### 💻 Direct Command Mode

Execute single commands without a file:

```bash
mas cmd MAKE_MODEL --args-json "{\"name\":\"test_model\",\"model_type\":\"llm\",\"architecture\":\"transformer_decoder\",\"vocab_size\":10000}"
```

---

### 📦 Dependency Management

```bash
# 🔗 Install dependencies for different formats
mas -get .pt --cpu      # PyTorch CPU
mas -get .st --gpu      # Safetensors GPU
mas -get .bin --full    # All formats

# 🗑️ Remove dependencies
mas -remove .pt --cpu

# 👁️ Dry run (preview only)
mas -get .st --gpu --dry-run
```

---

## 🚨 Troubleshooting

### ❌ Common Errors

#### 1️⃣ Invalid .MASAI Signature

**🔴 Error:**
```
Invalid .MASAI signature.
First non-empty line must be exactly: # MAS/1
```

**✅ Solution:**
Add `# MAS/1` as the **first line** of your file. Nothing before it!

---

#### 2️⃣ Incompatible Parameters

**🔴 Error:**
```
GuidedConfigError: Field 'vocab_size' is incompatible with model_type 'image_gen'
```

**✅ Solution:**
Remove text-specific parameters from image models. Check model type compatibility:
- 📚 **Text models** (`llm`, `text_classification`) → Use `vocab_size`, `tokenizer_type`
- 🖼️ **Image models** (`image_gen`, `image_classification`) → Use `image_size`, `image_channels`
- 🎬 **Video models** (`video_gen`) → Use `video_fps`, `video_resolution`

---

#### 3️⃣ Missing Dependencies

**🔴 Error:**
```
Some required dependencies could not be installed automatically.
```

**✅ Solution:**
```bash
# Install manually
pip install torch transformers tokenizers datasets

# Or use MAS dependency manager
mas -get .pt --cpu
```

---

#### 4️⃣ File Extension Error

**🔴 Error:**
```
Unsupported file extension '.mas'
```

**✅ Solution:**
Rename your file to use `.MASAI` extension (uppercase or lowercase - both work!)

---

### ⚡ Performance Tips

| Tip | Implementation | Use Case |
|:---:|:---|---|
| **🚀 Speed Boost** | Use `dtype="bfloat16"` | Fast training on modern GPUs |
| **💾 Memory Save** | Enable `gradient_checkpointing=True` | Training large models |
| **📦 Batch Tuning** | CPU: 1-4 / Small GPU: 4-8 / Large GPU: 16-32 | Optimal throughput |
| **🔀 Handle Large Models** | Enable `parts=True` with `max_ram_allocation` | Models > 2GB |

**Quick reference:**
```python
# Fast training configuration
MAKE_MODLE(
    name="optimized_model",
    dtype="bfloat16",                  # ⚡ Speed
    gradient_checkpointing=True,       # 💾 Memory
    batch_size=16,                     # 📦 Throughput
    parts=True,                        # 🔀 Large models
    max_ram_allocation=4.0
)
```

---

## 📂 Output Files

After running `MAKE_MODLE`, you'll find:

```
📁 artifacts/
└── 📁 model_name/
    ├── 📋 model_manifest.json    # ⚙️ Configuration and metadata
    ├── 📊 checkpoint-0.pt        # 🧠 Model weights (if generated)
    └── 📁 model/                 # 🔀 (or sharded parts if parts=True)
```

**manifest.json contains:**
- ⚙️ Model configuration
- 📦 Dependency report
- ⚠️ Warnings
- 📈 Estimated parameters
- 📍 Physical model path

---

## 🏗️ Architecture Reference

| Category | Supported Architectures |
|:---:|---|
| **🗣️ LLM** | `transformer_decoder` `gpt` `bert` `t5` |
| **🖼️ Image** | `unet` `vae` `gan` `vit` (Vision Transformer) |
| **🎤 Audio** | `wav2vec` `whisper` `tacotron` |

---

## 📖 Best Practices

<table>
<tr>
<td width="50%">

### ✅ DO

- ✔️ **Start small** - Test with small models first
- ✔️ **Use version control** - Track your .masai files
- ✔️ **Comment your code** - Use `#` for documentation
- ✔️ **Validate early** - Run `mas compile` to check syntax
- ✔️ **Monitor resources** - Set `max_ram_allocation`

</td>
<td width="50%">

### ❌ DON'T

- ❌ **Don't skip the MAS/1 header**
- ❌ **Don't use wrong extensions**
- ❌ **Don't set batch_size too high**
- ❌ **Don't ignore warnings**
- ❌ **Don't leave unsharded large models**

</td>
</tr>
</table>

**Advanced Best Practices:**
1. **Save frequently** - Use appropriate `save_format` (prefer `safetensors`)
2. **Test incrementally** - Build complex pipelines step by step
3. **Use LoRA for experiments** - Faster iteration with less compute
4. **Enable checkpointing** - Reduce memory footprint significantly
5. **Monitor heat** - Enable hardware heat sensing for production

---

## 📚 Additional Resources

<table>
<tr>
<td align="center">

### 🐛 Report Issues
[GitHub Issues](https://github.com/MAS-AI/issues)
Report bugs and request features

</td>
<td align="center">

### 📖 More Examples
Check the `/docs` folder
for additional examples

</td>
<td align="center">

### 👥 Community
Join discussions
for help and tips

</td>
</tr>
</table>

---

## 📜 Version History

| Version | Release | Features |
|:---:|:---:|---|
| **MAS/1** | Initial | Core commands • 14+ model types • Auto dependencies • LoRA • Multi-model |

---

<div align="center">

## 🎉 Getting Started

Ready to build amazing AI models? Follow these steps:

1. **Install MAS** - Choose your preferred method from [Installation](#installation)
2. **Read the syntax** - Understand the basics from [Syntax Overview](#syntax-overview)
3. **Try examples** - Start with [Example 1](#example-1-basic-language-model)
4. **Build your own** - Create your first `.masai` file
5. **Join the community** - Share your creations!

### 🚀 Quick Start Command

```bash
mas run examples/baby_llm.masai
```

---

**Made with ❤️ for the AI community**

![MAS Logo](https://img.shields.io/badge/MAS-AI%20Language-blue?style=flat-square)
![Release](https://img.shields.io/badge/Release-Stable-green?style=flat-square)
![Community](https://img.shields.io/badge/Community-Active-brightgreen?style=flat-square)

---

**🌟 Star us on GitHub if MAS helps you build amazing models!**

</div>
