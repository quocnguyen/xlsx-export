xlsx-export
===========

very basic node js streaming json -> xlsx converter

Based on **functionscope** https://www.npmjs.org/package/excel-export


**test**

```
npm test
```

**Usage**

Exports a xlsx on the fly

```
const http = require('http')
var XlsxExport = require('xlsx-export');
var readStream = mongo.collection('someCollection');

const server = http.createServer(function (req, res) {
  res.setHeader('Content-Type', 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet')
  XlsxExport(readStream).pipe(res)
})
//todo: enjoy!

```
