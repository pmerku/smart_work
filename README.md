## Dockerized dev

This is my custom development environment for `C`, `NASM` and `PYTHON` projects. \
Make sure you have `docker cli` and `docker-compose` installed.

### Installation

Please run the following:

```
git clone git://pmerku/smart_work.git ~/smart_work
cd ~/smart_work
docker-compose build
```

### Usage

The images are now build and you can use them with these commands in your project root directory:

```
docker run -it --rm --init -v "$PWD:/pwd" pmerku/clang sh -c "cd /pwd; zsh"
docker run -it --rm --init -v "$PWD:/pwd" pmerku/python sh -c "cd /pwd; zsh"
```

### Debug mode

You can switch to the debug version of the clang docker image by changing ``dev``  to ``debug`` in \
the `docker-compose.yaml` file and rebuilding the image

```
    build:
        context: ./clang
        target: dev      <--- HERE
```
