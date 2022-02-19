
# What is this?
A handful of scripts to create TLA+ modules and help run things in a shell

# Installation
First of all, go grab the TLA+ Toolbox and install it. You can find it [here](https://github.com/tlaplus/tlaplus/releases). You'll only need the jar, so feel free to only download that.

Grab the content of `aliases`, adjust the jar path env var and slap it in your shell of choice.

While you're at it, shove ztla in your path somewhere.

# Usage
`ztla <module-name>` will create a folder for your module, along with a model config and a model.

We're assuming that we'll use PlusCal in most places, so the expected flow is:

* Mess with your module's code in `<module-name>.tla`
* Run `pcal <module-name.tla>`, which will expand the PlusCal to TLA
* Run `tlc <model>.tla`, which should actually run the model and verification

You can configure the specifics of what each model should check in `<model>.cfg`.
