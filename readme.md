# Workshop: Introduction to Docker

## Software Installation

### Windows 10 Pro / Mac OS X / Linux
1. Visit [https://www.docker.com/community-edition#/download](https://www.docker.com/community-edition#/download) and download Docker for Mac or Windows.
2. Follow the instructions on the website to install Docker on your computer.
3. Start `Docker`

### Installation for Windows 10 Home Edition
1. Visit [https://docs.docker.com/toolbox/toolbox_install_windows](https://docs.docker.com/toolbox/toolbox_install_windows) instead to download and install Docker Toolbox.
2. Ensure that you've verified your docker toolbox installation in step 3 on that page. The Docker CLI should be installed and accessible via Git Bash, and all console/terminal commands should be run Git Bash.

### Installation for Windows 10 Home Edition: Enabling Shared Volumes
1. Ensure that you've opened the Docker Quick Start Terminal before this.
2. Click on Start and run `Oracle VM VirtualBox`.
3. Select the `default` machine and click on `Settings`, then select `Shared Folders`. To mount folders in our docker containers later, we will have to first explicitly share folders with the docker machine here.
4. Click on the green + at the right to share a folder. Choose a folder for `Folder Path` in which you will create all your projects in, and give it a convenient name in lower case under `Folder Name`. For convenience in mounting volumes later, choose the drive that you will be creating your projects in for the `Folder Path` and give it a corresponding `Folder Name`, e.g. if your Windows user folder is in `D:`, then select `D:` as your `Folder Path` to share, and give it the name `d`. 
5. If you are planning to install and use docker from the Windows Subsystem for Linux later, you should also add your Windows user folder, e.g. `D:\Users\Tan Ah Teck`, and give it the name of your WSL home folder `/home/tanahteck`.
5. Ensure that `Auto-mount` and `Make Permanent` are both checked, then click on `ok`. You can now close `VirtualBox`.
6. In the Docker Quick Start Terminal, run `docker-machine restart` for the shared folder settings to take effect.

### (Optional for Windows 10 Users) Installing Docker in Windows Subsystem for Linux (WSL)

Check [wsl-docker.md](wsl-docker.md).

## Verify your docker installation

1. Open your `Console`.

2. Type: `docker -v`

	This should show you which version of Docker you have installed.

	This will be the primary way in which you will interact with your Docker environment.

3. Type: `docker info`

	This should show you a wall of text with info about your Docker daemon (or your Docker installation).

4. Type : `docker run hello-world`

   You should see
    ```
    Hello from Docker!
    This message shows that your installation appears to be working correctly.

    To generate this message, Docker took the following steps:
    1. The Docker client contacted the Docker daemon.
    2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
        (amd64)
    3. The Docker daemon created a new container from that image which runs the
        executable that produces the output you are currently reading.
    4. The Docker daemon streamed that output to the Docker client, which sent it
        to your terminal.

    .....
    ```

## Contributors

- [Jinny Wong](https://github.com/shujin)
- [Reuben Tan](https://github.com/natnebuer)
- [Michael Cheng](https://github.com//miccheng)
- [Kok Chee Kean](https://github.com/CKKOK)