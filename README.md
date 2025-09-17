# `Turborepo` Vite starter + hot reload with docker compose

This is a community-maintained example. If you experience a problem, please submit a pull request with a fix. GitHub Issues will be closed.

## How to run

```
Added nginx-proxy service for domain routing
Added VIRTUAL_HOST and VIRTUAL_PORT environment variables
Created a new network for nginx-proxy
Connected the web service to both networks
```

Run the following command:

```sh
docker-compose up --build
```

```sh
sudo echo "127.0.0.1 my-domain.local" >> /etc/hosts
```

## What's inside?

This Turborepo includes the following packages and apps:

### Apps and Packages

- `web`: react [vite](https://vitejs.dev) ts app
- `@repo/ui`: a stub component library shared by `web` application
- `@repo/eslint-config`: shared `eslint` configurations
- `@repo/typescript-config`: `tsconfig.json`s used throughout the monorepo

Each package and app is 100% [TypeScript](https://www.typescriptlang.org/).

### Utilities

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting
