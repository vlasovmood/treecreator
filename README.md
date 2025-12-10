# TreeCreator

Welcome to **TreeCreator** --- a powerful application that helps you
easily convert files into the desired format and generate a file tree!

## How it works

-   **Folder selection**: Specify the source folder containing the files
    and the folder where the converted files will be saved.
-   **Extension change**: You can change the extension of all files (for
    example, to `.txt` or `.json`).
-   **Optional: create `tree.json`**: The program can generate a JSON
    file containing a tree-like structure of the files.
-   **Progress tracking**: You can see the percentage of the conversion
    process.

## URL scheme support

-   **mainFolder** --- Select the main folder containing the files.
-   **exportFolder** --- The destination folder, for example a GitHub
    folder.
-   **file** --- File extension (for example `.txt` or `.json`).
-   **tree** --- Whether to create the `tree.json` file: yes/no.

**URL structure:**

    TreeCreator://mainFolder=[sourcePath]&exportFolder=[destinationPath]&file=[extension]&tree=[yes/no]

**Example link:**

    TreeCreator://mainFolder=C:/input&exportFolder=C:/output&file=txt&tree=yes

## Registering the URL scheme in Windows

1.  Open Registry Editor (`Win+R → regedit`).
2.  Navigate to `HKEY_CLASSES_ROOT`.
3.  Create a new key named `TreeCreator`.
4.  Inside it, create a key `shell`, then `open`, then `command`.
5.  In the `command` key, create a string value (default) with the path
    to the application:

```
"C:\Path\To\TreeCreator.exe" "%1"
```

## How to use

Use `TreeCreator.exe` to track changes in files. Create a repository on
GitHub and upload files there. `TreeCreator` helps quickly generate a
file tree, and GitHub displays changes in files.

[Download](https://github.com/Paramert/TreeCreator/releases/)
