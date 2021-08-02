# Workshop 17 - Setup

## 1 - Installation

Please make sure you have the following programs installed:

- [node (version 14 or higher)](https://github.com/nodejs/node): javascript interpreter
- [npm](https://www.npmjs.com/): node package manager

To install `node` and `npm`:
- under fedora: `sudo dnf install nodejs`.
- under ubuntu: `sudo apt install nodejs npm`.

You have to install yarn globally using the following command:
```shell
$ npm install --global yarn
```

## 2 - Project bootstrap

Download and extract the sources available [here](https://github.com/PoCInnovation/Workshops/tree/software-grpc/software/17.gRPC/sources.zip).

The extracted folder should look like this:
```shell
➜  sources ✗ tree -a
.
├── gen-proto.sh      # Protobuff generator script
├── jestconfig.json   # Test configuration
├── package.json      # Package manager
├── proto
│   └── pochat.proto  # Protobuf file
├── src
│   ├── client.ts     # Client
│   ├── index.ts
│   └── server.ts     # Server
├── tests
│   └── chat.test.ts  # Test file
├── tsconfig.json     # Typescript configuration
└── yarn.lock         # Dependencies lock files

```

## 3 - Validation

To ensure that everything was extracted correctly, run the following command:
```shell
yarn install
```
It should give the following result:
```shell
➜  sources ✗ yarn install
yarn install v1.22.10
[1/4] Resolving packages...
[2/4] Fetching packages...
info fsevents@2.3.2: The platform "linux" is incompatible with this module.
info "fsevents@2.3.2" is an optional dependency and failed compatibility check. Excluding it from installation.
[3/4] Linking dependencies...
warning "eslint-config-airbnb-typescript > eslint-config-airbnb@18.2.1" has unmet peer dependency "eslint-plugin-jsx-a11y@^6.4.1".
warning "eslint-config-airbnb-typescript > eslint-config-airbnb@18.2.1" has unmet peer dependency "eslint-plugin-react@^7.21.5".
warning "eslint-config-airbnb-typescript > eslint-config-airbnb@18.2.1" has unmet peer dependency "eslint-plugin-react-hooks@^4 || ^3 || ^2.3.0 || ^1.7.0".
[4/4] Building fresh packages...
Done in 1.66s.
```

[Go back to the exercise](./README.md)