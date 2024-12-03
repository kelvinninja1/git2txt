# git2txt Documentation

## Description

git2txt is a command-line tool that converts GitHub repositories into readable text files. It clones a GitHub repository, processes its text files, and combines them into a single output file. This tool is useful for code review, analysis, and documentation purposes.

## Installation

To install git2txt globally using npm, run the following command:

```bash
npm install -g git2txt
```

## Usage

You can specify the repository in several formats:

```bash
# Full HTTPS URL
git2txt https://github.com/username/repository

# Short format (username/repository)
git2txt username/repository

# SSH format
git2txt git@github.com:username/repository
```

### URL Format Support

The tool accepts these GitHub repository URL formats:

- HTTPS URLs: `https://github.com/username/repository`
- Short format: `username/repository`
- SSH URLs: `git@github.com:username/repository`
- URLs with or without `.git` suffix
- URLs with or without trailing slashes

### Options

```
--output, -o     Specify output file path (default: repo-name.txt)
--threshold, -t  Set file size threshold in MB (default: 0.1)
--include-all    Include all files regardless of size or type
--debug         Enable debug mode with verbose logging
--help          Show help
--version       Show version
```

### Examples

Download and convert a repository using different formats:
```bash
# Using HTTPS URL
git2txt https://github.com/username/repository

# Using short format
git2txt username/repository

# Using SSH URL
git2txt git@github.com:username/repository

# With custom output file
git2txt username/repository --output=output.txt

# With custom file size threshold (2MB)
git2txt username/repository --threshold=2

# Include all files (no size/type filtering)
git2txt username/repository --include-all

# Enable debug output
git2txt username/repository --debug
```
