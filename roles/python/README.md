# Install python with pyenv

The commands boil down to:

```sh
CC="clang" \
CFLAGS="-I/usr/local/opt/readline/include -I/usr/local/opt/openssl/include -I/Library/Developer/CommandLineTools/SDKs/MacOSX10.14.sdk/usr/include" \
LDFLAGS="-L/usr/local/opt/readline/lib -L/usr/local/opt/openssl/lib" \
PYTHON_CONFIGURE_OPTS="--enable-framework --enable-framework=/Users/cgilmer/.pyenv/versions/3.7.2" \
pyenv install -s 3.7.2
```

Or:

```sh
CC="clang" \
CFLAGS="-I$(brew --prefix readline)/include -I$(brew --prefix openssl)/include -I$(xcrun --show-sdk-path)/usr/include" \
LDFLAGS="-L$(brew --prefix readline)/lib -L$(brew --prefix openssl)/lib" \
PYTHON_CONFIGURE_OPTS="--enable-framework --enable-framework=/Users/cgilmer/.pyenv/versions/3.7.2" \
pyenv install -s 3.7.2
```
