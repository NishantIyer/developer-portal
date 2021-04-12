---
id: use-cli
title: Command Line Interface
sidebar_label: Command Line Interface
description: Learn how to use CLI
image: ./img/og-developer-portal.png
---

This command line interface provides a collection of tools for key generation, transaction construction, certificate creation and other important tasks.

It is organized in a hierarchy of subcommands, and each level comes with its own built-in documentation of command syntax and options.

We can get the top level help by simply typing the command without arguments:

```
cardano-cli
```

We will be told that one available subcommand is `node`, and typing:

```
cardano-cli node
```

will display available sub-subcommands, one of which is `key-gen`. Typing:

```
cardano-cli node key-gen
```

will inform us about the parameters this command takes, so we can for example generate a key-pair of offline keys and a file for the issue counter by typing:

```
cardano-cli node key-gen \
--cold-verification-key-file cold.vkey \
--cold-signing-key-file cold.skey \
--operational-certificate-issue-counter-file cold.counter
```