# MRIModelBench

## Quick Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/WingfungHu/MRIModelBench.git
cd MRIModelBench
```

### 2. Set up a virtual environment

Choose the command for your operating system:

- **macOS / Linux:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
- **Windows (PowerShell):**
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

### 3. Install dependencies

Once your virtual environment is active, install the required packages:

```bash
pip install -r requirements.txt
```

### 4. Run the project

With the dependencies installed, you'll be able to run any of the available notebooks in the repository.

Run the notebooks in descending order:
- Preprocessing_Data.ipynb
- Naive_Benchmark.ipynb
- Decision_Tree_Baseline.ipynb


### Optional: VLM benchmark

`notebooks/ollama_vlm.ipynb` tests an open-weights vision-language model (VLM) on the same test split, with zero-shot and few-shot prompts. The model runs locally through [Ollama](https://ollama.com), so no API key is needed.

To run it:

1. Install Ollama and make sure it is running.
2. Download a vision model: `ollama pull qwen2.5vl:3b` (about 3 GB, fits a 4 GB GPU). With 8 GB of GPU memory or more you can try `qwen2.5vl:7b` instead.
3. Run `pip install -r requirements.txt`, then open the notebook, set `MODEL` and `SAMPLE_PER_CLASS` in the configuration cell, and run it.
