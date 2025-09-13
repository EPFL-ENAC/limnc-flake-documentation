# Updating the documentation

To update the documentation, follow these steps:

1. Make sure you have the latest version of the documentation repository.
2. Fork the repository on GitHub.
3. Create a new branch for your changes.
4. Make your changes to the documentation files, either on GitHub or locally after cloning the forked repository (recommended). If you create a new page in guides, add the name of the new page to `guides/index.md` and to`mkdocs.yml` (section `nav`).
5. Test your changes locally to ensure they work as expected: 
    1. install the python package mkdocs with `pip install mkdocs`
    2. in the python console, move to the local repository of the documentation and run `mkdocs serve`
    3. copy-paste the http link from the console to a web browser to visualize the website
    4. keep mkdocs running while making changes to the documentation (changes are automatically made to the website preview on the browser).
6. Commit your changes and push the branch to the remote repository.
7. Create a pull request to merge your changes into the main branch of the documentation repository.
8. Before making any additional change locally, make sure to (1) synchronize the forked repository with the original one and (2) pull the remote branch to the local repository. 
