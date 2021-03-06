mailgun-validate-email
=================

Super tiny wrapper of email validation API from [Mailgun](http://www.mailgun.com/), this can be most useful in form validation to avoid spam

### Disclaimer
This module uses a third party service from Mailgun to be able to verify the validy of the email, you can all the info in their [API docs](http://documentation.mailgun.com/api-email-validation.html)  
Emails are securely transmitted using Public Key Cryptography

# Badgers
[![NPM](https://nodei.co/npm/mailgun-validate-email.png?downloads=true&stars=true)](https://nodei.co/npm/mailgun-validate-email/)

[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/diasdavid/mailgun-validate-email?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge) 
[![Dependency Status](https://david-dm.org/diasdavid/mailgun-validate-email.svg)](https://david-dm.org/diasdavid/mailgun-validate-email)
[![Build Status](https://travis-ci.org/diasdavid/mailgun-validate-email.svg)](https://travis-ci.org/diasdavid/mailgun-validate-email)

### How to use

```javascript
var validator = require('mailgun-validate-email')
validator("banana@papaia.com", function (err, result){
  ...
})
```

Output will be something like

```javascript
{ 
  is_valid: true,
  parts: { 
    local_part: banana, 
    domain: papaia.com, 
    display_name: null 
  },
  address: 'banana@papaia.com',
  did_you_mean: null 
}
```




## License

(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
