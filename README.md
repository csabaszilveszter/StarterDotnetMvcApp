# StarterDotnetMvcApp

A basic dotnet MVC starter repo for vscode
with [devcontainers](https://containers.dev/).

## Local setup with `.NET 6.0` already installed

Clone the repo like so:

```sh
git clone git@github.com:csabaszilveszter/StarterDotnetMvcApp.git
```

Start VSCode in the project:

```sh
cd StarterDotnetMvcApp

code .  # start vscode

# then restart in devcontainer (as vcsode offers it)
```

## Run `dotnet` cli in your shell without installing it

Create a shell `alias`:

- For **.NET 6.0 _(LTS)_** as is in this project:
  
  ```sh
  alias dotnet6='docker run --rm -w /$(basename $PWD) -v $PWD:/$(basename $PWD) mcr.microsoft.com/dotnet/sdk:6.0 dotnet'
  ```

You can add this to your `~/.bashrc` or `~/.zshrc` file to make
the alias persist across your shell sessions.

## VSCode with devcontainer

Check out [devcontainer.json](./.devcontainer/devcontainer.json) for more details.

To open this project follow the instructions [here](https://code.visualstudio.com/docs/devcontainers/containers#_quick-start-open-an-existing-folder-in-a-container) (from step **#4**).

## Running the app

Before trying to "press play" on vscode please run this otherwise .NET will complain:

```console
dotnet dev-certs https --trust
```
