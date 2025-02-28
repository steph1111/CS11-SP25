<h1 align="center">CS11-SP25</h1>
<h3 align="center">CS11 Spring 25 Supplemental Instruction GitHub</h3>


# Getting started
## 0.1 Installing git (WSL)
1. Confirm git is installed by running the following command in your terminal
    ```sh
    git --version
    ```
    You should get back something that looks like `git version 2.39.0` 
2. If you did not receive a similar message run the following command.
    ```sh
    sudo apt-get install git
    ```

## 0.2 Installing git (Cygwin)
If you have Cygwin on your windows device, when you were installing, Cygwin gave you the option to install additional packages, one of these was for Git. Chances are you did not install this, but we can add packages after installation (kinda). There is no package management in Cygwin outside of the setup program, so you will have to run `setup-x86_64.exe` again. 
1. Open `File Explore` then to `Downloads` on your device
2. Search for `setup-x86_64.exe` and open the file
3. Go through the set up process again (choose the same options as last time) until you reach the `Select Packages` page. Here use the search tool to search for "Git". Choose the package named `Git` with description `Distributed version control system`
    ![packages](https://github.com/steph1111/F23_CS11_SI/assets/96219204/05954a94-ad7e-4596-855d-8a042905df34)
    Note: now is a good time to install any additional packages you may want like Vim
4. Finish the rest of the set up process
5. Open your Cygwin terminal and confirm git has been properly installed by running
    ```sh
    git --version
    ```
    You should get back something that looks like `git version 2.39.0`

<br>

## 0.3 Installing git (Mac and Linux)
1. By default, git should be installed on Mac and Linux systems
2. Confirm git is installed by running the following command in your terminal
    ```sh
    git --version
    ```
    You should get back something that looks like `git version 2.39.0`
3. If you did not get a version number, follow the this guide: [Install Git](https://github.com/git-guides/install-git)

<br>

## 1 Create a GitHub account
GitHub is the free web based platform we and many other software engineers use to share and collaborate on projects as well as control version history.
<img width="1440" alt="Screen Shot 2023-09-10 at 7 39 35 AM" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/0ed2d5d9-7b63-4953-8a56-3bfe7901db79">


1. Go to [GitHub](https://github.com/) and follow the steps to create an account
2. Return to the terminal (cygwin or your standard terminal) to configure git
3. Set up your username using the following command where `<your_GitHub_username>` is the username you chose when creating your GitHub account
    ```sh
    git config --global user.name <your_GitHub_username>
    ```
     ```sh
    git config --global user.name CS11SI
    ```
4. Set up your email using the following command where `<your_GitHub_email>` is the email you used when creating your GitHub account
    ```sh
    git config --global user.email <your_GitHub_email>
    ```
     ```sh
    git config --global user.email stlheure@cabrillo.edu
    ```

<br>

## 2.1 Set up SSH (Cygwin)
1. Open Cygwin as Administrator and enter the following command to configure SSH
    ```sh
    ssh-host-config
    ```
2. Enter yes for the prompts 
3. You will be prompted to with the text below
    <div><pre style="margin: 0; line-height: 125%"><span style="color: #DA70D6">***Query:</span><span style="color: white"> Enter the value CYGWIN for the daemon: []</span></div>

    For the value enter `ntsec`
    <div><pre style="margin: 0; line-height: 125%"><span style="color: #DA70D6">***Query:</span><span style="color: white"> Enter the value CYGWIN for the daemon: [] ntsec</span></div>

<br>

## 2.2 Set up SSH (Mac, Linux, WSL)
1. SSH should already be on Mac and Linux systems

<br>

## 3 Generate an SSH key
1. Generate an SSH key to connect your system to your GitHub account
    ```sh
    ssh-keygen
    ```
    - When it asks for the location to put the file hit enter 
    - Also just hit enter when it asks for the password, unless you can remember it (not recommended)
2. Copy the generated ssh key
    ```sh
    cat ~/.ssh/id_rsa.pub
    ```

<br>

## 4 Add the SSH key to GitHub
1. Return to GitHub and open your settings by clicking on your icon then ⚙️ `settings`
2. Scroll to  🔑 `SSH and GPG keys`

   <img width="300" alt="Tabs" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/43005ec1-80b4-4a11-8659-41eff2ee83b7">

4. Click the <img width="80" alt="New SSH Key" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/7529cd77-805d-4df4-a24d-e10786648852"> button located in the top right corner.
1. Choose a name for the key (something such that you'll remember what computer/system it was for)
2. Paste the key from step 2 into the `Key` box
3. Save the key by clicking <img width="80" alt="Add SSH Key" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/cb49a8b5-7d60-4498-9595-57634f3f6bba">

<br>

## 5 Fork the repo to your account
1. Open the `CS11-SP25` GitHub repo in your browser: https://github.com/steph1111/CS11-SP25
2. At the top of the page click on <img width="80" alt="fork" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/007c608d-9d06-4db9-bee0-eaae1cd0343d">

    <img width="582" alt="fork" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/80964a3a-e63b-4433-a070-0b69f7c4e747">

3. Follow the steps to fork the repo to your account by creating a new fork. Click on <img width="80" alt="create fork" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/575eb007-7936-40eb-9bbd-2d26490876cf"> when you are finished. This creates your own personal version of this repository

    <img width="582" alt="fork page" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/34ac40e0-c3e2-4717-9050-9fc804b8cf4a">

<br>

## 6 Clone your forked repo to your system
1. Open your forked repo. At the top of the page click the green <img width="70" alt="code" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/e6ab5cd8-2adf-44bd-8dab-865fefea6429">
 button. Open the SSH tab and copy the link

      <img width="364" alt="Screen Shot 2023-09-10 at 6 50 51 PM" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/477b25d6-1944-47e7-a0ea-507461b5d0cb">

2. Return to your terminal and navigate using `cd` to where you would like this repo contents to live with your file system
3. To clone your repo use the `git clone` command and paste the link from step 1. This points to the existing repo on GitHub and makes a connected copy, or clone, on your system
    ```sh
    git clone <link_here>
    ```
    Here is an example of how I would clone my repo (your link is different)
    ```sh
    git clone git@github.com:steph1111/CS11-SP25.git
    ```
4. To confirm the clone was successful list your files with `ls`. You should see the name of the cloned repo in your current directory

<br>

# Maintaining your repo

## 0 Sync and pull the changes
I will be updating my upstream version of your repo before SI sessions to add new content. In order to get the new content into your forked repo you must sync and pull the changes. *Every time* you want to work on your repo I recommend heading to your forked repo and seeing if there are upstream changes to be synced and pulled
1. Open your forked repo in GitHub. If there are no changes you should see a message that looks like the following stating this branch is up to date. If this is the case it means I have not made changes and you can ignore the following steps.
    ![up_to_date](https://github.com/steph1111/F23_CS11_SI/assets/96219204/a67537ba-91e8-4ec6-907d-8181b769b281)

2. If there are upstream changes to merge there should be a message on this page similar to the following:
    ![x_commits_behind](https://github.com/steph1111/F23_CS11_SI/assets/96219204/786f9c39-25de-4fd2-8b2b-2012b332646d)
   This means I have main changes to the upstream repo that need to be synced to your fork
3. Click on the button titled 🔄 `Sync fork`, you should see a window stating the code is out of date. Click <img width="80" alt="update branch" src="https://github.com/steph1111/F23_CS11_SI/assets/96219204/3330cd21-db4f-4ed4-9803-36796deea681">

4. Next navigate to your fork on your system 
5. Enter the command `git pull` to pull the changes on GitHub onto your device
   ```sh
   git pull
   ```
6.  Work on the exercises as you would any code on your device

<br>

## 1 Add changes
Once you make some changes you would like to be documented you need to start by `add`ing them. 
1. Add a singular file
    ```sh
    git add file_name
    ```
2. Add all files modified
    ```sh
    git add .
    ```

## 2 Commit your changes
Committing changes is how you can mark versions of your code you would like to be tracked. It is a good idea to commit changes before and after you add/remove a feature that way there is a record of your changes. Also commit changes after you have finished a session of programming then `push` (see following section)
1. To commit changes you use the `git commit` command. The parts of the command are as follows:
     - `git`: Denotes we are using a git command 
     - `commit`: The name of the command is commit, this is what we would like to do
     - `-m`: This is a flag that says we would like to add a commit message
     - `"Message here`: Between quotes state what changes you are committing 
     
     All together the git commit command syntax looks like this:
     ```sh
     git commit -m "Message here" 
     ```
     An example commit may be
     ```sh
     git commit -m "Added endl to move to the next line"
     ```
2. You will receive a short message summarizing the changes

<br>

## 3 Push your changes
Once you have finished a coding session it is a good idea to `push` your commits. The `push` command is basically the opposite of `pull`. `push` takes the changes (commits) you made on your local system and sends them to GitHub.
1. Add and commit your changes (see above)
2. Enter the command `git push` to push the changes from your system to GitHub
3. You can confirm this worked by heading to GitHub and seeing the changes reflected on your repo page
    ```sh 
    git pull
    ```
