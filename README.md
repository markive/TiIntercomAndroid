# Intercom android module for Intercom Android SDK version 1.1.11

Integrate Intercom.io with Appcelerator.  iOS module available here https://github.com/markive/TiIntercom . Tested with 5.1.1GA SDK

Example
```
var TiIntercom = require('intercom');
TiIntercom.initialize(<API KEY>,<APP ID>);
TiIntercom.startSession("jerodfritz@gmail.com");
```

/lib/intercom.js
```
var TiIntercom = require('ti.intercom.android');

exports.initialize = function(key, id){
  TiIntercom.initialize({
      api_key : key,
      app_id : id,
  });
}

exports.startSession = function(email) {
  TiIntercom.reset();
  TiIntercom.registerUserWithEmail(email);
};

exports.endSession = function() {
  TiIntercom.reset();
};

exports.openIntercom = function() {
  TiIntercom.presentConversationList();
};
```

Author
========

Jerod
(jerodfritz@gmail.com)


## License

    The MIT License (MIT) Copyright © 2015

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.
