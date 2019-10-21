# Represent Sketch Plugin

Present your UX/UI Designs lightning fast on client's devices without leaving Sketch. 📲
Exports the selected artboard and makes it available on your client's mobile phone.

_It was created using `skpm`. For a detailed explanation on how things work, checkout the [skpm Readme](https://github.com/skpm/skpm/blob/master/README.md)._

## Usage

Download the "Hello World" example or [clone the repo](https://github.com/BohemianCoding/SketchAPI):

```bash
curl https://codeload.github.com/BohemianCoding/SketchAPI/tar.gz/develop | tar -xz --strip=2 SketchAPI-develop/examples/hello-world
cd hello-world
```

Install the dependencies

```bash
npm install
```

Once the installation is done, you can run some commands inside the project folder:

```bash
npm run build
```

To watch for changes:

```bash
npm run watch
```

Additionally, if you wish to run the plugin every time it is built:

```bash
npm run start
```

## Debugging

To view the output of your `console.log`, you have a few different options:

* Use the [`sketch-dev-tools`](https://github.com/skpm/sketch-dev-tools)
* Open `Console.app` and look for the sketch logs
* Look at the `~/Library/Logs/com.bohemiancoding.sketch3/Plugin Output.log` file

Skpm provides a convenient way to do the latter:

```bash
skpm log
```

The `-f` option causes `skpm log` to not stop when the end of logs is reached, but rather to wait for additional data to be appended to the input


## Defining The Action Handler

In the manifest, we told Sketch that every time the `SelectionChanged` action finishes, we want it
to run the onSelectionChanged handler in our `represent.js` script file.

So now we need to put some code into the `represent.js` file to define that handler and make it do something useful.
@example Selection Changed available at [GitHub](https://github.com/BohemianCoding/SketchAPI/tree/develop/examples/selection-changed)
