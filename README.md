<!-- Gatsby OSS team is on holiday, expect a delayed response -->

<!--
  Please fill out each section below, otherwise, your issue will be closed. This info allows Gatsby maintainers to diagnose (and fix!) your issue as quickly as possible.

  Useful Links:
  - Documentation: https://www.gatsbyjs.org/docs/
  - How to File an Issue: https://www.gatsbyjs.org/contributing/how-to-file-an-issue/

  Before opening a new issue, please search existing issues: https://github.com/gatsbyjs/gatsby/issues
-->

## Description

(for gatsbyjs/gatsby#19863)

Failed extract queries from components when run VSCode build task, but succeed on the command line.


### Visual Studio Code task

```bat:vscode task
> Executing task: npm run develop <


> gatsby-starter-hello-world@0.1.0 develop C:\path\to\gatsby-bug-repo
> gatsby develop

success open and validate gatsby-configs - 0.066s
success load plugins - 1.254s
success onPreInit - 0.008s
success initialize cache - 0.021s
success copy gatsby files - 0.307s
success onPreBootstrap - 0.029s
success createSchemaCustomization - 0.014s
success source and transform nodes - 0.595s
success building schema - 0.828s
success createPages - 0.056s
success createPagesStatefully - 0.117s
success onPreExtractQueries - 0.005s
success update schema - 0.077s

 ERROR #85910  GRAPHQL

Multiple "root" queries found in file: "MarkdownPagesTemplateQuery" and "MarkdownPagesTemplateQuery".
Only the first ("MarkdownPagesTemplateQuery") will be registered.

Instead of:
1 | query MarkdownPagesTemplateQuery {
2 |   bar {
3 |     #...
4 |   }
5 | }
6 |
7 | query MarkdownPagesTemplateQuery {
8 |   foo {
9 |     #...
10 |   }
11 | }

Do:
1 | query markdownPagesTemplateQueryAndMarkdownPagesTemplateQuery {
2 |   bar {
3 |     #...
4 |   }
5 |   foo {
6 |     #...
7 |   }
8 | }

File: src\templates\markdown-pages-template.js

failed extract queries from components - 0.513s
success write out requires - 0.080s
success write out redirect data - 0.008s
success onPostBootstrap - 0.004s
⠀
info bootstrap finished - 15.399 s
⠀
success run queries - 0.161s - 3/3 18.58/s
⠀
You can now view gatsby-starter-hello-world in the browser.
⠀
  http://localhost:8000/
⠀
View GraphiQL, an in-browser IDE, to explore your site's data and schema
⠀
  http://localhost:8000/___graphql
⠀
Note that the development build is not optimized.
To create a production build, use gatsby build
⠀
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\object-assign\index.js
    Used by 2 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react\cjs\react.development.js
* C:\path\to\gatsby-bug-repo\node_modules\object-assign\index.js
    Used by 3 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react\cjs\react.development.js
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\checkPropTypes.js
    Used by 2 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react\cjs\react.development.js
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\checkPropTypes.js
    Used by 3 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react\cjs\react.development.js
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\factoryWithTypeCheckers.js
    Used by 1 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\prop-types\index.js
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\factoryWithTypeCheckers.js
    Used by 1 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\prop-types\index.js
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\index.js
    Used by 4 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\gatsby\dist\utils\babel-loader.js??ref--4-0!C:\path\to\gatsby-bug-repo\node_modules\eslint-loader\index.js??ref--11-0!C:\path\to\gatsby-bug-repo\.cache\dev-404-page.js
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\index.js
    Used by 23 module(s), i. e.
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\lib\ReactPropTypesSecret.js
    Used by 2 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\prop-types\factoryWithTypeCheckers.js
* C:\path\to\gatsby-bug-repo\node_modules\prop-types\lib\ReactPropTypesSecret.js
    Used by 2 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\prop-types\checkPropTypes.js
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\react-is\cjs\react-is.development.js
    Used by 1 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react-is\index.js
* C:\path\to\gatsby-bug-repo\node_modules\react-is\cjs\react-is.development.js
    Used by 1 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react-is\index.js
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\react-is\index.js
    Used by 2 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\prop-types\index.js
* C:\path\to\gatsby-bug-repo\node_modules\react-is\index.js
    Used by 3 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\prop-types\index.js
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\react\cjs\react.development.js
    Used by 1 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react\index.js
* C:\path\to\gatsby-bug-repo\node_modules\react\cjs\react.development.js
    Used by 1 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\react\index.js
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\react\index.js
    Used by 29 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\gatsby\dist\utils\babel-loader.js??ref--4-0!C:\path\to\gatsby-bug-repo\node_modules\eslint-loader\index.js??ref--11-0!C:\path\to\gatsby-bug-repo\src\templates\markdown-pages-template.js
* C:\path\to\gatsby-bug-repo\node_modules\react\index.js
    Used by 79 module(s), i. e.
warn There are multiple modules with names that only differ in casing.
This can lead to unexpected behavior when compiling on a filesystem with other case-semantic.
Use equal casing. Compare these module identifiers:
* C:\path\to\gatsby-bug-repo\node_modules\webpack\buildin\harmony-module.js
    Used by 3 module(s), i. e.
    C:\path\to\gatsby-bug-repo\node_modules\gatsby\dist\utils\babel-loader.js??ref--4-0!C:\path\to\gatsby-bug-repo\node_modules\eslint-loader\index.js??ref--11-0!C:\path\to\gatsby-bug-repo\src\templates\markdown-pages-template.js
* C:\path\to\gatsby-bug-repo\node_modules\webpack\buildin\harmony-module.js
    Used by 18 module(s), i. e.
success Building development bundle - 8.503s
```

### run in cmd.exe

```bat: cmd.exe
C:\path\to\gatsby-bug-repo>npm run develop

> gatsby-starter-hello-world@0.1.0 develop C:\path\to\gatsby-bug-repo
> gatsby develop

success open and validate gatsby-configs - 0.067s
success load plugins - 1.259s
success onPreInit - 0.011s
success initialize cache - 0.024s
success copy gatsby files - 0.348s
success onPreBootstrap - 0.030s
success createSchemaCustomization - 0.017s
success source and transform nodes - 0.564s
success building schema - 0.905s
success createPages - 0.064s
success createPagesStatefully - 0.122s
success onPreExtractQueries - 0.007s
success update schema - 0.080s
success extract queries from components - 0.392s
success write out requires - 0.076s
success write out redirect data - 0.008s
success onPostBootstrap - 0.005s
⠀
info bootstrap finished - 15.590 s
⠀
success run queries - 0.195s - 3/3 15.37/s
⠀
You can now view gatsby-starter-hello-world in the browser.
⠀
  http://localhost:8000/
⠀
View GraphiQL, an in-browser IDE, to explore your site's data and schema
⠀
  http://localhost:8000/___graphql
⠀
Note that the development build is not optimized.
To create a production build, use gatsby build
⠀
success Building development bundle - 7.637s
```

### Steps to reproduce

1. Create a new Gatsby site from `https://github.com/gatsbyjs/gatsby-starter-hello-world`
2. install `gatsby-source-filesystem` and `gatsby-transformer-remark` 
3. setup markdown build (`gatsby-node.js` and `gatsby-config.js`)
4. setup createNodeField
5. build develop from VSCode task.

### Expected result

`success extract queries from components`

### Actual result

`failed extract queries from components`

### Environment
****
```
  System:
    OS: Windows 10 10.0.17763
    CPU: (4) x64 Intel(R) Pentium(R) CPU 4415Y @ 1.60GHz
  Binaries:
    Node: 12.14.0 - C:\Program Files\nodejs\node.EXE
    npm: 6.13.4 - C:\Program Files\nodejs\npm.CMD
  Languages:
    Python: 2.7.17 - C:\Python27\python.EXE
  Browsers:
    Edge: 44.17763.831.0
  npmPackages:
    gatsby: ^2.18.12 => 2.18.12
    gatsby-source-filesystem: ^2.1.43 => 2.1.43
    gatsby-transformer-remark: ^2.6.45 => 2.6.45
```