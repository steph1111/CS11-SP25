# Instructions
**Objective:** Make your first commit to git.

## Background information 
Ensure you have followed the instructions to set up Git and GitHub located on the repo [home page](https://github.com/steph1111/CS11-SP25).  

## Instructions
1. Ensure your fork of the `CS11-SP25` repo is up to date.
1. Navigate to the file located at `CS11-SP25/week_2/ex00/hello.cpp`.
1. Replace the text `[your github username]` with the GitHub user name you created.
    ```cpp
    cout << "Welcome to GitHub steph1111!\n";
    ```
1. Add the file to your local git using the add command.
    <details>
      <summary>Hint?</summary>

      ```sh
      git add hello.cpp
      ```
    </details>
    </br>

1. Commit your changes with a message describing what you changed.
    <details>
      <summary>Hint?</summary>

      ```sh
      git commit -m "Added my github username to the output."
      ```
    </details>
    </br>

1. See which files you will be committing with `git status`
    ```sh
    git status
    ```

1. Push your changes to GitHub.
    <details>
      <summary>Hint?</summary>

      ```sh
      git push
      ```
    </details>
    </br>

1. Go to the web GitHub interface and see if your changes were reflected on your fork.