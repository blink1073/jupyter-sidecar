# jupyter-sidecar
Little side display of Jupyter kernel rich output

## Building

This package requires iojs and zmq.

Install ZeroMQ headers for your platform.
Install iojs

Install node-gyp:

```
npm install -g node-gyp
```

Clone this repository, `cd` into it, and run `npm install`.

In order to get Electron to come up, zmq has to be built with Electron headers. zmq also needs to use `nan` 1.8.4. This gets included in npm-shrinkwrap.json. After doing an `npm install`, you'll have to `cd` into `./node_modules/zmq` and run:

```
node-gyp rebuild --target=0.25.2 --arch=x64 --dist-url=https://atom.io/download/atom-shell
```

After that you're all set to hack on Electron Jupyter mashups.

Run it with `electron . {path to kernel-###.json}
