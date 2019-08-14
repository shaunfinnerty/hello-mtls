# Hello mTLS

This repository contains documentation on how to configure a broad array of technologies to perform mutual TLS. It is part of the Hello mTLS project, designed to raise developer awareness about public key infrastructure as a potential solution to common security problems.

If you notice any outdated, missing, or errant docs, pull requests are strongly encouraged!

## Contributing

Documentation for each technology lives in its corresponding directory in the [docs/](docs/) folder.

To get rolling on local development, clone this repository and start the local dev server:

```
$ yarn install
$ yarn start
```

You will be able to preview all changes at http://localhost:3000.


### Adding new technologies

If you are adding a new technology, your best bet is to refer to existing configurations in this repository, but here is a high-level breakdown of each directory's contents.

#### config.yaml

This file configures basic information like the technology name and external links to documentation.

#### logo.png

This is a 256 x 256px transparent PNG of the technology's logo. If missing, a standard placeholder will be used.

#### Documentation templates

Three optional markdown files provide prose describing how to configure the technology for three different scenarios:

1. Server TLS authentication (`server_auth.md`)
2. Client TLS authentication (`client_auth.md`)
3. Client requests using TLS (`client.md`)

If your documentation makes use of the name of a certificate's identity, its certificate filename, its private key filename, or the root certificate filename, please use these template tokens. They will be interpolated with the appropriate values at build time in different contexts:

1. `${identity_name}` - Name of the identity like `example.internal.net`
2. `${identity_cert}` - Filename of the identity's certificate like `example.crt`
3. `${identity_key}` - Filename of the identity's private key like `example.key`
3. `${ca_cert}` - Filename of the root CA certificate `ca.crt`

## Thanks!

Please don't hesitate to reach out on [our Gitter](https://gitter.im/smallstep/community) with any questions.