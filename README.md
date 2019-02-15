# rpgcoinjs-message

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

## Examples

``` javascript
var rpgcoin = require('rpgcoinjs-lib') // v1.x.x
var rpgcoinMessage = require('rpgcoinjs-message')
```

> sign(message, privateKey, compressed[, network.messagePrefix])

Sign a Rpgcoin message
``` javascript
var keyPair = rpgcoin.ECPair.fromWIF('5KYZdUEo39z3FPrtuX2QbbwGnNP5zTd7yyr2SC1j299sBCnWjss')
var privateKey = keyPair.privateKey
var message = 'This is an example of a signed message.'

var signature = rpgcoinMessage.sign(message, privateKey, keyPair.compressed)
console.log(signature.toString('base64'))
```

> verify(message, address, signature[, network.messagePrefix])

Verify a Rpgcoin message
``` javascript
var address = '1HZwkjkeaoZfTSaJxDw6aKkxp45agDiEzN'

console.log(rpgcoinMessage.verify(message, address, signature))
// => true
```

## LICENSE [MIT](LICENSE)
