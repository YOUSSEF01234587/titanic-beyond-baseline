# Contributing to Titanic: Beyond Baseline

Thank you for considering contributing! This document provides guidelines and instructions for contributing.

---

## How to Contribute

### Reporting Issues

If you find a bug or have a suggestion:

1. Check if the issue already exists in [GitHub Issues](https://github.com/YOUSSEF01234587/titanic-beyond-baseline/issues)
2. If not, create a new issue with:
   - A clear, descriptive title
   - Steps to reproduce (if applicable)
   - Expected vs actual behavior
   - Your environment (Python version, OS, etc.)

### Suggesting Enhancements

For feature requests or improvements:

1. Open an issue describing the enhancement
2. Explain why it would be useful
3. Include any relevant references or examples

### Pull Requests

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Run tests if applicable
5. Commit with a clear message
6. Push to your branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

---

## Development Setup

### Prerequisites

- Python 3.10+
- Git
- Jupyter Notebook or JupyterLab

### Installation

```bash
# Clone your fork
git clone https://github.com/YOUSSEF01234587/titanic-beyond-baseline.git
cd titanic-beyond-baseline

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt
```

---

## Code Standards

### Python Style

- Follow [PEP 8](https://peps.python.org/pep-0008/) style guidelines
- Use meaningful variable and function names
- Add docstrings to functions and classes
- Keep functions focused and concise

### Notebook Guidelines

- **Do not modify the main notebook** unless you are fixing a critical bug
- Use the design system (Cell 5) for all new visualizations
- Follow the existing cell structure and naming conventions
- Include clear markdown explanations between code cells

### Commit Messages

- Use clear, descriptive commit messages
- Start with a verb in imperative mood (Add, Fix, Update, etc.)
- Keep the subject line under 50 characters
- Add a body for complex changes

Examples:
```
Add confusion matrix visualization
Fix threshold optimization bug
Update requirements.txt with new dependencies
```

---

## Testing

### Running the Notebook

```bash
# Run the full notebook
jupyter notebook notebook/titanic-beyond-baseline.ipynb

# Or use nbconvert
jupyter nbconvert --to notebook --execute notebook/titanic-beyond-baseline.ipynb
```

### Verification

Before submitting a PR:

1. Ensure the notebook runs without errors
2. Verify all visualizations render correctly
3. Check that submission files are generated
4. Test on both Kaggle and local environments (if possible)

---

## Adding Visualizations

If you want to add new visualizations:

1. Use the design system functions from Cell 5
2. Apply consistent styling with `apply_chart_layout()`
3. Include descriptive titles and subtitles
4. Add source attribution
5. Save screenshots to `images/` folder
6. Update the README with the new image

---

## Documentation

- Update `README.md` for new features
- Add docstrings to new functions
- Update `PROJECT_STRUCTURE.md` for structural changes
- Include examples where helpful

---

## Code of Conduct

Please follow our [Code of Conduct](CODE_OF_CONDUCT.md) in all interactions.

---

## Questions?

If you have questions about contributing, feel free to open an issue or reach out.

---

Thank you for contributing!
