# kube-secret

Find it tedious to have to individually base64 encode/decode and copy/paste K8s secrets? I do!

Wonder why none of the K8s toolchains seem to do this one simple thing? I do!

Want someone to make a tool that does this? I did!

## Requirements

* python
* pyyaml
    * `pip install pyyaml`

## Usage

1. `bin/kube-secret my-secret.yml`
2. Your system's editor will open a decoded tempfile for you to edit.
3. Save and exit.
4. `kube-secret` will have update the encoded values in the file for you.

## Caveats

* Currently only operates on YAML-formated secrets files that already exist, does not create new ones.
