# mac-openssl

curl -LO https://github.com/nanto88/mac-openssl/releases/download/v1.0/openssl-1.1.tar.gz


# mac-openssl

Precompiled and portable OpenSSL 1.1 for macOS (Apple Silicon / Intel). Useful for systems without Homebrew access.

## 📦 Download

```bash
curl -LO https://github.com/nanto88/mac-openssl/releases/download/v1.0/openssl-1.1.tar.gz
```

## Extract to Homebrew path manually
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
