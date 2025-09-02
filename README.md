# Agora Academy

This repository contains a modular pipeline for generating language course lesson scripts using Large Language Models (LLMs). The system is designed to automate the creation of structured lesson content, including grammar concepts, course outlines, and detailed lesson scripts, with support for multiple languages and CEFR levels. Try out the generated language courses for 3 language pairs on LearnWorlds:<br> https://agoravision.learnworlds.com

## Features

- **Automated Course Generation:** Generate full language courses, including grammar concepts, topic distributions, and lesson scripts.
- **Multi-Language Support:** Easily switch between source and target languages, including right-to-left (RTL) languages.
- **Customizable Prompts:** Modular prompt and format files for easy adaptation to new lesson types or structures.
- **Spaced Repetition:** Lessons and reviews are distributed using a spaced repetition algorithm for optimal learning.
- **Word Document Export:** Lesson scripts are exported as `.docx` files, with RTL support and automatic page numbering.
- **LLM Integration:** Supports multiple LLM providers (DeepSeek, Claude, Gemini, etc.) via OpenRouter API.

## Folder Structure

```
Agora-Academy/
├── Phase 1/
│   ├── script_generator_phase_1.ipynb
│   ├── distribution_analyzer.ipynb
│   ├── Prompts/
│   │   ├── ... (prompts as .txt files)
│   │   ├── ... (response formats as .json files)
│   └── Courses/
│       └── ... (generated output)
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.8+
- [Jupyter Notebook](https://jupyter.org/)
- [python-docx](https://python-docx.readthedocs.io/)
- [tqdm](https://tqdm.github.io/)
- [requests](https://docs.python-requests.org/)
- [matplotlib](https://matplotlib.org/)
- [numpy](https://numpy.org/)
- [seaborn](https://seaborn.pydata.org/)
- [scikit-learn](https://scikit-learn.org/)
- [pandas](https://pandas.pydata.org/)
- [wordcloud](https://pypi.org/project/wordcloud/)
- An [OpenRouter](https://openrouter.ai/) API key

### Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/Agora-Vision-ML/Agora-Academy.git
   cd Agora-Academy/Phase 1
   ```

2. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Set up your API key:**
   - Create a `.env` file in the root of `Phase 1/` similar to `.sample_env` and insert your OpenRouter API key:
     ```
     OPEN_ROUTER_API_KEY=[put_your_key_here]
     ```

4. **Edit the configuration:**
   - Open `script_generator_phase_1.ipynb` and set your desired `source_language`, `target_language`, `CEFR_level`, and `topic_of_interest` at the top of the notebook.

5. **Run the notebook:**
   - Launch Jupyter Notebook and run all cells in `script_generator_phase_1.ipynb`.
 
## Analysis
You can analyze the distribution of the language items using the `distribution_analyzer.ipynb` file.
   
 1. **Edit the configuration:**
    - Open `distribution_analyzer.ipynb` and set the path of your desired `file_to_analyze` at the top of the notebook.

 3. **Run the notebook:**
    - Launch Jupyter Notebook and run all cells in `distribution_analyzer.ipynb`.
   

## Customization

- **Prompts and Formats:** All prompt templates and JSON formats are stored in the `Prompts/` folder for easy editing.
- **Model Selection:** Choose your preferred LLM in the notebook by editing the `models` dictionary.
- **Output:** Generated courses and lesson scripts are saved in the `Courses/` directory.

## Example Output

- Lesson scripts are generated `.docx` files, ready to be recorded and used in audio-based language courses.
- A sample course has been generated for teaching Kurdish Sorani for English listeners, and placed in the `Courses/` directory for reference.
