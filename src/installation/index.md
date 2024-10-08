# Installation

## Prerequisites

You need at least `git`, `docker` and `docker compose` installed on your machine to run the whole stack.

Additionally, if you want to develop in one of the components, you will need to have installed:

    - JDK 17+
    - NodeJs 16.10+
    - Angular cli 13+

It has been tested on linux, mac and windows, although on windows you might have to adapt some of the scripts.

There are different ways of running the stack, either locally (for e.g testing, development), or for production. 

### Testing, frontend development

If you just want to contribute in one of the frontends, or simply testing it without having to compile the backends, follow these steps:

[Frontend development](./compiled.md)

### Full-stack development

If you'd like to contribute in both backend and frontend, follow these steps:

[Full-Stack Development](./monorepo.md)

### Production

Deployment to production is described here:

[Production](./production/index.md)
