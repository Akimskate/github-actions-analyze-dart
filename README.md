# GitHub Action — Analyze Flutter

This GitHub Action (written in composite run steps) allows you to leverage GitHub Actions to analyze your Flutter project's Dart code.

## Usage
### Pre-requisites
Create a workflow `.yml` file in your `.github/workflows` directory. An [example workflow](#example-workflow---create-a-release) is available below. For more information, reference the GitHub Help Documentation for [Creating a workflow file](https://help.github.com/en/articles/configuring-a-workflow#creating-a-workflow-file).

### Inputs
None.

### Outputs
None.

### Common workflow

1. Your workflow must install Flutter before using this action. Suggestion: [Flutter action](https://github.com/marketplace/actions/flutter-action).
2. Use the action. For example:
```yaml
on: push

name: Sample Workflow

jobs:
  build:
    name: Examaple
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Set up Flutter
        uses: subosito/flutter-action@v1
      - name: Analyze Flutter
        use: zgosalvez/github-actions-analyze-flutter@v1
```

## License
The scripts and documentation in this project are released under the [MIT License](LICENSE)