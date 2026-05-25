# Contributing Guidelines & Development Setup

Thank you for your interest in contributing to Furio's Mods. To ensure a smooth development workflow across all repositories, we use a centralized path management system for the Vintage Story installation.

## Environment Setup

To compile the projects locally, the build system needs to know where your Vintage Story game files are located. You can configure this in one of two ways:

### Method 1: Local Configuration File (Recommended)
1. Copy the `Directory.Build.props.user.template` file from our central [.github/mod-template](https://github.com/Furio-s-Mods/.github/tree/main/mod-template) directory into the root folder of the specific mod repository you are working on.
2. Rename the copied file to `Directory.Build.props.user`.
3. Open the file and replace `[YOUR PATH HERE]` with the absolute path to your Vintage Story installation folder.
   * *Note: This file is already included in `.gitignore` and must never be committed to the repository.*

### Method 2: Environment Variable
Alternatively, you can define a system-wide environment variable named `VINTAGE_STORY` containing the absolute path to your Vintage Story installation directory. The build engine will automatically pick it up if no `.user` file is present.

## General Workflow

1. Fork the repository of the specific mod you want to update.
2. Setup your local paths using one of the methods above.
3. Apply your changes, ensuring code matches the target .NET version and style.
4. Submit a Pull Request describing your changes and the problem they solve.
