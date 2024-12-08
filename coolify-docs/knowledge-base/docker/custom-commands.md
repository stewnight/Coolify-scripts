---
title: 'Custom Commands'
head:
  - tag: 'meta'
    attrs:
      property: 'og:title'
      content: 'How to use custom commands for your Docker deployments with Coolify.'
description: 'A guide on how to use custom commands for your Docker deployments with Coolify.'
---

import { Aside, Steps } from '@astrojs/starlight/components';

For deploying your resources, you can add custom options to the final docker command, which is used to run your container.

<Aside type="caution">
  Some of the docker native options are not supported, because it could break
  the Coolify's functionality. If you need any of the unsupported options,
  please [contact us](/docs/contact)**.**
</Aside>

## Supported Options

- `--ip`
- `--ip6`
- `--shm-size`
- `--cap-add`
- `--cap-drop`
- `--security-opt`
- `--sysctl`
- `--device`
- `--ulimit`
- `--init`
- `--ulimit`
- `--privileged`

## Usage

You can simply add the options to the `Custom Docker Options` field on the `General` tab of your resource.

Example: `--cap-add SYS_ADMIN --privileged`
