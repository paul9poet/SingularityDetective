📘 docs/JUPYTER_NOTEBOOKS_GUIDE.md (Extended)
# Jupyter Notebooks Guide  
## AGI-ColdCases / SingularityDetective

This document is a complete, step-by-step guide to using, creating, and contributing Jupyter Notebooks for this project.

Notebooks here are not auxiliary examples — they are **interactive research artifacts** that combine narrative explanation, executable code, and visualization to teach and explore the structural ideas behind the AGI-ColdCases architecture.

---

## 🧠 Why Notebooks Matter in This Project

In a research-driven architecture like AGI-ColdCases, notebooks serve multiple essential purposes:

1. **Pedagogy:**  
   Teach core concepts (topos, spectral singularity, VSA, ethics) with narrative + code.

2. **Exploration:**  
   Run simulations, visualize singularity resolution, experiment with invariants.

3. **Documentation as Code:**  
   Make implementation *visible* — not just described.

4. **Collaboration:**  
   Provide an accessible entry point for researchers, engineers, linguists, and students.

---

## 🛠 Required Tools + Setup

### Install Jupyter and Dependencies

Ensure you have a Python environment. Then install:

```bash
pip install jupyter numpy scipy matplotlib pandas ripser scikit-tda

(Not all notebooks require every library — dependencies should be declared in requirements.txt.)

Launching Jupyter

In your shell:

cd AGI-ColdCases
jupyter notebook

A browser should open a local Jupyter interface. You’ll see the notebooks/ folder.

📊 Notebook Structure Pattern

Every notebook follows a predictable pattern that makes them easy to read and contribute to:

🧩 1. Title and Abstract

Each notebook starts with a clear title and a short description of:

what it explores

what the reader will learn

what they should expect

Example:

“Spectral Entropy and Gap Statistics: Interactive Exploration of Forensic Invariants”

🧠 2. Narrative Explanation Blocks

Markdown cells are rich — tabs, diagrams, and equations. These explain:

the problem addressed

why this tool matters

expected outcomes

This makes notebooks teaching tools, not just code dumps.

🧪 3. Executable Code Cells

These demonstrate:

computations (e.g., computing spectral entropy)

data generation (e.g., simulation logs)

visualization (e.g., topology landscapes, decision traces)

Cells are intended to be run cell by cell in order.

📉 4. Visual Output + Interpretation

Plots are paired with explanatory text:

“This plot shows spectral entropy increasing as structures diverge”

“Blue line indicates risk score; red line indicates ethical constraint threshold”

🧠 5. Interactive Exploration Sections

Where possible, notebooks include:

cells where parameters can be modified

sliders or widgets (via ipywidgets)

live experimentation prompts

This is especially valuable for pedagogic notebooks.

🔍 6. Exercises & Extensions (Optional)

Some notebooks include:

suggested reader challenges

open questions

mini research prompts tied to CCIP

These help foster community learning.

🧠 Notebooks You Will Find
Filename	Focus
01_Topos_Intro.ipynb	Intro to topos and category logic
02_Spectral_Singularities.ipynb	Showcasing collision phenomena
03_Persistent_Homology.ipynb	Topological fingerprints
04_Phoneme_Topology.ipynb	Phonetic topology example
05_VSA_Binding_Unbinding.ipynb	Vector Symbolic Architectures
06_Emergency_Focus_Demo.ipynb	Difficulty metric, focus mode
07_Katrina_Simulation.ipynb	AGI causal reasoning simulation
08_Audit_and_Explainability.ipynb	Decision audit visualizations
🧪 Key Usage Workflows
🔹 Running a Notebook

Navigate to notebooks/.

Click the notebook file.

Run each cell in order:
Shift + Enter

Observe code outputs, plots, and commentary.

🧹 Restarting a Kernel

If execution fails due to memory or state:

Kernel ➜ Restart

Rerun from top

Always re-run top-down to ensure narrative context.

🔁 Version Control & Sync

Notebooks are JSON — avoid merge conflicts by:

Committing narrative/markdown first

Committing code cells next

Minimizing stale output

Running nbstripout pre-commit for clean diffs (optional)

Add to .gitignore:

*.ipynb_checkpoints/
🚀 Contributing Notebooks
🌱 Starting a New Notebook

cd notebooks

Create a new file: NEW_YourTopicName.ipynb

Use an existing notebook as template

Include:

Title cell

Narrative explanation

Modular code blocks

Results interpretation

📌 Document Dependencies

At the top of the notebook, include a block:

!pip install [libraries]

so future users can install required env easily.

Also save a matching entry in requirements.txt.

📊 Coding Best Practices in Notebooks

Follow these guidelines:

🧾 Narrative First

Introduce concepts before showing code.

Example:

“In this cell we compute spectral entropy to distinguish structures…”

🧹 Clean Code Cells

No long single cells

Break logic into readable chunks

Avoid global variables

📝 Inline Comments

Use comments to explain logic:

# compute spectral entropy from eigenvalues
H = -np.sum(p * np.log(p))
📂 Relative Paths

Use relative paths for loading data:

data = pd.read_json('../examples/sample_audit_log.json')

This ensures ports cleanly across forks.

📈 Visual Styles & Accessibility

Prefer:

✔ seaborn color palettes
✔ Clear axis labels
✔ Inline explanation of figures
✔ Accessibility-friendly colors

Example:

import seaborn as sns
sns.set_theme(style="whitegrid")
📌 Interactive Widgets (Optional)

Notebooks can include interactive controls:

import ipywidgets as widgets
from IPython.display import display

slider = widgets.IntSlider(min=1, max=10)
display(slider)

These are great for parameter exploration.

📦 Example: Load & Plot Decision Trace
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_json('../examples/decision_trace.json')

plt.plot(df['time'], df['risk_scores'])
plt.title('Risk Scores over Time')
plt.xlabel('Time')
plt.ylabel('Risk')
plt.show()
🧪 Testing Notebooks

Include test notebooks that focus on:

✔ Persistent homology correctness
✔ Spectral entropy invariants
✔ VSA binding/unbinding
✔ Crisis escalation logic

These notebooks can serve as unit tests + tutorials.

🧠 Best Practices for Review & Pull Requests

When submitting a notebook:

✔ Ensure narrative explains each step
✔ No hard-coded, unexplainable values
✔ Outputs are readable and relevant
✔ Add a short description in PR

📌 Final Notes

Notebooks should:

teach concepts

demonstrate workflows

invite experimentation

be reproducible

be auditable

They are living research artifacts, and one of the most important ways this project will communicate its ideas to the community.

Happy exploring! 🎓🚀


---

If you’d like next, I can also provide:

👉 a **notebook template skeleton** with starter cells & narrative blocks  
👉 a **requirements.txt** matching the notebooks  
👉 example notebook content (e.g., computing spectral entropy or visualizing the Katrina simulation)

Just tell me what you’d like next!
::contentReference[oaicite:0]{index=0}


