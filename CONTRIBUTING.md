## Package Management

Uploading to PyPI
```python
# Install setuptools and wheel
python3 -m pip install --user --upgrade setuptools wheel

# Run from setup.py directory
python3 setup.py sdist bdist_wheel

# Files will be generated in the dist directory
dist/
  example_pkg_your_username-0.0.1-py3-none-any.whl
  example_pkg_your_username-0.0.1.tar.gz
  
# Install Twine
python3 -m pip install --user --upgrade twine

# Upload to Test
python3 -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*

# Upload to PyPI
python3 -m twine upload dist/*

# Install from Test
python3 -m pip install --index-url https://test.pypi.org/simple/ example-pkg-your-username

# Install from PyPI
python3 -m pip install example-pkg-your-username

```

## Travis Testing
To be implemented.
