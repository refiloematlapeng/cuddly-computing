

## Quick Start

```bash
git clone git@github.com:refiloematlapeng/cuddly-c.git
cd admin-vimo
npm install
npm start
```

`npm start` should open a browser window to <http://localhost:4200>

By default angular runs on port 4200. To change this port you can run:

```bash
# This starts the development server on port 4205,
# but you can use any port you'd like
export PORT=4205 && npm start
```

## Tests

### Unit Tests

```bash
npm run test
```

### e2e

```bash
npm run e2e
```

## Production

You can get Docker [here](https://www.docker.com/get-started)

```bash
npm run docker:build
npm run docker:run
```

## Generate Code

```bash
npm run generate:module -- --path src/modules --name Test
npm run generate:component -- --path src/modules/test/containers --name Test
npm run generate:component -- --path src/modules/test/components --name Test
npm run generate:directive -- --path src/modules/test/directives --name Test
npm run generate:service -- --path src/modules/test/services --name Test

### npm start

If you receive memory issues (most likely on Linux, but could technically happen on any system) adjust
`max_old_space_size` in the `ng` command of the `package.json`:

```json
"ng": "node --max_old_space_size=2048 ./node_modules/.bin/ng",
```

