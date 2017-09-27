# eztz
Easy Tezos key generator and utility tool - It's eztz! Live demo: http://173.254.236.122/keygen.html

#### *** Disclaimer - all keys generated should be treated as live. Please use the tool offline, and endavour to keep any input/output data secure and private ***

### Installation
In browser, just include eztz.js and you're good to go.

### Building
Rebuild bundle using the following code (requires browserify):
##### browserify main.js -o eztz.js

### Usage
Include the eztz.js file and run the eztz_ready function as per below:
```html
<script src="./eztz.js"></script>
<script>
    /* eztz is now ready to use */
    eztz_ready(function(eztz){
        var m = eztz.generateMnemonic();
        var keys = eztz.generateKeys(m, 'test');
        console.log(keys);
    });
</script>
```
### Available Functions

#### eztz.generateMnemonic()
Returns a mnemonic to be used for the key generator (string)

#### eztz.generateKeys(mnemonic, passphrase)
Returns an object with generated keys and associated data, as per below:
```javascript
{
    mnemonic : mnemonic, // The mneomic used
    passphrase : passphrase, // The passphrase used
    sk : sk, // The secret/private key hash (sk - starts with edsk)
    pk : pk, // The public key hash (pk - starts with edpk)
    pkh : pkh, // The public key hash (pkh or id - starts with tz1)
}
```
### Future Development
We will be working on this library on a regular basis, with hopes of adding more functiliaty (message signing/verification etc).

### Support Us
Please consider donating to help us develop this, and other Tezos related tools: Bitcoin: 1KSiyfgs5XwTZjaLpmCTHxonsyXMx383P1

### Credits
Coming soon - used a lot of existing libraries

### License
MIT
