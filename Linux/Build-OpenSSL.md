# Build #
- Config
```
./config --prefix=/usr/local/ssl --openssldir=/usr/local/ssl shared
```
- Make & Install
```
sudo make && sudo make install
```

# Trouble shooting #
- Can't locate IPC/Cmd.pm in @INC

```
yum install perl-IPC-Cmd
```
