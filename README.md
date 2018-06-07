# Managing vim

Deploy
```bash
cd ~
git clone --recursive https://github.com/epage/vimfiles.git .vim
cp .vim/extra/.vimrc ~/
cp .vim/extra/.gitconfig ~/
```
Note: be sure to set the email address in `.gitconfig`.

Add
```bash
cd ~/.vim/bundle
git submodule add REPO
```

Update
```bash
cd ~/.vim
git submodule foreach git pull origin master
git add bundle

# Or is it
git submodule update --recursive
```

# Machine setup

## Windows, elevated

```bash
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
choco install elevate
```

## Windows, non-elevated

```bash
elevate choco install git
elevate choco install 7zip
elevate choco install ripgrep
elevate choco install steam
elevate choco install vim
elevate choco install ConEmu
elevate choco install vcxsrv
elevate choco install winmerge
rem For Work
elevate choco install insted
elevate choco install p4v
```

## Linux

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get build-essetial pkg-config libssl-dev cmake curl
curl https://sh.rustup.rs -sSf | sh
source ~/.cargo/env
cargo install ripgrep
```


## Regular prompt

```bash
rustup install beta
rustup install nightly
rustup run nightly cargo install clippy
cargo install rustfmt --ver 0.8.6
cargo install fd-find
cargo install cargo-tree
cargo-install cargo-outdated
cargo install cargo-llvm-lines
```
