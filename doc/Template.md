# Template

Templates for buildscripts

## Make

```bash
# Setup
cd /shade/main/cache
# You may need to extract an archive
wget '<url>' # For direct downloads. You can replace this with a git clone
cd '<dir>'

# Building
./configure --prefix=/shade/etc/
make

# Finalizing
make install
```

## Binary

```bash
# Setup
cd /shade/main/cache
# You may need to extract an archive
wget '<url>' # For direct downloads. You can replace this with a git clone
cd '<dir>'

# Finalizing
cp ./<binary> /shade/etc/bin/
```
