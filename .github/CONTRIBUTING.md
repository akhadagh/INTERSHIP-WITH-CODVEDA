# Contributing Guidelines

## Welcome Contributors! 👋

Thank you for interest in contributing to the Data Analytics Internship Project. This document provides guidelines for contributions.

---

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [How to Contribute](#how-to-contribute)
3. [Development Setup](#development-setup)
4. [Coding Standards](#coding-standards)
5. [Commit Guidelines](#commit-guidelines)
6. [Pull Request Process](#pull-request-process)
7. [Reporting Issues](#reporting-issues)

---

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inspiring community for all. We expect all contributors to:

- Be respectful and inclusive
- Provide constructive feedback
- Focus on what is best for the community
- Show empathy towards other community members

### Unacceptable Behavior

- Harassment or discrimination
- Offensive comments or trolling
- Public or private attacks
- Publishing private information
- Other conduct deemed inappropriate

---

## How to Contribute

### Ways to Contribute

1. **Improve Documentation**
   - Fix typos
   - Clarify explanations
   - Add examples
   - Improve diagrams

2. **Add Features**
   - New analysis techniques
   - Additional models
   - Extended datasets
   - Advanced visualizations

3. **Fix Bugs**
   - Report issues you find
   - Propose fixes
   - Test solutions

4. **Enhance Code Quality**
   - Refactor for clarity
   - Improve performance
   - Add comments/docstrings
   - Write tests

5. **Share Knowledge**
   - Tutorials
   - How-to guides
   - Best practices
   - Real-world examples

---

## Development Setup

### Prerequisites

- Python 3.8+
- Git
- Jupyter Notebook or JupyterLab
- Virtual environment (recommended)

### Local Setup

```bash
# 1. Fork and clone
git clone https://github.com/YOUR-USERNAME/Data-Analytics-Internship.git
cd Data-Analytics-Internship

# 2. Create feature branch
git checkout -b feature/your-feature-name

# 3. Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 4. Install dependencies
pip install -r requirements.txt

# 5. Start developing!
jupyter notebook
```

---

## Coding Standards

### Python Code Style

Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/):

```python
# Good: Clear, well-documented
def calculate_model_metrics(y_true, y_pred):
    """
    Calculate classification metrics.
    
    Parameters:
    -----------
    y_true : array-like
        True labels
    y_pred : array-like
        Predicted labels
    
    Returns:
    --------
    dict : Dictionary containing accuracy, precision, recall, F1-score
    """
    accuracy = (y_true == y_pred).mean()
    precision = precision_score(y_true, y_pred, average='weighted')
    recall = recall_score(y_true, y_pred, average='weighted')
    f1 = f1_score(y_true, y_pred, average='weighted')
    
    return {
        'accuracy': accuracy,
        'precision': precision,
        'recall': recall,
        'f1': f1
    }
```

### Notebook Standards

1. **Cell Organization**
   - Title and description at top
   - Clear section headers
   - Logical code flow
   - Output descriptions

2. **Markdown Documentation**
   - Explain purpose of each section
   - Document assumptions
   - Note important findings
   - Add visualizations where helpful

3. **Code Cells**
   - One logical concept per cell
   - Clear variable names
   - Comments for complex logic
   - Print statements for checkpoints

### Variable Naming

```python
# Good
model_accuracy = 0.95
feature_importance_df = pd.DataFrame(...)
is_production_ready = True

# Avoid
ma = 0.95
fi = pd.DataFrame(...)
prod = True
```

---

## Commit Guidelines

### Message Format

```
[TAG] Brief description (50 chars max)

Optional detailed description (wrap at 72 chars)
- Use bullet points for multiple changes
- Reference related issues
- Explain WHY not just WHAT

Example:
[FEAT] Add XGBoost classifier model

Implements XGBoost for improved performance over Random Forest.
- Achieves 98.2% accuracy on Iris dataset
- Reduces training time by 40%
- Adds hyperparameter tuning notebook
- Resolves #45
```

### Tags

- `[FEAT]` - New feature/analysis
- `[FIX]` - Bug fix
- `[DOCS]` - Documentation update
- `[REFACTOR]` - Code refactoring
- `[TEST]` - Test addition/modification
- `[DATA]` - Dataset changes
- `[PERF]` - Performance improvement
- `[STYLE]` - Code style updates

### Commit Best Practices

✓ Commit frequently with logical chunks  
✓ Write descriptive messages  
✓ Reference issues when applicable  
✓ Keep commits focused and atomic  
✓ Don't commit sensitive information  

---

## Pull Request Process

### Before Starting

1. Check for existing issues/PRs
2. Discuss major changes (create issue first)
3. Fork the repository
4. Create feature branch from `main`

### Creating a PR

```bash
# Make changes and commit
git add .
git commit -m "[FEAT] Your feature"

# Push to your fork
git push origin feature/your-feature-name

# Go to GitHub and create Pull Request
```

### PR Description Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement

## Related Issues
Fixes #123

## Testing
- [ ] Added/updated tests
- [ ] Verified on local machine
- [ ] Results consistent with expectations

## Checklist
- [ ] Code follows style guidelines
- [ ] Documentation updated
- [ ] No new warnings generated
- [ ] Tests pass locally
```

### PR Review Process

1. **Automated Checks**
   - Code style (flake8, pylint)
   - Tests pass
   - Coverage maintained

2. **Manual Review**
   - Code quality
   - Logic correctness
   - Documentation clarity
   - Performance impact

3. **Feedback**
   - Address comments
   - Push additional commits
   - Request re-review

4. **Merge**
   - Squash commits if desired
   - Merge to main
   - Delete feature branch

---

## Reporting Issues

### Creating an Issue

Use the issue template on GitHub:

```markdown
## Description
What is the issue?

## Steps to Reproduce
1. Step 1
2. Step 2
3. etc.

## Expected Behavior
What should happen?

## Actual Behavior
What actually happens?

## Environment
- Python version: 3.9
- OS: Ubuntu 20.04
- Package versions: pandas==1.3.0, sklearn==0.24.2

## Possible Solution
Optional suggestions
```

### Issue Labels

- `bug` - Something isn't working
- `enhancement` - Feature request
- `documentation` - Docs improvement
- `good first issue` - Good for new contributors
- `help wanted` - Need assistance
- `question` - Ask for clarification

---

## Tips for Success

### For First-Time Contributors

1. **Start small**: Bug fixes or documentation
2. **Read existing code**: Understand patterns
3. **Ask questions**: Comment on issues
4. **Test thoroughly**: Verify before submitting
5. **Be patient**: Review takes time

### Code Review Tips

- Be constructive and kind
- Suggest improvements, not demands
- Praise good work
- Provide examples
- Be responsive to feedback

### Common Mistakes to Avoid

- ✗ Large PRs (split into smaller pieces)
- ✗ No documentation
- ✗ Missing tests
- ✗ Cryptic commit messages
- ✗ Changing unrelated code

---

## Resources

- [GitHub Contributing Guide](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository)
- [Open Source Guide](https://opensource.guide/)
- [First Contributions](https://github.com/firstcontributions/first-contributions)
- [Git Documentation](https://git-scm.com/doc)

---

## Questions?

Feel free to:
- Comment on issues
- Open discussions
- Contact maintainers
- Check documentation

---

## Thank You!

We appreciate your contributions to making this project better for everyone. Together we build better data science education! 🚀

---

**Last Updated**: June 2026  
**Maintained By**: Codveda Data Analytics Team
