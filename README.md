# is-zip-file
Checks if the file path is zip file. It does not read the complete file nor it depends upon file extension

### Installation

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install is-zip-file --save
```

### Usage

```javascript
var ZIP_FILE = require('is-zip-file');

// If a valid zip file is provided and exists at path specified
ZIP_FILE.isZip('temp.zip', function(err, is) {
    if(err) {
        console.log('Error while checking if file is zip : ' + err);
    } else {
        console.log('Given file is zip : ' + is);
    }
});
//=> Given file is zip : true

// If a valid zip file is provided and exists at path specified
ZIP_FILE.isZipSync('temp.zip')
//=> true


```

### Clone the repo

```bash
$ git clone https://github.com/luthraG/is-zip-file.git
```

### API

#### isZip(path, cb)

This is asynchronous API for checking if file is zip. This API takes two parameters:
1. File path which needs to be checked and 
2. callback, which is invoked when it checks the file to be zip or not or in case of errors

It throws
1. TypeError if path is not provided or if provided but not of type String or if callback is not provided or if provided but not of type Function
2. FileNotExists error which specified file does not exists.

Callback has two parameters:
1. First parameter is error which is null in case of success
2. Second parameter is boolean value which indicates if file is zip or not


**Example**

```javascript
var ZIP_FILE = require('is-zip-file');

// If a valid zip file is provided and exists at path specified
ZIP_FILE.isZip('temp.zip', function(err, is) {
    if(err) {
        console.log('Error while checking if file is zip : ' + err);
    } else {
        console.log('Given file is zip : ' + is);
    }
});
//=> Given file is zip : true


```

#### isZipSync(path)

This is synchronous API for checking if file is zip. This API takes one parameter:
1. File path which needs to be checked

It throws
1. TypeError if path is not provided or if provided but not of type String
2. FileNotExists error which specified file does not exists.

It returns
Boolean indicating if file at specified path is zip or not


**Example**

```javascript
var ZIP_FILE = require('is-zip-file');

// If a valid zip file is provided and exists at path specified
ZIP_FILE.isZipSync('temp.zip')
//=> true

```

### Related projects

You might also be interested in these projects:

* [is-pdf-file](https://www.npmjs.com/package/is-pdf-file): Checks if the file path is PDF file. It does not read the complete file nor it depends upon file extension. | [homepage](https://github.com/luthraG/is-pdf-file.git)
* [is-psd-file](https://www.npmjs.com/package/is-psd-file): Checks if the file path is PSD file. It does not read the complete file nor it depends upon file extension. | [homepage](https://github.com/luthraG/is-psd-file.git)

### Author

**Gaurav Luthra**

* [github/luthraG](https://github.com/luthraG)

## License

MIT © [Gaurav Luthra](luthra.zenith@gmail.com)


