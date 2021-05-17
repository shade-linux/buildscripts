# Template

Templates for buildscripts

## Make

```bash
# Setup
cd /usr/local/shade/etc/cache
# You may need to extract an archive
wget '<url>' # For direct downloads. You can replace this with a git clone
cd '<dir>'

# Building
./configure --prefix=/usr/local/shade
make

# Finalizing
make install
```

## Binary

```bash
# Setup
cd /usr/local/shade/etc/cache
# You may need to extract an archive
wget '<url>' # For direct downloads. You can replace this with a git clone
cd '<dir>'

# Finalizing
cp ./<binary> /usr/local/shade/bin/
```
