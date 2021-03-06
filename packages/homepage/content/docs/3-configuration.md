---
title: Configuration
authors: ['CompuIves']
description:
  You can configure sandboxes and templates with configuration files.
---

## Configuration Files

There are some advanced use cases where you might need more control over a sandbox or template. That's why we support configuration files. Every template on CodeSandbox has a list of configuration files it supports. You can see the supported files under Configuration Files from the left-hand activity bar in the editor.

![Configurations File UI](./images/configuration.png)

## Configuration UI

Some configuration files can be configured using a UI. This UI will generate a
configuration file based on its state.

![Configurations File UI](./images/ui-configuration.png)

## Sandbox Configuration

A sandbox can be configured too, you can do this with `sandbox.config.json`. We
support these options:

| Option                   | Description                                                                                         | Possible Values                                                                                                    | Default Value                                      |
| ------------------------ | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------- |
| `infiniteLoopProtection` | Whether we should throw an error if we detect an infinite loop                                      | `true`/`false`                                                                                                     | `true`                                             |
| `hardReloadOnChange`     | Whether we should refresh the sandbox page on every change, good for sandboxes with global state.   | `true`/`false`                                                                                                     | `false`                                            |
| `template`               | Which sandbox template to use                                                                       | [see here](https://github.com/codesandbox-app/codesandbox-importers/blob/master/packages/types/index.d.ts#L24-L39) | smart detection, w/ fallback to `create-react-app` |
| `container`              | The container object contains the configurable port option, for example: `container: { port: 3212}` |
| `port`                   | The main port which the browser window listens to                                                   | 1024 - 65535                                                                                                       | First opened port inside the container.            |
