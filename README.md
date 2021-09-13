# vscode releases

## Getting started

### Installation instructions

You can download the latest release for your platform from the [GitHub release page](https://github.com/gitpod-io/vscode/releases/latest).

### Starting the VS Code Server

#### Linux

First, untar the downloaded archive.

```bash
tar -xzf code-web-server-v*.tar.gz

```

Then, run the web server.

```bash
cd code-web-server-v*-x64
./startup.sh
```

### Docker

#### Starting the container
When using these commands, you can add a `-d` to the end of the command to detach from the container after starting it. This will make it run as a daemon in the background.

```bash
# Linux, macOS, or PowerShell
docker run -it --init -p 3000:3000 -v "$(pwd):/home/workspace:cached" gitpod/vscode

# Windows (cmd.exe)
docker run -it --init -p 3000:3000 -v "%cd%:/home/workspace:cached" gitpod/vscode
```

After this, visit [localhost:3000](http://localhost:3000).

#### Building the image
```bash
docker build -t gitpod/vscode .
```
