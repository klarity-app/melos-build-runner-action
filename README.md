# Melos Build Runner GitHub Action

A GitHub Action to automate and optimize the [Melos Build Runner](https://pub.dev/packages/melos) for Dart and Flutter projects. This action runs the build runner across your packages and caches the outputs to speed up subsequent runs.

## Features

- **Automated Build Runner Execution**: Streamlines the process of running the build runner in multi-package repositories managed by Melos.
- **Caching Mechanism**: Caches generated files to minimize redundant builds, improving overall CI/CD pipeline efficiency.
- **Customizable Melos Command**: Allows you to specify a custom Melos command to execute the build runner, providing maximum flexibility.

## Inputs

| Name           | Description                                                                        | Required | Default                                                                                                                    |
|----------------|------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| `output_paths` | Multiline list of output file paths generated by the build-runner. Each line represents a glob pattern for matching generated files. | `false`  | `**/*.g.dart`<br>`**/*.gr.dart`<br>`**/*.gen.dart`<br>`**/*generated.dart`<br>`**/*.mocks.dart`<br>`**/*.freezed.dart`<br>`**/*.io.dart` |
| `melos_command` | The full Melos command to execute the build runner.                                 | `false`  | `melos exec -c 1 --depends-on="build_runner" -- dart pub run build_runner build --delete-conflicting-outputs` |

## Usage

To use this action in your workflow, include the following step in your `.github/workflows/your-workflow.yml` file:
