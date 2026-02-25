# Pre-Requisites google Repositorys
```bash
mkdir -p ~/.local/bin
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.local/bin/repo
chmod a+x ~/.local/bin/repo
echo 'export PATH=~/.local/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
```

# Enable Build-Cache
```bash
export USE_CCACHE=1
export CCACHE_DIR=~/.ccache
ccache -M 100G

echo 'export USE_CCACHE=1' >> ~/.bashrc
echo 'export CCACHE_DIR=~/.ccache' >> ~/.bashrc
source ~/.bashrc
```

# Download
```bash
mkdir -p ~/Android/ && cd ~/Android/

repo init -u https://github.com/Smatek-DE/Android -b android-11.0

# 3. Sync (~30-40 Min, depends on internet connection)
repo sync -j$(nproc) -c
```
