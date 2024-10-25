# Melos Build Runner GitHub Action

A GitHub Action to automate and optimize the [Melos Build Runner](https://pub.dev/packages/melos) for Dart and Flutter projects. This action runs the build runner across your packages and caches the outputs to speed up subsequent runs.

## Features

- **Automated Build Runner Execution**: Streamlines the process of running the build runner in multi-package repositories managed by Melos.
- **Caching Mechanism**: Caches generated files to minimize redundant builds, improving overall CI/CD pipeline efficiency.
- **Customizable Build Commands**: Allows you to specify custom build runner commands as needed for your project.

## Inputs

| Name                 | Description                                                                                                            | Required | Default                                                         |
|----------------------|------------------------------------------------------------------------------------------------------------------------|----------|-----------------------------------------------------------------|
| `output_paths`       | Comma-separated list of output file paths or directories generated by the build runner.                                 | `true`   | N/A                                                             |
| `build_runner_command` | The build runner command to execute.                                                                                   | `false`  | `dart pub run build_runner build --delete-conflicting-outputs`  |

## Usage

To use this action in your workflow, include the following step in your `.github/workflows/your-workflow.yml` file:
