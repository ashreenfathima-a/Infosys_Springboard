# Milestone 2 – CodeGenie AI Explainer & Code Generator

## Project Overview

This project implements **Milestone 2** of the Infosys CodeGenie program.

**Objective:**

* Generate code using AI models
* Compare model performance
* Visualize results

**Models Implemented:**

* DeepSeek-Coder-1.3B (Salesforce/codegen-350M-multi)
* Phi-2-2.7B (microsoft/phi-2)

**Optional / Extended Models:**

* Gemma-2B-IT (google/gemma-2b-it)
* Stable-Code-3B (stabilityai/stable-code-3b)
* Replit-Code-3B (replit/replit-code-v1-3b)

---

## Folder Structure

```
Milestone_2/
│
├── Milestone_2_Ashreen_fathima (4).ipynb   # Main notebook
├── fixed_notebook.ipynb                     # Cleaned notebook
├── deepseek_output.txt                       # Sample DeepSeek output
├── phi2_output.txt                            # Sample Phi-2 output
├── response_times_plot.png                   # Model performance visualization
└── README.md                                 # This file
```

---

## Features

### Interactive Code Generation

* Choose **model** and input **code prompts**
* Models generate code **inline** in notebook cells

### Performance Testing

* Run each model on **10 sample prompts** across different domains
* Measure **response time** per prompt

### Visualization

* Bar plots for **average response time per model**
* Compare **speed and efficiency** of different models

---

## How to Run

### Prerequisites

* Python 3.10+
* Jupyter Notebook or VS Code Notebook
* Required packages:

```bash
pip install transformers accelerate torch matplotlib pandas gradio nbformat
```

### Steps

1. Open `Milestone_2_Ashreen_fathima (4).ipynb`
2. Run cells sequentially:

   * Load models (DeepSeek & Phi-2)
   * Generate code for sample prompts
   * Measure response time
   * Visualize results
3. Outputs are visible in notebook cells or saved as `.txt` / `.png` files

---

## Sample Output

**DeepSeek Generated Code:**

```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True
```

**Visualization of Response Time:**

![Response Time Plot](response_times_plot.png)

---

## Notes

* Only **DeepSeek** and **Phi-2** used for visualization to avoid GPU memory issues
* Outputs displayed **inline** and optionally saved as `.txt` / `.png` files
* Notebook cleaned to remove widget metadata: `fixed_notebook.ipynb`

---

## References

* [Infosys CodeGenie – Milestone 2 Instructions](https://colab.research.google.com/drive/17k3Vxrhp6seB7eUKMLAHYXqajA1YnIk8?usp=sharing)
* [Hugging Face Transformers](https://huggingface.co/docs/transformers/index)
* [Jupyter Notebook](https://jupyter.org/documentation)
