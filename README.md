# mac-openssl

Since Homebrew has disabled fetching openssl@1.1, 
this repository provides a way to download and install openssl@1.1 on macOS 
for those who still need it due to legacy dependencies.

## 📦 Download

```bash
curl -LO https://github.com/nanto88/mac-openssl/releases/download/v1.0/openssl-1.1.tar.gz
```

## Extract to Homebrew path manually 
### (or you can adjust your own directory)
```bash
sudo mkdir -p /opt/homebrew/opt
sudo tar -xzvf openssl-1.1.tar.gz -C /opt/homebrew/opt

export PATH="/opt/homebrew/opt/openssl@1.1/bin:$PATH"
export LDFLAGS="-L/opt/homebrew/opt/openssl@1.1/lib"
export CPPFLAGS="-I/opt/homebrew/opt/openssl@1.1/include"
export PKG_CONFIG_PATH="/opt/homebrew/opt/openssl@1.1/lib/pkgconfig"

source ~/.zshrc
```

## Verify
```bash
openssl version
```
Should return: OpenSSL 1.1.1w or similar
