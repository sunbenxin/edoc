issue:
    two separate projects yet still be able to use one from winth the other
    1. including the library (diffcult to customize the library more diffcult to deploy)
    2. vendoring the code(any custom changes are diffcult to merge when upstream changes become available)

git submodules allow you to keep a Git repository as a subdirectory of another Git repository
lets you clone another repository into your project and keep your commits separate


commands:
    1. add an existing Git repository as a submodule of a repository.
        git submodule add <URL>
    2. clone a repository with submodules
        git clone <URL>
        git submodule init
        git submodule update

        or 
        git clone --recursive <URL>
    3. working a project with submodules
        a: pulling in upstream changes
            pull from subrepository
            if you commit at this point then you will lock the submodule into having the new code when other people update
        (git submodule update --remote)
    4. working on submodule
