[🇬🇧 English](CONTRIBUTING.md) | [🇷🇺 Русский](CONTRIBUTING_RU.md)

# Contributing to WakeLink

First off, thank you for considering contributing to WakeLink! It's people like you that make WakeLink such a great tool.

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible.

**Report bugs in the appropriate repository:**

| Issue Type | Repository |
|:-----------|:-----------|
| Cryptography / Protocol | [ewsp-core](https://github.com/wakelinkdev/ewsp-core/issues) |
| ESP Firmware | [firmware](https://github.com/wakelinkdev/firmware/issues) |
| CLI Client | [cli](https://github.com/wakelinkdev/cli/issues) |
| Android App | [android](https://github.com/wakelinkdev/android/issues) |
| Multiplatform App | [multiplatform](https://github.com/wakelinkdev/multiplatform/issues) |
| Documentation | [docs](https://github.com/wakelinkdev/docs/issues) |

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. Create an issue in the appropriate repository and provide:

- A clear and descriptive title
- A detailed description of the proposed enhancement
- Explain why this enhancement would be useful

### Pull Requests

1. Fork the repo and create your branch from `main`
2. If you've added code that should be tested, add tests
3. If you've changed APIs, update the documentation
4. Ensure the test suite passes
5. Make sure your code lints
6. Issue that pull request!

## Development Setup

### ewsp-core (C)

```bash
git clone https://github.com/wakelinkdev/ewsp-core.git
cd ewsp-core
mkdir build && cd build
cmake .. -DEWSP_BUILD_TESTS=ON
cmake --build .
ctest -V
```

### wakelink-client (Python)

```bash
git clone https://github.com/wakelinkdev/cli.git
cd cli
pip install -e ".[dev]"
pytest
mypy core/
```

### wakelink-android (Kotlin)

```bash
git clone https://github.com/wakelinkdev/android.git
cd android
./gradlew build
./gradlew test
```

## Style Guides

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

**Commit types:**
- `feat:` A new feature
- `fix:` A bug fix
- `docs:` Documentation only changes
- `style:` Code style changes (formatting, etc)
- `refactor:` Code change that neither fixes a bug nor adds a feature
- `perf:` Performance improvement
- `test:` Adding missing tests
- `chore:` Changes to the build process or auxiliary tools

### C Code Style (ewsp-core)

- 4 spaces for indentation
- Function names: `ewsp_snake_case()`
- Macros: `EWSP_UPPER_CASE`
- All public functions must have documentation

### Python Code Style (wakelink-client)

- Follow PEP 8
- Use type hints
- Docstrings for all public functions
- Run `black` and `isort` before committing

### Kotlin Code Style

- Follow Kotlin coding conventions
- Use `ktlint` for formatting

## Security

**Do not open public issues for security vulnerabilities.**

Please email **security@wakelink.io** instead. See [SECURITY.md](SECURITY.md) for details.

## Questions?

Feel free to open a discussion in the appropriate repository or contact the maintainers.

---

Thank you for contributing! 🎉
