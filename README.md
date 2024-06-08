# GitHub CLI Extension: gh-cp


`gh-cp` is a GitHub CLI extension that allows you to easily copy files from a GitHub repository to a local destination. With `gh-cp`, you can seamlessly download specific files or multiple files from a repository, optionally specifying a branch or commit to copy from.


## Features

- Copy files from a GitHub repository to a local destination
- Support for copying multiple files in a single command
- Option to specify a branch or commit to copy files from
- Progress bar indication during file download
- Detailed error messages and guidance for resolving issues


## Installation

To install the `gh-cp` extension, follow these steps:

1. Ensure that you have [GitHub CLI](https://cli.github.com/) installed on your system.

2. Install the `gh-cp` extension using the following command:
   ```
   gh extension install MohamedElashri/gh-cp
   ```

   This command will clone the `gh-cp` repository to your local extensions directory and make it available as a `gh` command.

3. Verify the installation by running:
   ```
   gh cp --help
   ```

   If the installation is successful, you should see the help message for the `gh-cp` extension.

## Usage

The basic syntax for using `gh-cp` is as follows:

```
gh cp [OPTIONS] <repo> <paths>... <dest>
```

- `<repo>`: The repository in the format 'owner/repo'.
- `<paths>...`: The paths to the files in the repository (separated by space).
- `<dest>`: The local destination directory.

### Options

- `-h`, `--help`: Show the help message and exit.
- `-f`, `--file`: Read file paths from a file (one path per line).
- `-b`, `--branch <name>`: Specify the branch to copy files from (default: main).
- `-c`, `--commit <hash>`: Specify the commit hash to copy files from.

### Examples

1. Copy a single file from a repository:
   ```
   gh cp myuser/myrepo path/to/file.txt /local/directory
   ```

2. Copy multiple files from a repository:
   ```
   gh cp myuser/myrepo path/to/file1.txt path/to/file2.txt /local/directory
   ```

3. Copy files specified in a file:
   ```
   gh cp -f myuser/myrepo path_file.txt /local/directory
   ```

   The `path_file.txt` should contain file paths, one per line.

4. Copy files from a specific branch:
   ```
   gh cp -b feature-branch myuser/myrepo path/to/file.txt /local/directory
   ```

5. Copy files from a specific commit:
   ```
   gh cp -c a1b2c3d4 myuser/myrepo path/to/file.txt /local/directory
   ```

## Contributing

Contributions to `gh-cp` are welcome! If you encounter any issues, have suggestions for improvements, or would like to add new features, please open an issue or submit a pull request on the [GitHub repository](https://github.com/MohamedElashri/gh-cp).

## License

`gh-cp` is open-source software licensed under the [MIT License](https://github.com/MohamedElashri/gh-cp/blob/main/LICENSE).
