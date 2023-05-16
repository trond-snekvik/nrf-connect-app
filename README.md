# nRF Connect SDK application template

Blank starting point for an nRF Connect SDK application.

## Get started

The repo contains a top level West manifest that will initialize an instance of the nRF Connect SDK around the application directory. Use the following commands to initialize your workspace:

```
west init -m https://github.com/trond-snekvik/nrf-connect-app my-project
cd my-project
west update -n -o=--depth=1
```

The west workspace with the nRF Connect SDK and Zephyr will be created in ./my-project, and this repo will be cloned under ./my-project/app.

## Alternative setup

If you don't want to set up a separate instance of the nRF Connect SDK for this application, there are other alternatives:

### Usage with Toolchain Manager

If you have an nRF Connect SDK instance installed by the nRF Connect for Desktop Toolchain Manager, you can clone the application somewhere else, and use the VS Code configuration to point to your SDK. The west.yml file in the app will be ignored, and you'll need to continue using the toolchain manager with this application.

### Add to existing nRF Connect SDK directory

If you already have an nRF Connect SDK, you can clone this repo next to ./nrf and ./zephyr in the top directory of the SDK. VS Code will automatically tie your application to this SDK instance.

The west.yml file in the app will be ignored, but you can reconfigure your west workspace to use the application's manifest later by calling:

```
west config manifest.path nrf-connect-app
west update
```
