# recaptcha-test-keys

The ReCaptcha widget keys for testing and development environments, but as a
Node.js module with a name.

[Provided by Google in the reCAPTCHA documentation.][ref]

## Installation

```
npm install --save recaptcha-test-keys
```

## Usage

```js
const testKeys = require('recaptcha-test-keys')

grecaptcha.render('recaptcha-element', {
  sitekey: process.env.NODE_ENV === 'development'
    ? testKeys.sitekey
    : yourActualSiteKey()
})

// or
import { sitekey, secret } from 'recaptcha-test-keys'

// etc
```

## API

### `testKeys.sitekey`

Site key: 6LeIxAcTAAAAAJcZVRqyHh71UMIEGNQ_MXjiZKhI

### `testKeys.secret`

Secret key: 6LeIxAcTAAAAAGG-vFI1TnRWxMZNFuojJ4WifJWe

## License

[Unlicense](./LICENSE)

[ref]: https://developers.google.com/recaptcha/docs/faq#id-like-to-run-automated-tests-with-recaptcha-v2-what-should-i-do
