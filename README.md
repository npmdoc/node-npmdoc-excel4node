# api documentation for  [excel4node (v1.2.1)](https://github.com/natergj/excel4node#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-excel4node.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-excel4node) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-excel4node.svg)](https://travis-ci.org/npmdoc/node-npmdoc-excel4node)
#### Library to create Formatted Excel Files.

[![NPM](https://nodei.co/npm/excel4node.png?downloads=true)](https://www.npmjs.com/package/excel4node)

[![apidoc](https://npmdoc.github.io/node-npmdoc-excel4node/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-excel4node_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-excel4node/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-excel4node/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-excel4node/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nater",
        "email": "nater@seas.harvard.edu"
    },
    "bugs": {
        "url": "https://github.com/natergj/excel4node/labels/bug"
    },
    "dependencies": {
        "babel-register": "^6.9.0",
        "colors": "^1.1.2",
        "image-size": "0.5.0",
        "jszip": "^3.0.0",
        "lodash": "4.13.1",
        "mime": "^1.3.4",
        "sloth-logger": "^1.0.3",
        "xmlbuilder": "8.2.2"
    },
    "description": "Library to create Formatted Excel Files.",
    "devDependencies": {
        "babel-cli": "^6.10.1",
        "babel-polyfill": "^6.9.1",
        "babel-preset-es2015": "^6.9.0",
        "babel-preset-es2015-node4": "^2.1.0",
        "jsdoc-babel": "^0.2.1",
        "source-map-support": "^0.4.1",
        "tape": "^4.6.0",
        "tape-promise": "^1.1.0",
        "xmldom": "^0.1.22",
        "xpath.js": "^1.0.6"
    },
    "directories": {},
    "dist": {
        "shasum": "94ee13a004e9af2191d2cf0fae76d3dbf5ff3e5e",
        "tarball": "https://registry.npmjs.org/excel4node/-/excel4node-1.2.1.tgz"
    },
    "engines": {
        "node": ">4.0.0"
    },
    "gitHead": "03e65713f036a6e47775f2e56a9bf99219a7e27a",
    "homepage": "https://github.com/natergj/excel4node#readme",
    "keywords": [
        "excel",
        "spreadsheet",
        "xlsx",
        "formatted",
        "styled",
        "report",
        "workbook",
        "ooxml"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "http://opensource.org/licenses/mit-license.php"
        }
    ],
    "main": "./distribution/index.js",
    "maintainers": [
        {
            "name": "amekkawi",
            "email": "npm@andremekkawi.com"
        },
        {
            "name": "natergj",
            "email": "nater@iamnater.com"
        }
    ],
    "name": "excel4node",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/natergj/excel4node.git"
    },
    "scripts": {
        "build": "./node_modules/babel-cli/bin/babel.js source --presets babel-preset-es2015 -s --out-dir distribution",
        "document": "jsdoc ./source -r -d docs",
        "prepublish": "npm run build; npm run test",
        "test": "NODE_ENV=test ./node_modules/tape/bin/tape -r babel-register ./tests/*.test.js",
        "watch": "./node_modules/babel-cli/bin/babel.js source -w --presets babel-preset-es2015 -s --out-dir distribution"
    },
    "version": "1.2.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module excel4node](#apidoc.module.excel4node)
1.  [function <span class="apidocSignatureSpan">excel4node.</span>Workbook (opts)](#apidoc.element.excel4node.Workbook)
1.  [function <span class="apidocSignatureSpan">excel4node.</span>getExcelAlpha (colNum)](#apidoc.element.excel4node.getExcelAlpha)
1.  [function <span class="apidocSignatureSpan">excel4node.</span>getExcelCellRef (rowNum, colNum)](#apidoc.element.excel4node.getExcelCellRef)
1.  [function <span class="apidocSignatureSpan">excel4node.</span>getExcelRowCol (str)](#apidoc.element.excel4node.getExcelRowCol)
1.  [function <span class="apidocSignatureSpan">excel4node.</span>getExcelTS (date)](#apidoc.element.excel4node.getExcelTS)
1.  object <span class="apidocSignatureSpan">excel4node.</span>BorderStyle
1.  object <span class="apidocSignatureSpan">excel4node.</span>HorizontalAlignment
1.  object <span class="apidocSignatureSpan">excel4node.</span>Orientation
1.  object <span class="apidocSignatureSpan">excel4node.</span>PageOrder
1.  object <span class="apidocSignatureSpan">excel4node.</span>Pane
1.  object <span class="apidocSignatureSpan">excel4node.</span>PaneState
1.  object <span class="apidocSignatureSpan">excel4node.</span>PaperSize
1.  object <span class="apidocSignatureSpan">excel4node.</span>PatternType
1.  object <span class="apidocSignatureSpan">excel4node.</span>PositiveUniversalMeasure
1.  object <span class="apidocSignatureSpan">excel4node.</span>PresetColorVal
1.  object <span class="apidocSignatureSpan">excel4node.</span>PrintError
1.  object <span class="apidocSignatureSpan">excel4node.</span>VerticalAlignment



# <a name="apidoc.module.excel4node"></a>[module excel4node](#apidoc.module.excel4node)

#### <a name="apidoc.element.excel4node.Workbook"></a>[function <span class="apidocSignatureSpan">excel4node.</span>Workbook (opts)](#apidoc.element.excel4node.Workbook)
- description and source-code
```javascript
function Workbook(opts) {
    _classCallCheck(this, Workbook);

    opts = opts ? opts : {};

    this.logger = new SlothLogger.Logger({
        logLevel: Number.isNaN(parseInt(opts.logLevel)) ? 0 : parseInt(opts.logLevel)
    });

    this.opts = _.merge({}, workbookDefaultOpts, opts);

    this.sheets = [];
    this.sharedStrings = [];
    this.styles = [];
    this.stylesLookup = {};
    this.dxfCollection = new DXFCollection(this);
    this.mediaCollection = new MediaCollection();
    this.definedNameCollection = new DefinedNameCollection();
    this.styleData = {
        'numFmts': [],
        'fonts': [],
        'fills': [new Fill({ type: 'pattern', patternType: 'none' }), new Fill({ type: 'pattern', patternType: 'gray125' })],
        'borders': [new Border()],
        'cellXfs': [{
            'borderId': null,
            'fillId': null,
            'fontId': 0,
            'numFmtId': null
        }]
    };

    // Lookups for style components to quickly find existing entries
    // - Lookup keys are stringified JSON of a style's toObject result
    // - Lookup values are the indexes for the actual entry in the styleData arrays
    this.styleDataLookup = {
        'fonts': {},
        'fills': this.styleData.fills.reduce(function (ret, fill, index) {
            ret[JSON.stringify(fill.toObject())] = index;
            return ret;
        }, {}),
        'borders': this.styleData.borders.reduce(function (ret, border, index) {
            ret[JSON.stringify(border.toObject())] = index;
            return ret;
        }, {})
    };

    // Set Default Font and Style
    this.createStyle({ font: this.opts.defaultFont });
}
```
- example usage
```shell
...

### Basic Usage
'''javascript
// Require library
var xl = require('excel4node');

// Create a new instance of a Workbook class
var wb = new xl.Workbook();

// Add Worksheets to the workbook
var ws = wb.addWorksheet('Sheet 1');
var ws2 = wb.addWorksheet('Sheet 2');

// Create a reusable style
var style = wb.createStyle({
...
```

#### <a name="apidoc.element.excel4node.getExcelAlpha"></a>[function <span class="apidocSignatureSpan">excel4node.</span>getExcelAlpha (colNum)](#apidoc.element.excel4node.getExcelAlpha)
- description and source-code
```javascript
function getExcelAlpha(colNum) {
    var remaining = colNum;
    var aCharCode = 65;
    var columnName = '';
    while (remaining > 0) {
        var mod = (remaining - 1) % 26;
        columnName = String.fromCharCode(aCharCode + mod) + columnName;
        remaining = (remaining - 1 - mod) / 26;
    }
    return columnName;
}
```
- example usage
```shell
...
Accepts cell reference (i.e. 'A1') and returns object with corresponding row and column

'''javascript
xl.getExcelRowCol('B5');
// returns { row: 5, col: 2}
'''

xl.getExcelAlpha(column)
Accepts column as integer and returns corresponding column reference as alpha

'''javascript
xl.getExcelAlpha(10);
// returns 'J'
'''
...
```

#### <a name="apidoc.element.excel4node.getExcelCellRef"></a>[function <span class="apidocSignatureSpan">excel4node.</span>getExcelCellRef (rowNum, colNum)](#apidoc.element.excel4node.getExcelCellRef)
- description and source-code
```javascript
function getExcelCellRef(rowNum, colNum) {
    var remaining = colNum;
    var aCharCode = 65;
    var columnName = '';
    while (remaining > 0) {
        var mod = (remaining - 1) % 26;
        columnName = String.fromCharCode(aCharCode + mod) + columnName;
        remaining = (remaining - 1 - mod) / 26;
    }
    return columnName + rowNum;
}
```
- example usage
```shell
...
Accepts column as integer and returns corresponding column reference as alpha

'''javascript
xl.getExcelAlpha(10);
// returns 'J'
'''

xl.getExcelCellRef(row, column)
Accepts row and column as integers and returns Excel cell reference

'''javascript
xl.getExcelCellRef(5, 3);
// returns 'C5'
'''
...
```

#### <a name="apidoc.element.excel4node.getExcelRowCol"></a>[function <span class="apidocSignatureSpan">excel4node.</span>getExcelRowCol (str)](#apidoc.element.excel4node.getExcelRowCol)
- description and source-code
```javascript
function getExcelRowCol(str) {
    var numeric = str.split(/\D/).filter(function (el) {
        return el !== '';
    })[0];
    var alpha = str.split(/\d/).filter(function (el) {
        return el !== '';
    })[0];
    var row = parseInt(numeric, 10);
    var col = alpha.toUpperCase().split('').reduce(function (a, b, index, arr) {
        return a + (b.charCodeAt(0) - 64) * Math.pow(26, arr.length - index - 1);
    }, 0);
    return { row: row, col: col };
}
```
- example usage
```shell
...
ws.cell(3,1).bool(true).style(style).style({font: {size: 14}});

wb.write('Excel.xlsx');
'''
## excelnode
excel4node comes with some generic functions and types

xl.getExcelRowCol(cellRef)
Accepts cell reference (i.e. 'A1') and returns object with corresponding row and column

'''javascript
xl.getExcelRowCol('B5');
// returns { row: 5, col: 2}
'''
...
```

#### <a name="apidoc.element.excel4node.getExcelTS"></a>[function <span class="apidocSignatureSpan">excel4node.</span>getExcelTS (date)](#apidoc.element.excel4node.getExcelTS)
- description and source-code
```javascript
function getExcelTS(date) {

    var thisDt = new Date(date);
    thisDt.setDate(thisDt.getDate() + 1);
    // Take timezone into account when calculating date
    thisDt.setMinutes(thisDt.getMinutes() - thisDt.getTimezoneOffset());

    var epoch = new Date(1899, 11, 31);
    // Take timezone into account when calculating epoch
    epoch.setMinutes(epoch.getMinutes() - epoch.getTimezoneOffset());

    // Get milliseconds between date sent to function and epoch
    var diff2 = thisDt.getTime() - epoch.getTime();

    var ts = diff2 / (1000 * 60 * 60 * 24);
    return ts;
}
```
- example usage
```shell
...
Accepts row and column as integers and returns Excel cell reference

'''javascript
xl.getExcelCellRef(5, 3);
// returns 'C5'
'''

xl.getExcelTS(date)
Accepts Date object and returns an Excel timestamp

'''javascript
var newDate = new Date('2015-01-01T00:00:00.0000Z');
xl.getExcelTS(newDate);
// Returns 42004.791666666664
'''
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
