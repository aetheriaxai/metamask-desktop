# MetaMask Desktop App
### Prerequisites

- Install [Node.js](https://nodejs.org) version 16
    - If you are using [nvm](https://github.com/creationix/nvm#installation) (recommended) running `nvm use` will automatically choose the right node version for you.
- Install [Yarn](https://yarnpkg.com/en/docs/install)

### Building locally

- Install dependencies: `yarn setup` (not the usual install command)
- Copy the `.metamaskrc.dist` file to `.metamaskrc`
    - Replace the `INFURA_PROJECT_ID` value with your own personal [Infura Project ID](https://infura.io/docs).
    - Optionally, replace the `PASSWORD` value with your development wallet password to avoid entering it each time you open the app.
- Build the extension with desktop support using `yarn build:desktop:extension`.
- Build the desktop app using `yarn build:desktop`.
    - Run `yarn start:desktop` to run dev mode.


### Building locally with MV3 enabled

- Install dependencies: `yarn setup` (not the usual install command)
- Copy the `.metamaskrc.dist` file to `.metamaskrc`
    - `ENABLE_MV3=true` is automatically set at build step.
- Build the extension with desktop support using `yarn build:desktop:extension:mv3`.
- Build the desktop app using `yarn build:desktop:mv3`.
    - Run `yarn start:desktop` to run the desktop app.


### Running Unit Tests and Linting

Run unit tests and the linter with `yarn test`. To run just unit tests, run `yarn test:unit`.

You can run the linter by itself with `yarn lint`, and you can automatically fix some lint problems with `yarn lint:fix`. You can also run these two commands just on your local changes to save time with `yarn lint:changed` and `yarn lint:changed:fix` respectively.


### Environment Variables

#### Development

| Name | Description |
| ---  | --- |
| SKIP_OTP_PAIRING_FLOW | Whether set to `1` skips the OTP pairing flow. |