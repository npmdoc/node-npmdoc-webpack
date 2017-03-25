# api documentation for  [webpack (v2.3.2)](https://github.com/webpack/webpack)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webpack.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webpack)
#### Packs CommonJs/AMD modules for the browser. Allows to split your codebase into multiple bundles, which can be loaded on demand. Support loaders to preprocess files, i.e. json, jsx, es7, css, less, ... and your custom stuff.

[![NPM](https://nodei.co/npm/webpack.png?downloads=true)](https://www.npmjs.com/package/webpack)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webpack/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-webpack_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webpack/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-webpack/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Tobias Koppers @sokra"
    },
    "bin": {
        "webpack": "./bin/webpack.js"
    },
    "bugs": {
        "url": "https://github.com/webpack/webpack/issues"
    },
    "dependencies": {
        "acorn": "^4.0.4",
        "acorn-dynamic-import": "^2.0.0",
        "ajv": "^4.7.0",
        "ajv-keywords": "^1.1.1",
        "async": "^2.1.2",
        "enhanced-resolve": "^3.0.0",
        "interpret": "^1.0.0",
        "json-loader": "^0.5.4",
        "loader-runner": "^2.3.0",
        "loader-utils": "^0.2.16",
        "memory-fs": "~0.4.1",
        "mkdirp": "~0.5.0",
        "node-libs-browser": "^2.0.0",
        "source-map": "^0.5.3",
        "supports-color": "^3.1.0",
        "tapable": "~0.2.5",
        "uglify-js": "^2.8.5",
        "watchpack": "^1.3.1",
        "webpack-sources": "^0.2.3",
        "yargs": "^6.0.0"
    },
    "description": "Packs CommonJs/AMD modules for the browser. Allows to split your codebase into multiple bundles, which can be loaded on demand. Support loaders to preprocess files, i.e. json, jsx, es7, css, less, ... and your custom stuff.",
    "devDependencies": {
        "beautify-lint": "^1.0.3",
        "benchmark": "^2.1.1",
        "bundle-loader": "~0.5.0",
        "codacy-coverage": "^2.0.1",
        "codecov.io": "^0.1.2",
        "coffee-loader": "~0.7.1",
        "coffee-script": "^1.10.0",
        "coveralls": "^2.11.2",
        "css-loader": "~0.25.0",
        "es6-promise-polyfill": "^1.1.1",
        "eslint": "3.12.2",
        "eslint-plugin-node": "^3.0.5",
        "express": "~4.13.1",
        "extract-text-webpack-plugin": "^2.0.0-beta",
        "file-loader": "~0.9.0",
        "i18n-webpack-plugin": "^0.3.0",
        "istanbul": "^0.4.5",
        "jade": "^1.11.0",
        "jade-loader": "~0.8.0",
        "js-beautify": "^1.5.10",
        "less": "^2.5.1",
        "less-loader": "^2.0.0",
        "lodash": "^4.17.4",
        "mocha": "^3.2.0",
        "mocha-lcov-reporter": "^1.0.0",
        "nsp": "^2.6.1",
        "raw-loader": "~0.5.0",
        "react": "^15.2.1",
        "react-dom": "^15.2.1",
        "script-loader": "~0.7.0",
        "should": "^11.1.1",
        "simple-git": "^1.65.0",
        "sinon": "^1.17.7",
        "style-loader": "~0.13.0",
        "url-loader": "~0.5.0",
        "val-loader": "~0.5.0",
        "vm-browserify": "~0.0.0",
        "webpack-dev-middleware": "^1.9.0",
        "worker-loader": "~0.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "7d521e6f0777a3a58985c69425263fdfe977b458",
        "tarball": "https://registry.npmjs.org/webpack/-/webpack-2.3.2.tgz"
    },
    "engines": {
        "node": ">=4.3.0 <5.0.0 || >=5.10"
    },
    "files": [
        "lib/",
        "bin/",
        "buildin/",
        "hot/",
        "web_modules/",
        "schemas/"
    ],
    "gitHead": "6b209b13d76ec43080d6afbad4bb4dd6931e4638",
    "homepage": "https://github.com/webpack/webpack",
    "license": "MIT",
    "main": "lib/webpack.js",
    "maintainers": [
        {
            "name": "jhnns",
            "email": "mail@johannesewald.de"
        },
        {
            "name": "sokra",
            "email": "tobias.koppers@googlemail.com"
        },
        {
            "name": "thelarkinn",
            "email": "sean.larkin@cuw.edu"
        }
    ],
    "name": "webpack",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/webpack/webpack.git"
    },
    "scripts": {
        "appveyor:benchmark": "npm run benchmark",
        "appveyor:test": "node --max_old_space_size=4096 node_modules\\mocha\\bin\\mocha --harmony test/*.test.js",
        "beautify-lint": "beautify-lint 'lib/**/*.js' 'hot/**/*.js' 'bin/**/*.js' 'benchmark/*.js' 'test/*.js'",
        "benchmark": "mocha test/*.benchmark.js --harmony -R spec",
        "build:examples": "cd examples && node buildAll.js",
        "cover": "node --harmony ./node_modules/istanbul/lib/cli.js cover -x '**/*.runtime.js' node_modules/mocha/bin/_mocha -- test/*.test.js",
        "cover:min": "node --harmony ./node_modules/.bin/istanbul cover -x '**/*.runtime.js' --report lcovonly node_modules/mocha/bin/_mocha -- test/*.test.js",
        "lint": "eslint lib bin hot buildin test/**/webpack.config.js test/binCases/**/test.js examples/**/webpack.config.js",
        "lint-files": "npm run lint && npm run beautify-lint",
        "nsp": "nsp check --output summary",
        "pretest": "npm run lint-files",
        "publish-patch": "npm run lint && npm run beautify-lint && mocha && npm version patch && git push && git push --tags && npm publish",
        "test": "mocha test/*.test.js --harmony --check-leaks",
        "travis:benchmark": "npm run benchmark",
        "travis:lint": "npm run lint-files && npm run nsp",
        "travis:test": "npm run cover:min"
    },
    "version": "2.3.2",
    "web": "lib/webpack.web.js"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module webpack](#apidoc.module.webpack)
1.  [function <span class="apidocSignatureSpan">webpack.</span>AutomaticPrefetchPlugin (compiler)](#apidoc.element.webpack.AutomaticPrefetchPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>BannerPlugin (options)](#apidoc.element.webpack.BannerPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>CachePlugin (cache)](#apidoc.element.webpack.CachePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Compiler ()](#apidoc.element.webpack.Compiler)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Compiler.Watching (compiler, watchOptions, handler)](#apidoc.element.webpack.Compiler.Watching)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ContextModuleFactory (resolvers)](#apidoc.element.webpack.ContextModuleFactory)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ContextReplacementPlugin (resourceRegExp, newContentResource, newContentRecursive, newContentRegExp)](#apidoc.element.webpack.ContextReplacementPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DefinePlugin (definitions)](#apidoc.element.webpack.DefinePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DelegatedModule (sourceRequest, data, type, userRequest)](#apidoc.element.webpack.DelegatedModule)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DependenciesBlock ()](#apidoc.element.webpack.DependenciesBlock)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Dependency ()](#apidoc.element.webpack.Dependency)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DllPlugin (options)](#apidoc.element.webpack.DllPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DllReferencePlugin (options)](#apidoc.element.webpack.DllReferencePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DynamicEntryPlugin (context, entry)](#apidoc.element.webpack.DynamicEntryPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>EntryModuleNotFoundError (err)](#apidoc.element.webpack.EntryModuleNotFoundError)
1.  [function <span class="apidocSignatureSpan">webpack.</span>EnvironmentPlugin (keys)](#apidoc.element.webpack.EnvironmentPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>EvalDevToolModulePlugin (sourceUrlComment, moduleFilenameTemplate)](#apidoc.element.webpack.EvalDevToolModulePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>EvalSourceMapDevToolPlugin (options)](#apidoc.element.webpack.EvalSourceMapDevToolPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ExtendedAPIPlugin (compiler)](#apidoc.element.webpack.ExtendedAPIPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ExternalModuleFactoryPlugin (type, externals)](#apidoc.element.webpack.ExternalModuleFactoryPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ExternalsPlugin (type, externals)](#apidoc.element.webpack.ExternalsPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>FlagDependencyUsagePlugin ()](#apidoc.element.webpack.FlagDependencyUsagePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>HashedModuleIdsPlugin (options)](#apidoc.element.webpack.HashedModuleIdsPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>HotModuleReplacementPlugin (options)](#apidoc.element.webpack.HotModuleReplacementPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>IgnorePlugin (resourceRegExp, contextRegExp)](#apidoc.element.webpack.IgnorePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>JsonpChunkTemplatePlugin ()](#apidoc.element.webpack.JsonpChunkTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>JsonpMainTemplatePlugin ()](#apidoc.element.webpack.JsonpMainTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>JsonpTemplatePlugin (compiler)](#apidoc.element.webpack.JsonpTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>LibManifestPlugin (options)](#apidoc.element.webpack.LibManifestPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>LibraryTemplatePlugin (name, target, umdNamedDefine, auxiliaryComment)](#apidoc.element.webpack.LibraryTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>LoaderOptionsPlugin (options)](#apidoc.element.webpack.LoaderOptionsPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>LoaderTargetPlugin (target)](#apidoc.element.webpack.LoaderTargetPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>MemoryOutputFileSystem (data)](#apidoc.element.webpack.MemoryOutputFileSystem)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Module ()](#apidoc.element.webpack.Module)
1.  [function <span class="apidocSignatureSpan">webpack.</span>MultiCompiler (compilers)](#apidoc.element.webpack.MultiCompiler)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NamedModulesPlugin (options)](#apidoc.element.webpack.NamedModulesPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NewWatchingPlugin (compiler)](#apidoc.element.webpack.NewWatchingPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NoEmitOnErrorsPlugin (compiler)](#apidoc.element.webpack.NoEmitOnErrorsPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NoErrorsPlugin (compiler)](#apidoc.element.webpack.NoErrorsPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NodeEnvironmentPlugin (compiler)](#apidoc.element.webpack.NodeEnvironmentPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NodeStuffPlugin (options)](#apidoc.element.webpack.NodeStuffPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NormalModuleFactory (context, resolvers, options)](#apidoc.element.webpack.NormalModuleFactory)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NormalModuleReplacementPlugin (resourceRegExp, newResource)](#apidoc.element.webpack.NormalModuleReplacementPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Parser (options)](#apidoc.element.webpack.Parser)
1.  [function <span class="apidocSignatureSpan">webpack.</span>PrefetchPlugin (context, request)](#apidoc.element.webpack.PrefetchPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ProgressPlugin (options)](#apidoc.element.webpack.ProgressPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ProvidePlugin (definitions)](#apidoc.element.webpack.ProvidePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>SetVarMainTemplatePlugin (varExpression, copyObject)](#apidoc.element.webpack.SetVarMainTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>SourceMapDevToolPlugin (options)](#apidoc.element.webpack.SourceMapDevToolPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>UmdMainTemplatePlugin (name, options)](#apidoc.element.webpack.UmdMainTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>WatchIgnorePlugin (paths)](#apidoc.element.webpack.WatchIgnorePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>WebpackOptionsApply ()](#apidoc.element.webpack.WebpackOptionsApply)
1.  [function <span class="apidocSignatureSpan">webpack.</span>WebpackOptionsDefaulter ()](#apidoc.element.webpack.WebpackOptionsDefaulter)
1.  [function <span class="apidocSignatureSpan">webpack.</span>WebpackOptionsValidationError (validationErrors)](#apidoc.element.webpack.WebpackOptionsValidationError)
1.  [function <span class="apidocSignatureSpan">webpack.</span>validate ()](#apidoc.element.webpack.validate)
1.  [function <span class="apidocSignatureSpan">webpack.</span>validateSchema (schema, options)](#apidoc.element.webpack.validateSchema)
1.  [function <span class="apidocSignatureSpan">webpack.</span>webpack_web (options, callback)](#apidoc.element.webpack.webpack_web)
1.  object <span class="apidocSignatureSpan">webpack.</span>Compiler.Watching.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>Compiler.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>ContextModuleFactory.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>DelegatedModule.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>DependenciesBlock.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>EntryModuleNotFoundError.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>ErrorHelpers
1.  object <span class="apidocSignatureSpan">webpack.</span>ExternalModuleFactoryPlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>FlagDependencyUsagePlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>HotModuleReplacementPlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>JsonpChunkTemplatePlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>JsonpMainTemplatePlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>LibManifestPlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>MemoryOutputFileSystem.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>Module.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>ModuleFilenameHelpers
1.  object <span class="apidocSignatureSpan">webpack.</span>MultiCompiler.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>NodeStuffPlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>NormalModuleFactory.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>Parser.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>ParserHelpers
1.  object <span class="apidocSignatureSpan">webpack.</span>SizeFormatHelpers
1.  object <span class="apidocSignatureSpan">webpack.</span>SourceMapDevToolPlugin.prototype
1.  object <span class="apidocSignatureSpan">webpack.</span>dependencies
1.  object <span class="apidocSignatureSpan">webpack.</span>optimize

#### [module webpack.Compiler](#apidoc.module.webpack.Compiler)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Compiler ()](#apidoc.element.webpack.Compiler.Compiler)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.</span>Watching (compiler, watchOptions, handler)](#apidoc.element.webpack.Compiler.Watching)

#### [module webpack.Compiler.Watching](#apidoc.module.webpack.Compiler.Watching)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.</span>Watching (compiler, watchOptions, handler)](#apidoc.element.webpack.Compiler.Watching.Watching)

#### [module webpack.Compiler.Watching.prototype](#apidoc.module.webpack.Compiler.Watching.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>_done (err, compilation)](#apidoc.element.webpack.Compiler.Watching.prototype._done)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>_go ()](#apidoc.element.webpack.Compiler.Watching.prototype._go)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>close (callback)](#apidoc.element.webpack.Compiler.Watching.prototype.close)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>invalidate ()](#apidoc.element.webpack.Compiler.Watching.prototype.invalidate)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>watch (files, dirs, missing)](#apidoc.element.webpack.Compiler.Watching.prototype.watch)

#### [module webpack.Compiler.prototype](#apidoc.module.webpack.Compiler.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>compile (callback)](#apidoc.element.webpack.Compiler.prototype.compile)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>constructor ()](#apidoc.element.webpack.Compiler.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createChildCompiler (compilation, compilerName, outputOptions, plugins)](#apidoc.element.webpack.Compiler.prototype.createChildCompiler)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createCompilation ()](#apidoc.element.webpack.Compiler.prototype.createCompilation)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createContextModuleFactory ()](#apidoc.element.webpack.Compiler.prototype.createContextModuleFactory)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createNormalModuleFactory ()](#apidoc.element.webpack.Compiler.prototype.createNormalModuleFactory)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>emitAssets (compilation, callback)](#apidoc.element.webpack.Compiler.prototype.emitAssets)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>emitRecords (callback)](#apidoc.element.webpack.Compiler.prototype.emitRecords)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>isChild ()](#apidoc.element.webpack.Compiler.prototype.isChild)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>newCompilation (params)](#apidoc.element.webpack.Compiler.prototype.newCompilation)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>newCompilationParams ()](#apidoc.element.webpack.Compiler.prototype.newCompilationParams)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>purgeInputFileSystem ()](#apidoc.element.webpack.Compiler.prototype.purgeInputFileSystem)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>readRecords (callback)](#apidoc.element.webpack.Compiler.prototype.readRecords)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>run (callback)](#apidoc.element.webpack.Compiler.prototype.run)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>runAsChild (callback)](#apidoc.element.webpack.Compiler.prototype.runAsChild)
1.  [function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>watch (watchOptions, handler)](#apidoc.element.webpack.Compiler.prototype.watch)

#### [module webpack.ContextModuleFactory](#apidoc.module.webpack.ContextModuleFactory)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ContextModuleFactory (resolvers)](#apidoc.element.webpack.ContextModuleFactory.ContextModuleFactory)

#### [module webpack.ContextModuleFactory.prototype](#apidoc.module.webpack.ContextModuleFactory.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.ContextModuleFactory.prototype.</span>constructor (resolvers)](#apidoc.element.webpack.ContextModuleFactory.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">webpack.ContextModuleFactory.prototype.</span>create (data, callback)](#apidoc.element.webpack.ContextModuleFactory.prototype.create)
1.  [function <span class="apidocSignatureSpan">webpack.ContextModuleFactory.prototype.</span>resolveDependencies (fs, resource, recursive, regExp, callback)](#apidoc.element.webpack.ContextModuleFactory.prototype.resolveDependencies)

#### [module webpack.DelegatedModule](#apidoc.module.webpack.DelegatedModule)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DelegatedModule (sourceRequest, data, type, userRequest)](#apidoc.element.webpack.DelegatedModule.DelegatedModule)

#### [module webpack.DelegatedModule.prototype](#apidoc.module.webpack.DelegatedModule.prototype)
1.  boolean <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>delegated
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>build (options, compilation, resolver, fs, callback)](#apidoc.element.webpack.DelegatedModule.prototype.build)
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>constructor (sourceRequest, data, type, userRequest)](#apidoc.element.webpack.DelegatedModule.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>identifier ()](#apidoc.element.webpack.DelegatedModule.prototype.identifier)
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>needRebuild ()](#apidoc.element.webpack.DelegatedModule.prototype.needRebuild)
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>readableIdentifier ()](#apidoc.element.webpack.DelegatedModule.prototype.readableIdentifier)
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>size ()](#apidoc.element.webpack.DelegatedModule.prototype.size)
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>source ()](#apidoc.element.webpack.DelegatedModule.prototype.source)
1.  [function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>unbuild ()](#apidoc.element.webpack.DelegatedModule.prototype.unbuild)

#### [module webpack.DependenciesBlock](#apidoc.module.webpack.DependenciesBlock)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DependenciesBlock ()](#apidoc.element.webpack.DependenciesBlock.DependenciesBlock)

#### [module webpack.DependenciesBlock.prototype](#apidoc.module.webpack.DependenciesBlock.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>addBlock (block)](#apidoc.element.webpack.DependenciesBlock.prototype.addBlock)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>addDependency (dependency)](#apidoc.element.webpack.DependenciesBlock.prototype.addDependency)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>addVariable (name, expression, dependencies)](#apidoc.element.webpack.DependenciesBlock.prototype.addVariable)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>disconnect ()](#apidoc.element.webpack.DependenciesBlock.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>hasDependencies (filter)](#apidoc.element.webpack.DependenciesBlock.prototype.hasDependencies)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>sortItems ()](#apidoc.element.webpack.DependenciesBlock.prototype.sortItems)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>unseal ()](#apidoc.element.webpack.DependenciesBlock.prototype.unseal)
1.  [function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>updateHash (hash)](#apidoc.element.webpack.DependenciesBlock.prototype.updateHash)

#### [module webpack.Dependency](#apidoc.module.webpack.Dependency)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Dependency ()](#apidoc.element.webpack.Dependency.Dependency)
1.  [function <span class="apidocSignatureSpan">webpack.Dependency.</span>compare (a, b)](#apidoc.element.webpack.Dependency.compare)

#### [module webpack.DynamicEntryPlugin](#apidoc.module.webpack.DynamicEntryPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>DynamicEntryPlugin (context, entry)](#apidoc.element.webpack.DynamicEntryPlugin.DynamicEntryPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.DynamicEntryPlugin.</span>createDependency (entry, name)](#apidoc.element.webpack.DynamicEntryPlugin.createDependency)

#### [module webpack.EntryModuleNotFoundError](#apidoc.module.webpack.EntryModuleNotFoundError)
1.  [function <span class="apidocSignatureSpan">webpack.</span>EntryModuleNotFoundError (err)](#apidoc.element.webpack.EntryModuleNotFoundError.EntryModuleNotFoundError)

#### [module webpack.EntryModuleNotFoundError.prototype](#apidoc.module.webpack.EntryModuleNotFoundError.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.EntryModuleNotFoundError.prototype.</span>constructor (err)](#apidoc.element.webpack.EntryModuleNotFoundError.prototype.constructor)

#### [module webpack.ErrorHelpers](#apidoc.module.webpack.ErrorHelpers)
1.  [function <span class="apidocSignatureSpan">webpack.ErrorHelpers.</span>cleanUp (stack, message)](#apidoc.element.webpack.ErrorHelpers.cleanUp)
1.  [function <span class="apidocSignatureSpan">webpack.ErrorHelpers.</span>cutOffLoaderExecution (stack)](#apidoc.element.webpack.ErrorHelpers.cutOffLoaderExecution)
1.  [function <span class="apidocSignatureSpan">webpack.ErrorHelpers.</span>cutOffMessage (stack, message)](#apidoc.element.webpack.ErrorHelpers.cutOffMessage)

#### [module webpack.ExternalModuleFactoryPlugin](#apidoc.module.webpack.ExternalModuleFactoryPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>ExternalModuleFactoryPlugin (type, externals)](#apidoc.element.webpack.ExternalModuleFactoryPlugin.ExternalModuleFactoryPlugin)

#### [module webpack.ExternalModuleFactoryPlugin.prototype](#apidoc.module.webpack.ExternalModuleFactoryPlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.ExternalModuleFactoryPlugin.prototype.</span>apply (normalModuleFactory)](#apidoc.element.webpack.ExternalModuleFactoryPlugin.prototype.apply)

#### [module webpack.FlagDependencyUsagePlugin](#apidoc.module.webpack.FlagDependencyUsagePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>FlagDependencyUsagePlugin ()](#apidoc.element.webpack.FlagDependencyUsagePlugin.FlagDependencyUsagePlugin)

#### [module webpack.FlagDependencyUsagePlugin.prototype](#apidoc.module.webpack.FlagDependencyUsagePlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.FlagDependencyUsagePlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.FlagDependencyUsagePlugin.prototype.apply)

#### [module webpack.HotModuleReplacementPlugin](#apidoc.module.webpack.HotModuleReplacementPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>HotModuleReplacementPlugin (options)](#apidoc.element.webpack.HotModuleReplacementPlugin.HotModuleReplacementPlugin)

#### [module webpack.HotModuleReplacementPlugin.prototype](#apidoc.module.webpack.HotModuleReplacementPlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.HotModuleReplacementPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.HotModuleReplacementPlugin.prototype.apply)

#### [module webpack.JsonpChunkTemplatePlugin](#apidoc.module.webpack.JsonpChunkTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>JsonpChunkTemplatePlugin ()](#apidoc.element.webpack.JsonpChunkTemplatePlugin.JsonpChunkTemplatePlugin)

#### [module webpack.JsonpChunkTemplatePlugin.prototype](#apidoc.module.webpack.JsonpChunkTemplatePlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.JsonpChunkTemplatePlugin.prototype.</span>apply (chunkTemplate)](#apidoc.element.webpack.JsonpChunkTemplatePlugin.prototype.apply)

#### [module webpack.JsonpMainTemplatePlugin](#apidoc.module.webpack.JsonpMainTemplatePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>JsonpMainTemplatePlugin ()](#apidoc.element.webpack.JsonpMainTemplatePlugin.JsonpMainTemplatePlugin)

#### [module webpack.JsonpMainTemplatePlugin.prototype](#apidoc.module.webpack.JsonpMainTemplatePlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.JsonpMainTemplatePlugin.prototype.</span>apply (mainTemplate)](#apidoc.element.webpack.JsonpMainTemplatePlugin.prototype.apply)

#### [module webpack.LibManifestPlugin](#apidoc.module.webpack.LibManifestPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>LibManifestPlugin (options)](#apidoc.element.webpack.LibManifestPlugin.LibManifestPlugin)

#### [module webpack.LibManifestPlugin.prototype](#apidoc.module.webpack.LibManifestPlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.LibManifestPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.LibManifestPlugin.prototype.apply)

#### [module webpack.MemoryOutputFileSystem](#apidoc.module.webpack.MemoryOutputFileSystem)
1.  [function <span class="apidocSignatureSpan">webpack.</span>MemoryOutputFileSystem (data)](#apidoc.element.webpack.MemoryOutputFileSystem.MemoryOutputFileSystem)

#### [module webpack.MemoryOutputFileSystem.prototype](#apidoc.module.webpack.MemoryOutputFileSystem.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>_remove (_path, name, testFn)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype._remove)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>createReadStream (path, options)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.createReadStream)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>createWriteStream (path, options)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.createWriteStream)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>exists (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.exists)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>existsSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.existsSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>join (path, request)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.join)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>meta (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.meta)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdir (path, optArg, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdir)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdirSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdirp (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirp)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdirpSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirpSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>normalize (path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.normalize)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>pathToArray (path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.pathToArray)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readFile (path, optArg, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readFile)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readFileSync (_path, encoding)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readFileSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readdir (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readdir)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readdirSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readdirSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readlink (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readlink)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readlinkSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readlinkSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>rmdir (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.rmdir)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>rmdirSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.rmdirSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>stat (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.stat)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>statSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.statSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>unlink (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.unlink)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>unlinkSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.unlinkSync)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>writeFile (path, content, encoding, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.writeFile)
1.  [function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>writeFileSync (_path, content, encoding)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.writeFileSync)

#### [module webpack.Module](#apidoc.module.webpack.Module)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Module ()](#apidoc.element.webpack.Module.Module)

#### [module webpack.Module.prototype](#apidoc.module.webpack.Module.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>addChunk (chunk)](#apidoc.element.webpack.Module.prototype.addChunk)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>addReason (module, dependency)](#apidoc.element.webpack.Module.prototype.addReason)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>constructor ()](#apidoc.element.webpack.Module.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>disconnect ()](#apidoc.element.webpack.Module.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>hasReasonForChunk (chunk)](#apidoc.element.webpack.Module.prototype.hasReasonForChunk)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>isProvided (exportName)](#apidoc.element.webpack.Module.prototype.isProvided)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>isUsed (exportName)](#apidoc.element.webpack.Module.prototype.isUsed)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>needRebuild (fileTimestamps, contextTimestamps)](#apidoc.element.webpack.Module.prototype.needRebuild)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>removeChunk (chunk)](#apidoc.element.webpack.Module.prototype.removeChunk)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>removeReason (module, dependency)](#apidoc.element.webpack.Module.prototype.removeReason)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>rewriteChunkInReasons (oldChunk, newChunks)](#apidoc.element.webpack.Module.prototype.rewriteChunkInReasons)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>sortItems ()](#apidoc.element.webpack.Module.prototype.sortItems)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>toString ()](#apidoc.element.webpack.Module.prototype.toString)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>unbuild ()](#apidoc.element.webpack.Module.prototype.unbuild)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>unseal ()](#apidoc.element.webpack.Module.prototype.unseal)
1.  [function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>updateHash (hash)](#apidoc.element.webpack.Module.prototype.updateHash)
1.  object <span class="apidocSignatureSpan">webpack.Module.prototype.</span>build
1.  object <span class="apidocSignatureSpan">webpack.Module.prototype.</span>identifier
1.  object <span class="apidocSignatureSpan">webpack.Module.prototype.</span>nameForCondition
1.  object <span class="apidocSignatureSpan">webpack.Module.prototype.</span>readableIdentifier
1.  object <span class="apidocSignatureSpan">webpack.Module.prototype.</span>size
1.  object <span class="apidocSignatureSpan">webpack.Module.prototype.</span>source

#### [module webpack.ModuleFilenameHelpers](#apidoc.module.webpack.ModuleFilenameHelpers)
1.  [function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>createFilename (module, moduleFilenameTemplate, requestShortener)](#apidoc.element.webpack.ModuleFilenameHelpers.createFilename)
1.  [function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>createFooter (module, requestShortener)](#apidoc.element.webpack.ModuleFilenameHelpers.createFooter)
1.  [function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>matchObject (obj, str)](#apidoc.element.webpack.ModuleFilenameHelpers.matchObject)
1.  [function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>matchPart (str, test)](#apidoc.element.webpack.ModuleFilenameHelpers.matchPart)
1.  [function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>replaceDuplicates (array, fn, comparator)](#apidoc.element.webpack.ModuleFilenameHelpers.replaceDuplicates)
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_ABSOLUTE_RESOURCE_PATH
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_ALL_LOADERS
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_ALL_LOADERS_RESOURCE
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_HASH
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_ID
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_LOADERS
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_LOADERS_RESOURCE
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_QUERY
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_RESOURCE
1.  object <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>REGEXP_RESOURCE_PATH
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>ABSOLUTE_RESOURCE_PATH
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>ALL_LOADERS
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>ALL_LOADERS_RESOURCE
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>HASH
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>ID
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>LOADERS
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>LOADERS_RESOURCE
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>QUERY
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>RESOURCE
1.  string <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>RESOURCE_PATH

#### [module webpack.MultiCompiler](#apidoc.module.webpack.MultiCompiler)
1.  [function <span class="apidocSignatureSpan">webpack.</span>MultiCompiler (compilers)](#apidoc.element.webpack.MultiCompiler.MultiCompiler)

#### [module webpack.MultiCompiler.prototype](#apidoc.module.webpack.MultiCompiler.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>constructor (compilers)](#apidoc.element.webpack.MultiCompiler.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>purgeInputFileSystem ()](#apidoc.element.webpack.MultiCompiler.prototype.purgeInputFileSystem)
1.  [function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>run (callback)](#apidoc.element.webpack.MultiCompiler.prototype.run)
1.  [function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>watch (watchOptions, handler)](#apidoc.element.webpack.MultiCompiler.prototype.watch)

#### [module webpack.NodeStuffPlugin](#apidoc.module.webpack.NodeStuffPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NodeStuffPlugin (options)](#apidoc.element.webpack.NodeStuffPlugin.NodeStuffPlugin)

#### [module webpack.NodeStuffPlugin.prototype](#apidoc.module.webpack.NodeStuffPlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.NodeStuffPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.NodeStuffPlugin.prototype.apply)

#### [module webpack.NormalModuleFactory](#apidoc.module.webpack.NormalModuleFactory)
1.  [function <span class="apidocSignatureSpan">webpack.</span>NormalModuleFactory (context, resolvers, options)](#apidoc.element.webpack.NormalModuleFactory.NormalModuleFactory)

#### [module webpack.NormalModuleFactory.prototype](#apidoc.module.webpack.NormalModuleFactory.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>constructor (context, resolvers, options)](#apidoc.element.webpack.NormalModuleFactory.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>create (data, callback)](#apidoc.element.webpack.NormalModuleFactory.prototype.create)
1.  [function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>createParser (parserOptions)](#apidoc.element.webpack.NormalModuleFactory.prototype.createParser)
1.  [function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>getParser (parserOptions)](#apidoc.element.webpack.NormalModuleFactory.prototype.getParser)
1.  [function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>resolveRequestArray (contextInfo, context, array, resolver, callback)](#apidoc.element.webpack.NormalModuleFactory.prototype.resolveRequestArray)

#### [module webpack.Parser](#apidoc.module.webpack.Parser)
1.  [function <span class="apidocSignatureSpan">webpack.</span>Parser (options)](#apidoc.element.webpack.Parser.Parser)

#### [module webpack.Parser.prototype](#apidoc.module.webpack.Parser.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>constructor (options)](#apidoc.element.webpack.Parser.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterArrayPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterArrayPattern)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterAssignmentPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterAssignmentPattern)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterIdentifier (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterIdentifier)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterObjectPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterObjectPattern)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterPattern)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterRestElement (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterRestElement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>evaluate (source)](#apidoc.element.webpack.Parser.prototype.evaluate)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>evaluateExpression (expression)](#apidoc.element.webpack.Parser.prototype.evaluateExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>getRenameIdentifier (expr)](#apidoc.element.webpack.Parser.prototype.getRenameIdentifier)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>inScope (params, fn)](#apidoc.element.webpack.Parser.prototype.inScope)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>initializeEvaluating ()](#apidoc.element.webpack.Parser.prototype.initializeEvaluating)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>isHoistedStatement (statement)](#apidoc.element.webpack.Parser.prototype.isHoistedStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parse (source, initialState)](#apidoc.element.webpack.Parser.prototype.parse)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseCalculatedString (expression)](#apidoc.element.webpack.Parser.prototype.parseCalculatedString)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseCalculatedStringArray (expression)](#apidoc.element.webpack.Parser.prototype.parseCalculatedStringArray)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseString (expression)](#apidoc.element.webpack.Parser.prototype.parseString)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseStringArray (expression)](#apidoc.element.webpack.Parser.prototype.parseStringArray)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkArrayExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkArrayExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkArrayPattern (pattern)](#apidoc.element.webpack.Parser.prototype.walkArrayPattern)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkArrowFunctionExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkArrowFunctionExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkAssignmentExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkAssignmentExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkAwaitExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkAwaitExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkBinaryExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkBinaryExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkBlockStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkBlockStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkCallExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkCallExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkCatchClause (catchClause)](#apidoc.element.webpack.Parser.prototype.walkCatchClause)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkClass (classy)](#apidoc.element.webpack.Parser.prototype.walkClass)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkClassDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkClassDeclaration)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkClassExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkClassExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkConditionalExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkConditionalExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkDoWhileStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkDoWhileStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExportAllDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkExportAllDeclaration)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExportDefaultDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkExportDefaultDeclaration)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExportNamedDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkExportNamedDeclaration)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExpressionStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkExpressionStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExpressions (expressions)](#apidoc.element.webpack.Parser.prototype.walkExpressions)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkForInStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkForInStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkForOfStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkForOfStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkForStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkForStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkFunctionDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkFunctionDeclaration)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkFunctionExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkFunctionExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkIdentifier (expression)](#apidoc.element.webpack.Parser.prototype.walkIdentifier)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkIfStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkIfStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkImportDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkImportDeclaration)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkLabeledStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkLabeledStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkLogicalExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkLogicalExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkMemberExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkMemberExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkMethodDefinition (methodDefinition)](#apidoc.element.webpack.Parser.prototype.walkMethodDefinition)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkNewExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkNewExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkObjectExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkObjectExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkObjectPattern (pattern)](#apidoc.element.webpack.Parser.prototype.walkObjectPattern)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkPattern (pattern)](#apidoc.element.webpack.Parser.prototype.walkPattern)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkRestElement (pattern)](#apidoc.element.webpack.Parser.prototype.walkRestElement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkReturnStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkReturnStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSequenceExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkSequenceExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSpreadElement (expression)](#apidoc.element.webpack.Parser.prototype.walkSpreadElement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkStatements (statements)](#apidoc.element.webpack.Parser.prototype.walkStatements)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSwitchCases (switchCases)](#apidoc.element.webpack.Parser.prototype.walkSwitchCases)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSwitchStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkSwitchStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkTaggedTemplateExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkTaggedTemplateExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkTemplateLiteral (expression)](#apidoc.element.webpack.Parser.prototype.walkTemplateLiteral)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkThrowStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkThrowStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkTryStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkTryStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkUnaryExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkUnaryExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkUpdateExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkUpdateExpression)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkVariableDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkVariableDeclaration)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkVariableDeclarators (declarators)](#apidoc.element.webpack.Parser.prototype.walkVariableDeclarators)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkWhileStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkWhileStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkWithStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkWithStatement)
1.  [function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkYieldExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkYieldExpression)

#### [module webpack.ParserHelpers](#apidoc.module.webpack.ParserHelpers)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>addParsedVariableToModule (parser, name, expression)](#apidoc.element.webpack.ParserHelpers.addParsedVariableToModule)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>approve ()](#apidoc.element.webpack.ParserHelpers.approve)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>evaluateToBoolean (value)](#apidoc.element.webpack.ParserHelpers.evaluateToBoolean)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>evaluateToString (value)](#apidoc.element.webpack.ParserHelpers.evaluateToString)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>expressionIsUnsupported (message)](#apidoc.element.webpack.ParserHelpers.expressionIsUnsupported)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>requireFileAsExpression (context, pathToModule)](#apidoc.element.webpack.ParserHelpers.requireFileAsExpression)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>skipTraversal ()](#apidoc.element.webpack.ParserHelpers.skipTraversal)
1.  [function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>toConstantDependency (value)](#apidoc.element.webpack.ParserHelpers.toConstantDependency)

#### [module webpack.SizeFormatHelpers](#apidoc.module.webpack.SizeFormatHelpers)
1.  [function <span class="apidocSignatureSpan">webpack.SizeFormatHelpers.</span>formatSize (size <= 0)](#apidoc.element.webpack.SizeFormatHelpers.formatSize)

#### [module webpack.SourceMapDevToolPlugin](#apidoc.module.webpack.SourceMapDevToolPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.</span>SourceMapDevToolPlugin (options)](#apidoc.element.webpack.SourceMapDevToolPlugin.SourceMapDevToolPlugin)

#### [module webpack.SourceMapDevToolPlugin.prototype](#apidoc.module.webpack.SourceMapDevToolPlugin.prototype)
1.  [function <span class="apidocSignatureSpan">webpack.SourceMapDevToolPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.SourceMapDevToolPlugin.prototype.apply)

#### [module webpack.optimize](#apidoc.module.webpack.optimize)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>AggressiveMergingPlugin (options)](#apidoc.element.webpack.optimize.AggressiveMergingPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>AggressiveSplittingPlugin (options)](#apidoc.element.webpack.optimize.AggressiveSplittingPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>ChunkModuleIdRangePlugin (options)](#apidoc.element.webpack.optimize.ChunkModuleIdRangePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>CommonsChunkPlugin (options)](#apidoc.element.webpack.optimize.CommonsChunkPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>DedupePlugin (compiler)](#apidoc.element.webpack.optimize.DedupePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>LimitChunkCountPlugin (options)](#apidoc.element.webpack.optimize.LimitChunkCountPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>MinChunkSizePlugin (options)](#apidoc.element.webpack.optimize.MinChunkSizePlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>OccurrenceOrderPlugin (preferEntry)](#apidoc.element.webpack.optimize.OccurrenceOrderPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.optimize.</span>UglifyJsPlugin (options)](#apidoc.element.webpack.optimize.UglifyJsPlugin)

#### [module webpack.webpack_web](#apidoc.module.webpack.webpack_web)
1.  [function <span class="apidocSignatureSpan">webpack.</span>webpack_web (options, callback)](#apidoc.element.webpack.webpack_web.webpack_web)
1.  [function <span class="apidocSignatureSpan">webpack.webpack_web.</span>Compiler ()](#apidoc.element.webpack.webpack_web.Compiler)
1.  [function <span class="apidocSignatureSpan">webpack.webpack_web.</span>WebEnvironmentPlugin (inputFileSystem, outputFileSystem)](#apidoc.element.webpack.webpack_web.WebEnvironmentPlugin)
1.  [function <span class="apidocSignatureSpan">webpack.webpack_web.</span>WebpackOptionsApply ()](#apidoc.element.webpack.webpack_web.WebpackOptionsApply)
1.  [function <span class="apidocSignatureSpan">webpack.webpack_web.</span>WebpackOptionsDefaulter ()](#apidoc.element.webpack.webpack_web.WebpackOptionsDefaulter)



# <a name="apidoc.module.webpack"></a>[module webpack](#apidoc.module.webpack)

#### <a name="apidoc.element.webpack.AutomaticPrefetchPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>AutomaticPrefetchPlugin (compiler)](#apidoc.element.webpack.AutomaticPrefetchPlugin)
- description and source-code
```javascript
class AutomaticPrefetchPlugin {
	apply(compiler) {
		compiler.plugin("compilation", (compilation, params) => {
			const normalModuleFactory = params.normalModuleFactory;

			compilation.dependencyFactories.set(PrefetchDependency, normalModuleFactory);
		});
		let lastModules = null;
		compiler.plugin("after-compile", (compilation, callback) => {
			lastModules = compilation.modules
				.filter(m => m instanceof NormalModule)
				.map(m => ({
					context: m.context,
					request: m.request
				}));
			callback();
		});
		compiler.plugin("make", (compilation, callback) => {
			if(!lastModules) return callback();
			async.forEach(lastModules, (m, callback) => {
				compilation.prefetch(m.context || compiler.context, new PrefetchDependency(m.request), callback);
			}, callback);
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.BannerPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>BannerPlugin (options)](#apidoc.element.webpack.BannerPlugin)
- description and source-code
```javascript
class BannerPlugin {
	constructor(options) {
		if(arguments.length > 1)
			throw new Error("BannerPlugin only takes one argument (pass an options object)");
		if(typeof options === "string")
			options = {
				banner: options
			};
		this.options = options || {};
		this.banner = this.options.raw ? options.banner : wrapComment(options.banner);
	}

	apply(compiler) {
		const options = this.options;
		const banner = this.banner;

		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("optimize-chunk-assets", (chunks, callback) => {
				chunks.forEach((chunk) => {
					if(options.entryOnly && !chunk.isInitial()) return;

					chunk.files
						.filter(ModuleFilenameHelpers.matchObject.bind(undefined, options))
						.forEach((file) =>
							compilation.assets[file] = new ConcatSource(
								banner, "\n", compilation.assets[file]
							)
						);
				});
				callback();
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.CachePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>CachePlugin (cache)](#apidoc.element.webpack.CachePlugin)
- description and source-code
```javascript
class CachePlugin {
	constructor(cache) {
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
						new Error('CachePlugin - Cache cannot be used because of: ${compilation.notCacheable}')
					);
				}
			});
			compiler.plugin("watch-run", (compiler, callback) => {
				this.watching = true;
				callback();
			});
			compiler.plugin("run", (compiler, callback) => {
				if(!compiler._lastCompilationFileDependencies) return callback();
				const fs = compiler.inputFileSystem;
				const fileTs = compiler.fileTimestamps = {};
				async.forEach(compiler._lastCompilationFileDependencies, (file, callback) => {
					fs.stat(file, (err, stat) => {
						if(err) {
							if(err.code === "ENOENT") return callback();
							return callback(err);
						}

						if(stat.mtime)
							this.applyMtime(+stat.mtime);

						fileTs[file] = +stat.mtime || Infinity;
						callback();
					});
				}, err => {
					if(err) return callback(err);
					Object.keys(fileTs).forEach(key => {
						fileTs[key] += this.FS_ACCURENCY;
					});
					callback();
				});
			});
			compiler.plugin("after-compile", function(compilation, callback) {
				compilation.compiler._lastCompilationFileDependencies = compilation.fileDependencies;
				compilation.compiler._lastCompilationContextDependencies = compilation.contextDependencies;
				callback();
			});
		}
	}

	/* istanbul ignore next */
	applyMtime(mtime) {
		if(this.FS_ACCURENCY > 1 && mtime % 2 !== 0)
			this.FS_ACCURENCY = 1;
		else if(this.FS_ACCURENCY > 10 && mtime % 20 !== 0)
			this.FS_ACCURENCY = 10;
		else if(this.FS_ACCURENCY > 100 && mtime % 200 !== 0)
			this.FS_ACCURENCY = 100;
		else if(this.FS_ACCURENCY > 1000 && mtime % 2000 !== 0)
			this.FS_ACCURENCY = 1000;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler"></a>[function <span class="apidocSignatureSpan">webpack.</span>Compiler ()](#apidoc.element.webpack.Compiler)
- description and source-code
```javascript
function Compiler() {
	Tapable.call(this);

	this.outputPath = "";
	this.outputFileSystem = null;
	this.inputFileSystem = null;

	this.recordsInputPath = null;
	this.recordsOutputPath = null;
	this.records = {};

	this.fileTimestamps = {};
	this.contextTimestamps = {};

	this.resolvers = {
		normal: null,
		loader: null,
		context: null
	};
	var deprecationReported = false;
	this.parser = {
		plugin: function(hook, fn) {
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.plugin(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.plugin(hook, fn);
				});
			});
		}.bind(this),
		apply: function() {
			var args = arguments;
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.apply(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.apply.apply(parser, args);
				});
			});
		}.bind(this)
	};

	this.options = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.Watching"></a>[function <span class="apidocSignatureSpan">webpack.</span>Compiler.Watching (compiler, watchOptions, handler)](#apidoc.element.webpack.Compiler.Watching)
- description and source-code
```javascript
function Watching(compiler, watchOptions, handler) {
	this.startTime = null;
	this.invalid = false;
	this.error = null;
	this.stats = null;
	this.handler = handler;
	this.closed = false;
	if(typeof watchOptions === "number") {
		this.watchOptions = {
			aggregateTimeout: watchOptions
		};
	} else if(watchOptions && typeof watchOptions === "object") {
		this.watchOptions = Object.assign({}, watchOptions);
	} else {
		this.watchOptions = {};
	}
	this.watchOptions.aggregateTimeout = this.watchOptions.aggregateTimeout || 200;
	this.compiler = compiler;
	this.running = true;
	this.compiler.readRecords(function(err) {
		if(err) return this._done(err);

		this._go();
	}.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ContextModuleFactory"></a>[function <span class="apidocSignatureSpan">webpack.</span>ContextModuleFactory (resolvers)](#apidoc.element.webpack.ContextModuleFactory)
- description and source-code
```javascript
function ContextModuleFactory(resolvers) {
	Tapable.call(this);
	this.resolvers = resolvers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ContextReplacementPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>ContextReplacementPlugin (resourceRegExp, newContentResource, newContentRecursive, newContentRegExp)](#apidoc.element.webpack.ContextReplacementPlugin)
- description and source-code
```javascript
class ContextReplacementPlugin {
	constructor(resourceRegExp, newContentResource, newContentRecursive, newContentRegExp) {
		this.resourceRegExp = resourceRegExp;

		if(typeof newContentResource === "function") {
			this.newContentCallback = newContentResource;
		} else if(typeof newContentResource === "string" && typeof newContentRecursive === "object") {
			this.newContentResource = newContentResource;
			this.newContentCreateContextMap = (fs, callback) => {
				callback(null, newContentRecursive);
			};
		} else if(typeof newContentResource === "string" && typeof newContentRecursive === "function") {
			this.newContentResource = newContentResource;
			this.newContentCreateContextMap = newContentRecursive;
		} else {
			if(typeof newContentResource !== "string") {
				newContentRegExp = newContentRecursive;
				newContentRecursive = newContentResource;
				newContentResource = undefined;
			}
			if(typeof newContentRecursive !== "boolean") {
				newContentRegExp = newContentRecursive;
				newContentRecursive = undefined;
			}
			this.newContentResource = newContentResource;
			this.newContentRecursive = newContentRecursive;
			this.newContentRegExp = newContentRegExp;
		}
	}

	apply(compiler) {
		const resourceRegExp = this.resourceRegExp;
		const newContentCallback = this.newContentCallback;
		const newContentResource = this.newContentResource;
		const newContentRecursive = this.newContentRecursive;
		const newContentRegExp = this.newContentRegExp;
		const newContentCreateContextMap = this.newContentCreateContextMap;

		compiler.plugin("context-module-factory", (cmf) => {
			cmf.plugin("before-resolve", (result, callback) => {
				if(!result) return callback();
				if(resourceRegExp.test(result.request)) {
					if(typeof newContentResource !== "undefined")
						result.request = newContentResource;
					if(typeof newContentRecursive !== "undefined")
						result.recursive = newContentRecursive;
					if(typeof newContentRegExp !== "undefined")
						result.regExp = newContentRegExp;
					if(typeof newContentCallback === "function") {
						newContentCallback(result);
					} else {
						result.dependencies.forEach((d) => {
							if(d.critical)
								d.critical = false;
						});
					}
				}
				return callback(null, result);
			});
			cmf.plugin("after-resolve", (result, callback) => {
				if(!result) return callback();
				if(resourceRegExp.test(result.resource)) {
					if(typeof newContentResource !== "undefined")
						result.resource = path.resolve(result.resource, newContentResource);
					if(typeof newContentRecursive !== "undefined")
						result.recursive = newContentRecursive;
					if(typeof newContentRegExp !== "undefined")
						result.regExp = newContentRegExp;
					if(typeof newContentCreateContextMap === "function")
						result.resolveDependencies = createResolveDependenciesFromContextMap(newContentCreateContextMap);
					if(typeof newContentCallback === "function") {
						const origResource = result.resource;
						newContentCallback(result);
						if(result.resource !== origResource) {
							result.resource = path.resolve(origResource, result.resource);
						}
					} else {
						result.dependencies.forEach((d) => {
							if(d.critical)
								d.critical = false;
						});
					}
				}
				return callback(null, result);
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DefinePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>DefinePlugin (definitions)](#apidoc.element.webpack.DefinePlugin)
- description and source-code
```javascript
class DefinePlugin {
	constructor(definitions) {
		this.definitions = definitions;
	}

	apply(compiler) {
		const definitions = this.definitions;
		compiler.plugin("compilation", (compilation, params) => {
			compilation.dependencyFactories.set(ConstDependency, new NullFactory());
			compilation.dependencyTemplates.set(ConstDependency, new ConstDependency.Template());

			params.normalModuleFactory.plugin("parser", (parser) => {
				(function walkDefinitions(definitions, prefix) {
					Object.keys(definitions).forEach((key) => {
						const code = definitions[key];
						if(code && typeof code === "object" && !(code instanceof RegExp)) {
							walkDefinitions(code, prefix + key + ".");
							applyObjectDefine(prefix + key, code);
							return;
						}
						applyDefineKey(prefix, key);
						applyDefine(prefix + key, code);
					});
				}(definitions, ""));

				function stringifyObj(obj) {
					return "__webpack_require__.i({" + Object.keys(obj).map((key) => {
						const code = obj[key];
						return JSON.stringify(key) + ":" + toCode(code);
					}).join(",") + "})";
				}

				function toCode(code) {
					if(code === null) return "null";
					else if(code === undefined) return "undefined";
					else if(code instanceof RegExp && code.toString) return code.toString();
					else if(typeof code === "function" && code.toString) return "(" + code.toString() + ")";
					else if(typeof code === "object") return stringifyObj(code);
					else return code + "";
				}

				function applyDefineKey(prefix, key) {
					const splittedKey = key.split(".");
					splittedKey.slice(1).forEach((_, i) => {
						const fullKey = prefix + splittedKey.slice(0, i + 1).join(".");
						parser.plugin("can-rename " + fullKey, ParserHelpers.approve);
					});
				}

				function applyDefine(key, code) {
					const isTypeof = /^typeof\s+/.test(key);
					if(isTypeof) key = key.replace(/^typeof\s+/, "");
					let recurse = false;
					let recurseTypeof = false;
					code = toCode(code);
					if(!isTypeof) {
						parser.plugin("can-rename " + key, ParserHelpers.approve);
						parser.plugin("evaluate Identifier " + key, (expr) => {
							/**
							 * this is needed in case there is a recursion in the DefinePlugin
							 * to prevent an endless recursion
							 * e.g.: new DefinePlugin({
							 * "a": "b",
							 * "b": "a"
							 * });
							 */
							if(recurse) return;
							recurse = true;
							const res = parser.evaluate(code);
							recurse = false;
							res.setRange(expr.range);
							return res;
						});
						parser.plugin("expression " + key, ParserHelpers.toConstantDependency(code));
					}
					const typeofCode = isTypeof ? code : "typeof (" + code + ")";
					parser.plugin("evaluate typeof " + key, (expr) => {
						/**
						 * this is needed in case there is a recursion in the DefinePlugin
						 * to prevent an endless recursion
						 * e.g.: new DefinePlugin({
						 * "typeof a": "tyepof b",
						 * "typeof b": "typeof a"
						 * });
						 */
						if(recurseTypeof) return;
						recurseTypeof = true;
						const res = parser.evaluate(typeofCode);
						recurseTypeof = false;
						res.setRange(expr.range);
						return res;
					});
					parser.plugin("typeof " + key, (expr) => {
						const res = parser.evaluate(typeofCode);
						if(!res.isString()) return;
						return ParserHelpers.toConstantDependency(JSON.stringify(res.string)).bind(parser)(expr);
					});
				}

				function applyObjectDefine(key, obj) {
					const code = stringifyObj(obj);
					parser.plugin("can-rename " + key, ParserHelpers.approve);
					parser.plugin("evaluate Identifier " + key, (expr) => new BasicEvaluatedExpression().setRange(expr.range));
					parser.plugin("evaluate typeof " + key, ParserHelpers.evaluateToString("object"));
					parser.plugin("expression " + key, ParserHelpers.toConstantDependency(code));
					parser.plugin("typeof " + key, ParserHelpers.toConstantDependency(JSON.stringify("object")));
				}
			});
		} ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DelegatedModule"></a>[function <span class="apidocSignatureSpan">webpack.</span>DelegatedModule (sourceRequest, data, type, userRequest)](#apidoc.element.webpack.DelegatedModule)
- description and source-code
```javascript
function DelegatedModule(sourceRequest, data, type, userRequest) {
	Module.call(this);
	this.sourceRequest = sourceRequest;
	this.request = data.id;
	this.meta = data.meta;
	this.type = type;
	this.userRequest = userRequest;
	this.built = false;
	this.delegateData = data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DependenciesBlock"></a>[function <span class="apidocSignatureSpan">webpack.</span>DependenciesBlock ()](#apidoc.element.webpack.DependenciesBlock)
- description and source-code
```javascript
function DependenciesBlock() {
	this.dependencies = [];
	this.blocks = [];
	this.variables = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Dependency"></a>[function <span class="apidocSignatureSpan">webpack.</span>Dependency ()](#apidoc.element.webpack.Dependency)
- description and source-code
```javascript
class Dependency {
	constructor() {
		this.module = null;
	}

	isEqualResource() {
		return false;
	}

	// Returns the referenced module and export
	getReference() {
		if(!this.module) return null;
		return {
			module: this.module,
			importedNames: true, // true: full object, false: only sideeffects/no export, array of strings: the exports with this names
		};
	}

	// Returns the exported names
	getExports() {
		return null;
	}

	getWarnings() {
		return null;
	}

	getErrors() {
		return null;
	}

	updateHash(hash) {
		hash.update((this.module && this.module.id) + "");
	}

	disconnect() {
		this.module = null;
	}

	compare(a, b) {
		return compareLocations(a.loc, b.loc);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DllPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>DllPlugin (options)](#apidoc.element.webpack.DllPlugin)
- description and source-code
```javascript
class DllPlugin {
	constructor(options) {
		this.options = options;
	}

	apply(compiler) {
		compiler.plugin("entry-option", (context, entry) => {
			function itemToPlugin(item, name) {
				if(Array.isArray(item))
					return new DllEntryPlugin(context, item, name);
				else
					throw new Error("DllPlugin: supply an Array as entry");
			}
			if(typeof entry === "object" && !Array.isArray(entry)) {
				Object.keys(entry).forEach(name => {
					compiler.apply(itemToPlugin(entry[name], name));
				});
			} else {
				compiler.apply(itemToPlugin(entry, "main"));
			}
			return true;
		});
		compiler.apply(new LibManifestPlugin(this.options));
		compiler.apply(new FlagInitialModulesAsUsedPlugin());
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DllReferencePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>DllReferencePlugin (options)](#apidoc.element.webpack.DllReferencePlugin)
- description and source-code
```javascript
class DllReferencePlugin {
	constructor(options) {
		this.options = options;
	}

	apply(compiler) {
		compiler.plugin("compilation", (compilation, params) => {
			const normalModuleFactory = params.normalModuleFactory;
			compilation.dependencyFactories.set(DelegatedSourceDependency, normalModuleFactory);
		});

		compiler.plugin("before-compile", (params, callback) => {
			const manifest = this.options.manifest;
			if(typeof manifest === "string") {
				params.compilationDependencies.push(manifest);
				compiler.inputFileSystem.readFile(manifest, function(err, result) {
					if(err) return callback(err);
					params["dll reference " + manifest] = JSON.parse(result.toString("utf-8"));
					return callback();
				});
			} else {
				return callback();
			}
		});

		compiler.plugin("compile", (params) => {
			let manifest = this.options.manifest;
			if(typeof manifest === "string") {
				manifest = params["dll reference " + manifest];
			}
			const name = this.options.name || manifest.name;
			const sourceType = this.options.sourceType || "var";
			const externals = {};
			const source = "dll-reference " + name;
			externals[source] = name;
			params.normalModuleFactory.apply(new ExternalModuleFactoryPlugin(sourceType, externals));
			params.normalModuleFactory.apply(new DelegatedModuleFactoryPlugin({
				source: source,
				type: this.options.type,
				scope: this.options.scope,
				context: this.options.context || compiler.options.context,
				content: this.options.content || manifest.content,
				extensions: this.options.extensions
			}));
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DynamicEntryPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>DynamicEntryPlugin (context, entry)](#apidoc.element.webpack.DynamicEntryPlugin)
- description and source-code
```javascript
class DynamicEntryPlugin {
	constructor(context, entry) {
		this.context = context;
		this.entry = entry;
	}

	apply(compiler) {
		compiler.plugin("compilation", (compilation, params) => {
			const multiModuleFactory = new MultiModuleFactory();
			const normalModuleFactory = params.normalModuleFactory;

			compilation.dependencyFactories.set(MultiEntryDependency, multiModuleFactory);
			compilation.dependencyFactories.set(SingleEntryDependency, normalModuleFactory);
		});

		compiler.plugin("make", (compilation, callback) => {
			const addEntry = (entry, name) => {
				const dep = DynamicEntryPlugin.createDependency(entry, name);
				return new Promise((resolve, reject) => {
					compilation.addEntry(this.context, dep, name, (err) => {
						if(err) return reject(err);
						resolve();
					});
				});
			};

			Promise.resolve(this.entry()).then((entry) => {
				if(typeof entry === "string" || Array.isArray(entry)) {
					addEntry(entry, "main").then(() => callback(), callback);
				} else if(typeof entry === "object") {
					Promise.all(Object.keys(entry).map((name) => {
						return addEntry(entry[name], name);
					})).then(() => callback(), callback);
				}
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.EntryModuleNotFoundError"></a>[function <span class="apidocSignatureSpan">webpack.</span>EntryModuleNotFoundError (err)](#apidoc.element.webpack.EntryModuleNotFoundError)
- description and source-code
```javascript
function EntryModuleNotFoundError(err) {
	Error.call(this);
	this.name = "EntryModuleNotFoundError";
	this.message = "Entry module not found: " + err;
	this.details = err.details;
	this.error = err;
	Error.captureStackTrace(this, EntryModuleNotFoundError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.EnvironmentPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>EnvironmentPlugin (keys)](#apidoc.element.webpack.EnvironmentPlugin)
- description and source-code
```javascript
class EnvironmentPlugin {
	constructor(keys) {
		if(Array.isArray(keys)) {
			this.keys = keys;
			this.defaultValues = {};
		} else if(keys && typeof keys === "object") {
			this.keys = Object.keys(keys);
			this.defaultValues = keys;
		} else {
			this.keys = Array.prototype.slice.call(arguments);
			this.defaultValues = {};
		}
	}

	apply(compiler) {
		const definitions = this.keys.reduce((defs, key) => {
			const value = process.env[key] !== undefined ? process.env[key] : this.defaultValues[key];

			if(value === undefined) {
				compiler.plugin("this-compilation", compilation => {
					const error = new Error(
						'EnvironmentPlugin - ${key} environment variable is undefined.\n\n' +
						"You can pass an object with default values to suppress this warning.\n" +
						"See https://webpack.js.org/plugins/environment-plugin for example."
					);

					error.name = "EnvVariableNotDefinedError";
					compilation.warnings.push(error);
				});
			}

			defs['process.env.${key}'] = typeof value === "undefined" ? "undefined" : JSON.stringify(value);

			return defs;
		}, {});

		compiler.apply(new DefinePlugin(definitions));
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.EvalDevToolModulePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>EvalDevToolModulePlugin (sourceUrlComment, moduleFilenameTemplate)](#apidoc.element.webpack.EvalDevToolModulePlugin)
- description and source-code
```javascript
class EvalDevToolModulePlugin {
	constructor(sourceUrlComment, moduleFilenameTemplate) {
		this.sourceUrlComment = sourceUrlComment;
		this.moduleFilenameTemplate = moduleFilenameTemplate;
	}

	apply(compiler) {
		compiler.plugin("compilation", (compilation) => {
			compilation.moduleTemplate.apply(new EvalDevToolModuleTemplatePlugin(this.sourceUrlComment, this.moduleFilenameTemplate));
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.EvalSourceMapDevToolPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>EvalSourceMapDevToolPlugin (options)](#apidoc.element.webpack.EvalSourceMapDevToolPlugin)
- description and source-code
```javascript
class EvalSourceMapDevToolPlugin {
	constructor(options) {
		if(arguments.length > 1)
			throw new Error("EvalSourceMapDevToolPlugin only takes one argument (pass an options object)");
		if(typeof options === "string") {
			options = {
				append: options
			};
		}
		if(!options) options = {};
		this.options = options;
	}

	apply(compiler) {
		const options = this.options;
		compiler.plugin("compilation", (compilation) => {
			new SourceMapDevToolModuleOptionsPlugin(options).apply(compilation);
			compilation.moduleTemplate.apply(new EvalSourceMapDevToolModuleTemplatePlugin(compilation, options));
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ExtendedAPIPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>ExtendedAPIPlugin (compiler)](#apidoc.element.webpack.ExtendedAPIPlugin)
- description and source-code
```javascript
class ExtendedAPIPlugin {
	apply(compiler) {
		compiler.plugin("compilation", (compilation, params) => {
			compilation.dependencyFactories.set(ConstDependency, new NullFactory());
			compilation.dependencyTemplates.set(ConstDependency, new ConstDependency.Template());
			compilation.mainTemplate.plugin("require-extensions", function(source, chunk, hash) {
				const buf = [source];
				buf.push("");
				buf.push("// __webpack_hash__");
				buf.push('${this.requireFn}.h = ${JSON.stringify(hash)};');
				return this.asString(buf);
			});
			compilation.mainTemplate.plugin("global-hash", () => true);

			params.normalModuleFactory.plugin("parser", (parser, parserOptions) => {
				Object.keys(REPLACEMENTS).forEach(key => {
					parser.plugin('expression ${key}', ParserHelpers.toConstantDependency(REPLACEMENTS[key]));
					parser.plugin('evaluate typeof ${key}', ParserHelpers.evaluateToString(REPLACEMENT_TYPES[key]));
				});
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ExternalModuleFactoryPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>ExternalModuleFactoryPlugin (type, externals)](#apidoc.element.webpack.ExternalModuleFactoryPlugin)
- description and source-code
```javascript
function ExternalModuleFactoryPlugin(type, externals) {
	this.type = type;
	this.externals = externals;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ExternalsPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>ExternalsPlugin (type, externals)](#apidoc.element.webpack.ExternalsPlugin)
- description and source-code
```javascript
class ExternalsPlugin {
	constructor(type, externals) {
		this.type = type;
		this.externals = externals;
	}
	apply(compiler) {
		compiler.plugin("compile", (params) => {
			params.normalModuleFactory.apply(new ExternalModuleFactoryPlugin(this.type, this.externals));
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.FlagDependencyUsagePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>FlagDependencyUsagePlugin ()](#apidoc.element.webpack.FlagDependencyUsagePlugin)
- description and source-code
```javascript
function FlagDependencyUsagePlugin() {

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.HashedModuleIdsPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>HashedModuleIdsPlugin (options)](#apidoc.element.webpack.HashedModuleIdsPlugin)
- description and source-code
```javascript
class HashedModuleIdsPlugin {
	constructor(options) {
		this.options = Object.assign({
			hashFunction: "md5",
			hashDigest: "base64",
			hashDigestLength: 4
		}, options);
	}

	apply(compiler) {
		const options = this.options;
		compiler.plugin("compilation", (compilation) => {
			const usedIds = new Set();
			compilation.plugin("before-module-ids", (modules) => {
				modules.forEach((module) => {
					if(module.id === null && module.libIdent) {
						const id = module.libIdent({
							context: this.options.context || compiler.options.context
						});
						const hash = createHash(options.hashFunction);
						hash.update(id);
						const hashId = hash.digest(options.hashDigest);
						let len = options.hashDigestLength;
						while(usedIds.has(hashId.substr(0, len)))
							len++;
						module.id = hashId.substr(0, len);
						usedIds.add(module.id);
					}
				});
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.HotModuleReplacementPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>HotModuleReplacementPlugin (options)](#apidoc.element.webpack.HotModuleReplacementPlugin)
- description and source-code
```javascript
function HotModuleReplacementPlugin(options) {
	options = options || {};
	this.multiStep = options.multiStep;
	this.fullBuildTimeout = options.fullBuildTimeout || 200;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.IgnorePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>IgnorePlugin (resourceRegExp, contextRegExp)](#apidoc.element.webpack.IgnorePlugin)
- description and source-code
```javascript
class IgnorePlugin {
	constructor(resourceRegExp, contextRegExp) {
		this.resourceRegExp = resourceRegExp;
		this.contextRegExp = contextRegExp;
	}

	apply(compiler) {
		const resourceRegExp = this.resourceRegExp;
		const contextRegExp = this.contextRegExp;
		compiler.plugin("normal-module-factory", (nmf) => {
			nmf.plugin("before-resolve", (result, callback) => {
				if(!result) return callback();
				if(resourceRegExp.test(result.request) &&
					(!contextRegExp || contextRegExp.test(result.context))) {
					return callback();
				}
				return callback(null, result);
			});
		});
		compiler.plugin("context-module-factory", (cmf) => {
			cmf.plugin("before-resolve", (result, callback) => {
				if(!result) return callback();
				if(resourceRegExp.test(result.request)) {
					return callback();
				}
				return callback(null, result);
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.JsonpChunkTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>JsonpChunkTemplatePlugin ()](#apidoc.element.webpack.JsonpChunkTemplatePlugin)
- description and source-code
```javascript
function JsonpChunkTemplatePlugin() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.JsonpMainTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>JsonpMainTemplatePlugin ()](#apidoc.element.webpack.JsonpMainTemplatePlugin)
- description and source-code
```javascript
function JsonpMainTemplatePlugin() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.JsonpTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>JsonpTemplatePlugin (compiler)](#apidoc.element.webpack.JsonpTemplatePlugin)
- description and source-code
```javascript
class JsonpTemplatePlugin {
	apply(compiler) {
		compiler.plugin("this-compilation", (compilation) => {
			compilation.mainTemplate.apply(new JsonpMainTemplatePlugin());
			compilation.chunkTemplate.apply(new JsonpChunkTemplatePlugin());
			compilation.hotUpdateChunkTemplate.apply(new JsonpHotUpdateChunkTemplatePlugin());
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.LibManifestPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>LibManifestPlugin (options)](#apidoc.element.webpack.LibManifestPlugin)
- description and source-code
```javascript
function LibManifestPlugin(options) {
	this.options = options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.LibraryTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>LibraryTemplatePlugin (name, target, umdNamedDefine, auxiliaryComment)](#apidoc.element.webpack.LibraryTemplatePlugin)
- description and source-code
```javascript
class LibraryTemplatePlugin {

	constructor(name, target, umdNamedDefine, auxiliaryComment) {
		this.name = name;
		this.target = target;
		this.umdNamedDefine = umdNamedDefine;
		this.auxiliaryComment = auxiliaryComment;
	}

	apply(compiler) {
		compiler.plugin("this-compilation", (compilation) => {
			switch(this.target) {
				case "var":
					compilation.apply(new SetVarMainTemplatePlugin('var ${accessorAccess(false, this.name)}'));
					break;
				case "assign":
					compilation.apply(new SetVarMainTemplatePlugin(accessorAccess(undefined, this.name)));
					break;
				case "this":
				case "window":
				case "global":
					if(this.name)
						compilation.apply(new SetVarMainTemplatePlugin(accessorAccess(this.target, this.name)));
					else
						compilation.apply(new SetVarMainTemplatePlugin(this.target, true));
					break;
				case "commonjs":
					if(this.name)
						compilation.apply(new SetVarMainTemplatePlugin(accessorAccess("exports", this.name)));
					else
						compilation.apply(new SetVarMainTemplatePlugin("exports", true));
					break;
				case "commonjs2":
				case "commonjs-module":
					compilation.apply(new SetVarMainTemplatePlugin("module.exports"));
					break;
				case "amd":
					var AmdMainTemplatePlugin = require("./AmdMainTemplatePlugin");
					compilation.apply(new AmdMainTemplatePlugin(this.name));
					break;
				case "umd":
				case "umd2":
					var UmdMainTemplatePlugin = require("./UmdMainTemplatePlugin");
					compilation.apply(new UmdMainTemplatePlugin(this.name, {
						optionalAmdExternalAsGlobal: this.target === "umd2",
						namedDefine: this.umdNamedDefine,
						auxiliaryComment: this.auxiliaryComment
					}));
					break;
				case "jsonp":
					var JsonpExportMainTemplatePlugin = require("./JsonpExportMainTemplatePlugin");
					compilation.apply(new JsonpExportMainTemplatePlugin(this.name));
					break;
				default:
					throw new Error('${this.target} is not a valid Library target');
			}
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.LoaderOptionsPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>LoaderOptionsPlugin (options)](#apidoc.element.webpack.LoaderOptionsPlugin)
- description and source-code
```javascript
class LoaderOptionsPlugin {
	constructor(options) {
		if(typeof options !== "object") options = {};
		if(!options.test) options.test = {
			test: () => true
		};
		this.options = options;
	}

	apply(compiler) {
		const options = this.options;
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("normal-module-loader", (context, module) => {
				const resource = module.resource;
				if(!resource) return;
				const i = resource.indexOf("?");
				if(ModuleFilenameHelpers.matchObject(options, i < 0 ? resource : resource.substr(0, i))) {
					const filterSet = new Set(["include", "exclude", "test"]);
					Object.keys(options)
						.filter((key) => !filterSet.has(key))
						.forEach((key) => context[key] = options[key]);
				}
			});
		});
	}
}
```
- example usage
```shell
...
				switch(err.params.additionalProperty) {
					case "debug":
						return '${baseMessage}\n' +
							"The 'debug' property was removed in webpack 2.\n" +
							"Loaders should be updated to allow passing this option via loader options in module.rules.\n" +
							"Until loaders are updated one can use the LoaderOptionsPlugin to switch loaders into debug mode:\n" +
							"plugins: [\n" +
							"  new webpack.LoaderOptionsPlugin({\n" +
							"    debug: true\n" +
							"  })\n" +
							"]";
				}
				return baseMessage + "\n" +
					"For typos: please correct them.\n" +
					"For loader options: webpack 2 no longer allows custom properties in configuration.\n" +
...
```

#### <a name="apidoc.element.webpack.LoaderTargetPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>LoaderTargetPlugin (target)](#apidoc.element.webpack.LoaderTargetPlugin)
- description and source-code
```javascript
class LoaderTargetPlugin {
	constructor(target) {
		this.target = target;
	}

	apply(compiler) {
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("normal-module-loader", (loaderContext) => loaderContext.target = this.target);
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem"></a>[function <span class="apidocSignatureSpan">webpack.</span>MemoryOutputFileSystem (data)](#apidoc.element.webpack.MemoryOutputFileSystem)
- description and source-code
```javascript
function MemoryFileSystem(data) {
	this.data = data || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Module"></a>[function <span class="apidocSignatureSpan">webpack.</span>Module ()](#apidoc.element.webpack.Module)
- description and source-code
```javascript
function Module() {
	DependenciesBlock.call(this);
	this.context = null;
	this.reasons = [];
	this.debugId = debugId++;
	this.lastId = -1;
	this.id = null;
	this.portableId = null;
	this.index = null;
	this.index2 = null;
	this.depth = null;
	this.used = null;
	this.usedExports = null;
	this.providedExports = null;
	this.chunks = [];
	this.warnings = [];
	this.dependenciesWarnings = [];
	this.errors = [];
	this.dependenciesErrors = [];
	this.strict = false;
	this.meta = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MultiCompiler"></a>[function <span class="apidocSignatureSpan">webpack.</span>MultiCompiler (compilers)](#apidoc.element.webpack.MultiCompiler)
- description and source-code
```javascript
function MultiCompiler(compilers) {
	Tapable.call(this);
	if(!Array.isArray(compilers)) {
		compilers = Object.keys(compilers).map(function(name) {
			compilers[name].name = name;
			return compilers[name];
		});
	}
	this.compilers = compilers;

	function delegateProperty(name) {
		Object.defineProperty(this, name, {
			configurable: false,
			get: function() {
				throw new Error("Cannot read " + name + " of a MultiCompiler");
			},
			set: function(value) {
				this.compilers.forEach(function(compiler) {
					compiler[name] = value;
				});
			}.bind(this)
		});
	}
	delegateProperty.call(this, "outputFileSystem");
	delegateProperty.call(this, "inputFileSystem");

	Object.defineProperty(this, "outputPath", {
		configurable: false,
		get: function() {
			var commonPath = compilers[0].outputPath;
			for(var i = 1; i < compilers.length; i++) {
				while(compilers[i].outputPath.indexOf(commonPath) !== 0 && /[\/\\]/.test(commonPath)) {
					commonPath = commonPath.replace(/[\/\\][^\/\\]*$/, "");
				}
			}
			if(!commonPath && compilers[0].outputPath[0] === "/") return "/";
			return commonPath;
		}
	});

	var doneCompilers = 0;
	var compilerStats = [];
	this.compilers.forEach(function(compiler, idx) {
		var compilerDone = false;
		compiler.plugin("done", function(stats) {
			if(!compilerDone) {
				compilerDone = true;
				doneCompilers++;
			}
			compilerStats[idx] = stats;
			if(doneCompilers === this.compilers.length) {
				this.applyPlugins("done", new MultiStats(compilerStats));
			}
		}.bind(this));
		compiler.plugin("invalid", function() {
			if(compilerDone) {
				compilerDone = false;
				doneCompilers--;
			}
			this.applyPlugins("invalid");
		}.bind(this));
	}, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NamedModulesPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NamedModulesPlugin (options)](#apidoc.element.webpack.NamedModulesPlugin)
- description and source-code
```javascript
class NamedModulesPlugin {
	constructor(options) {
		this.options = options || {};
	}

	apply(compiler) {
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("before-module-ids", (modules) => {
				modules.forEach((module) => {
					if(module.id === null && module.libIdent) {
						module.id = module.libIdent({
							context: this.options.context || compiler.options.context
						});
					}
				});
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NewWatchingPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NewWatchingPlugin (compiler)](#apidoc.element.webpack.NewWatchingPlugin)
- description and source-code
```javascript
class NewWatchingPlugin {
	apply(compiler) {
		compiler.plugin("compilation", function(compilation) {
			compilation.warnings.push(new Error("The 'NewWatchingPlugin' is no longer necessary (now default)"));
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NoEmitOnErrorsPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NoEmitOnErrorsPlugin (compiler)](#apidoc.element.webpack.NoEmitOnErrorsPlugin)
- description and source-code
```javascript
class NoEmitOnErrorsPlugin {
	apply(compiler) {
		compiler.plugin("should-emit", (compilation) => {
			if(compilation.errors.length > 0)
				return false;
		});
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("should-record", () => {
				if(compilation.errors.length > 0)
					return false;
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NoErrorsPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NoErrorsPlugin (compiler)](#apidoc.element.webpack.NoErrorsPlugin)
- description and source-code
```javascript
class NoErrorsPlugin {
	apply(compiler) {
		compiler.plugin("should-emit", (compilation) => {
			if(!deprecationReported) {
				compilation.warnings.push("webpack: Using NoErrorsPlugin is deprecated.\n" +
					"Use NoEmitOnErrorsPlugin instead.\n");
				deprecationReported = true;
			}
			if(compilation.errors.length > 0)
				return false;
		});
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("should-record", () => {
				if(compilation.errors.length > 0)
					return false;
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NodeEnvironmentPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NodeEnvironmentPlugin (compiler)](#apidoc.element.webpack.NodeEnvironmentPlugin)
- description and source-code
```javascript
class NodeEnvironmentPlugin {
	apply(compiler) {
		compiler.inputFileSystem = new CachedInputFileSystem(new NodeJsInputFileSystem(), 60000);
		const inputFileSystem = compiler.inputFileSystem;
		compiler.outputFileSystem = new NodeOutputFileSystem();
		compiler.watchFileSystem = new NodeWatchFileSystem(compiler.inputFileSystem);
		compiler.plugin("before-run", (compiler, callback) => {
			if(compiler.inputFileSystem === inputFileSystem)
				inputFileSystem.purge();
			callback();
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NodeStuffPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NodeStuffPlugin (options)](#apidoc.element.webpack.NodeStuffPlugin)
- description and source-code
```javascript
function NodeStuffPlugin(options) {
	this.options = options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NormalModuleFactory"></a>[function <span class="apidocSignatureSpan">webpack.</span>NormalModuleFactory (context, resolvers, options)](#apidoc.element.webpack.NormalModuleFactory)
- description and source-code
```javascript
function NormalModuleFactory(context, resolvers, options) {
	Tapable.call(this);
	this.resolvers = resolvers;
	this.ruleSet = new RuleSet(options.rules || options.loaders);
	this.cachePredicate = typeof options.unsafeCache === "function" ? options.unsafeCache : Boolean.bind(null, options.unsafeCache);
	this.context = context || "";
	this.parserCache = {};
	this.plugin("factory", function() {
		var _this = this;
		return function(result, callback) {
			var resolver = _this.applyPluginsWaterfall0("resolver", null);

			// Ignored
			if(!resolver) return callback();

			resolver(result, function onDoneResolving(err, data) {
				if(err) return callback(err);

				// Ignored
				if(!data) return callback();

				// direct module
				if(typeof data.source === "function")
					return callback(null, data);

				_this.applyPluginsAsyncWaterfall("after-resolve", data, function(err, result) {
					if(err) return callback(err);

					// Ignored
					if(!result) return callback();

					var createdModule = _this.applyPluginsBailResult("create-module", result);
					if(!createdModule) {

						if(!result.request) {
							return callback(new Error("Empty dependency (no request)"));
						}

						createdModule = new NormalModule(
							result.request,
							result.userRequest,
							result.rawRequest,
							result.loaders,
							result.resource,
							result.parser
						);
					}

					createdModule = _this.applyPluginsWaterfall0("module", createdModule);

					return callback(null, createdModule);
				});
			});
		};
	});
	this.plugin("resolver", function() {
		var _this = this;
		return function(data, callback) {
			var contextInfo = data.contextInfo;
			var context = data.context;
			var request = data.request;
			var resolveContextInfo = {};

			var noAutoLoaders = /^-?!/.test(request);
			var noPrePostAutoLoaders = /^!!/.test(request);
			var noPostAutoLoaders = /^-!/.test(request);
			var elements = request.replace(/^-?!+/, "").replace(/!!+/g, "!").split("!");
			var resource = elements.pop();
			elements = elements.map(identToLoaderRequest);

			async.parallel([
				function(callback) {
					_this.resolveRequestArray(resolveContextInfo, context, elements, _this.resolvers.loader, callback);
				},
				function(callback) {
					if(resource === "" || resource[0] === "?")
						return callback(null, {
							resource: resource
						});

					_this.resolvers.normal.resolve(resolveContextInfo, context, resource, function(err, resource, resourceResolveData) {
						if(err) return callback(err);
						callback(null, {
							resourceResolveData: resourceResolveData,
							resource: resource,
						});
					});
				}
			], function(err, results) {
				if(err) return callback(err);
				var loaders = results[0];
				var resourceResolveData = results[1].resourceResolveData;
				resource = results[1].resource;

				// translate option idents
				try {
					loaders.forEach(function(item) {
						if(typeof item.options === "string" && /^\?/.test(item.options)) {
							item.options = _this.ruleSet.findOptionsByIdent(item.options.substr(1));
						}
					});
				} catch(e) {
					return callback(e);
				}

				if(resource === false)
					return callback(null,
						new RawModule("/* (ignored) */",
							"ignored " + context + " " + request,
							request + " (ignored)")); // ignored

				var userRequest = loaders.map(loaderToIdent).concat([resource]).join("!");

				var resourcePath = resource;
				var resourceQuery = "";
				var queryIndex = resourcePath.indexOf("?");
				if(queryIndex >= 0) {
					resourceQuery = resourcePath.substr(queryIndex);
					resourcePath = resourcePath.substr(0, queryIndex);
				}

				var result = _this.ruleSet.exec({
					resource: resourcePath,
					resourceQuery: resourceQuery,
					issuer: contextInfo.issuer,
					compiler: contextInfo.compiler
				});
				var settings = {};
				var useLoadersPost = [];
				var useLoaders = [];
				var useLoadersPre = [];
				result.forEac ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NormalModuleReplacementPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NormalModuleReplacementPlugin (resourceRegExp, newResource)](#apidoc.element.webpack.NormalModuleReplacementPlugin)
- description and source-code
```javascript
class NormalModuleReplacementPlugin {
	constructor(resourceRegExp, newResource) {
		this.resourceRegExp = resourceRegExp;
		this.newResource = newResource;
	}

	apply(compiler) {
		const resourceRegExp = this.resourceRegExp;
		const newResource = this.newResource;
		compiler.plugin("normal-module-factory", (nmf) => {
			nmf.plugin("before-resolve", (result, callback) => {
				if(!result) return callback();
				if(resourceRegExp.test(result.request)) {
					if(typeof newResource === "function") {
						newResource(result);
					} else {
						result.request = newResource;
					}
				}
				return callback(null, result);
			});
			nmf.plugin("after-resolve", (result, callback) => {
				if(!result) return callback();
				if(resourceRegExp.test(result.resource)) {
					if(typeof newResource === "function") {
						newResource(result);
					} else {
						result.resource = path.resolve(path.dirname(result.resource), newResource);
					}
				}
				return callback(null, result);
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser"></a>[function <span class="apidocSignatureSpan">webpack.</span>Parser (options)](#apidoc.element.webpack.Parser)
- description and source-code
```javascript
function Parser(options) {
	Tapable.call(this);
	this.options = options;
	this.initializeEvaluating();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.PrefetchPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>PrefetchPlugin (context, request)](#apidoc.element.webpack.PrefetchPlugin)
- description and source-code
```javascript
class PrefetchPlugin {

	constructor(context, request) {
		if(!request) {
			this.request = context;
		} else {
			this.context = context;
			this.request = request;
		}
	}

	apply(compiler) {
		compiler.plugin("compilation", (compilation, params) => {
			const normalModuleFactory = params.normalModuleFactory;

			compilation.dependencyFactories.set(PrefetchDependency, normalModuleFactory);
		});
		compiler.plugin("make", (compilation, callback) => {
			compilation.prefetch(this.context || compiler.context, new PrefetchDependency(this.request), callback);
		});
	}

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ProgressPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>ProgressPlugin (options)](#apidoc.element.webpack.ProgressPlugin)
- description and source-code
```javascript
class ProgressPlugin {

	constructor(options) {
		if(typeof options === "function") {
			options = {
				handler: options
			};
		}
		options = options || {};
		this.profile = options.profile;
		this.handler = options.handler;
	}

	apply(compiler) {
		const handler = this.handler || defaultHandler;
		const profile = this.profile;
		if(compiler.compilers) {
			const states = new Array(compiler.compilers.length);
			compiler.compilers.forEach(function(compiler, idx) {
				compiler.apply(new ProgressPlugin((p, msg) => {
					states[idx] = Array.prototype.slice.apply(arguments);
					handler.apply(null, [
						states.map(state => state && state[0] || 0).reduce((a, b) => a + b) / states.length,
						'[${idx}] ${msg}'
					].concat(Array.prototype.slice.call(arguments, 2)));
				}));
			});
		} else {
			let lastModulesCount = 0;
			let moduleCount = 500;
			let doneModules = 0;
			const activeModules = [];

			const update = function update(module) {
				handler(
					0.1 + (doneModules / Math.max(lastModulesCount, moduleCount)) * 0.6,
					"building modules",
					'${doneModules}/${moduleCount} modules',
					'${activeModules.length} active',
					activeModules[activeModules.length - 1]
				);
			};

			const moduleDone = function moduleDone(module) {
				doneModules++;
				const ident = module.identifier();
				if(ident) {
					const idx = activeModules.indexOf(ident);
					if(idx >= 0) activeModules.splice(idx, 1);
				}
				update();
			};
			compiler.plugin("compilation", function(compilation) {
				if(compilation.compiler.isChild()) return;
				lastModulesCount = moduleCount;
				moduleCount = 0;
				doneModules = 0;
				handler(0, "compiling");
				compilation.plugin("build-module", function(module) {
					moduleCount++;
					const ident = module.identifier();
					if(ident) {
						activeModules.push(ident);
					}
					update();
				});
				compilation.plugin("failed-module", moduleDone);
				compilation.plugin("succeed-module", moduleDone);
				const syncHooks = {
					"seal": [0.71, "sealing"],
					"optimize": [0.72, "optimizing"],
					"optimize-modules-basic": [0.73, "basic module optimization"],
					"optimize-modules": [0.74, "module optimization"],
					"optimize-modules-advanced": [0.75, "advanced module optimization"],
					"optimize-chunks-basic": [0.76, "basic chunk optimization"],
					"optimize-chunks": [0.77, "chunk optimization"],
					"optimize-chunks-advanced": [0.78, "advanced chunk optimization"],
					// optimize-tree
					"revive-modules": [0.80, "module reviving"],
					"optimize-module-order": [0.81, "module order optimization"],
					"optimize-module-ids": [0.82, "module id optimization"],
					"revive-chunks": [0.83, "chunk reviving"],
					"optimize-chunk-order": [0.84, "chunk order optimization"],
					"optimize-chunk-ids": [0.85, "chunk id optimization"],
					"before-hash": [0.86, "hashing"],
					"before-module-assets": [0.87, "module assets processing"],
					"before-chunk-assets": [0.88, "chunk assets processing"],
					"additional-chunk-assets": [0.89, "additional chunk assets processing"],
					"record": [0.90, "recording"]
				};
				Object.keys(syncHooks).forEach(name => {
					let pass = 0;
					const settings = syncHooks[name];
					compilation.plugin(name, () => {
						if(pass++ > 0)
							handler(settings[0], settings[1], 'pass ${pass}');
						else
							handler(settings[0], settings[1]);
					});
				});
				compilation.plugin("optimize-tree", (chunks, modules, callback) => {
					handler(0.79, "module and chunk tree optimization");
					callback();
				});
				compilation.plugin("additional-assets", callback => {
					handler(0.91, "additional asset processing");
					callback();
				});
				compilation.plugin("optimize-chunk-assets", (chunks, callback) => {
					handler(0.92, "chunk asset optimization");
					callback();
				});
				compilation.plugin("optimize-assets", (assets, callback) => {
					handler(0.94, "asset optimization");
					callback(); ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ProvidePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>ProvidePlugin (definitions)](#apidoc.element.webpack.ProvidePlugin)
- description and source-code
```javascript
class ProvidePlugin {
	constructor(definitions) {
		this.definitions = definitions;
	}

	apply(compiler) {
		const definitions = this.definitions;
		compiler.plugin("compilation", (compilation, params) => {
			compilation.dependencyFactories.set(ConstDependency, new NullFactory());
			compilation.dependencyTemplates.set(ConstDependency, new ConstDependency.Template());
			params.normalModuleFactory.plugin("parser", (parser, parserOptions) => {
				Object.keys(definitions).forEach(name => {
					var request = [].concat(definitions[name]);
					var splittedName = name.split(".");
					if(splittedName.length > 0) {
						splittedName.slice(1).forEach((_, i) => {
							const name = splittedName.slice(0, i + 1).join(".");
							parser.plugin('can-rename ${name}', ParserHelpers.approve);
						});
					}
					parser.plugin('expression ${name}', function(expr) {
						let nameIdentifier = name;
						const scopedName = name.indexOf(".") >= 0;
						let expression = 'require(${JSON.stringify(request[0])})';
						if(scopedName) {
							nameIdentifier = '__webpack_provided_${name.replace(/\./g, "_dot_")}';
						}
						if(request.length > 1) {
							expression += request.slice(1).map(r => '[${JSON.stringify(r)}]').join("");
						}
						if(!ParserHelpers.addParsedVariableToModule(this, nameIdentifier, expression)) {
							return false;
						}
						if(scopedName) {
							ParserHelpers.toConstantDependency(nameIdentifier).bind(this)(expr);
						}
						return true;
					});
				});
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.SetVarMainTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>SetVarMainTemplatePlugin (varExpression, copyObject)](#apidoc.element.webpack.SetVarMainTemplatePlugin)
- description and source-code
```javascript
class SetVarMainTemplatePlugin {
	constructor(varExpression, copyObject) {
		this.varExpression = varExpression;
		this.copyObject = copyObject;
	}

	apply(compilation) {
		const mainTemplate = compilation.mainTemplate;
		compilation.templatesPlugin("render-with-entry", (source, chunk, hash) => {
			const varExpression = mainTemplate.applyPluginsWaterfall("asset-path", this.varExpression, {
				hash,
				chunk
			});
			if(this.copyObject) {
				return new ConcatSource('(function(e, a) { for(var i in a) e[i] = a[i]; }(${varExpression}, ', source, "))");
			} else {
				const prefix = '${varExpression} =\n';
				return new ConcatSource(prefix, source);
			}
		});
		mainTemplate.plugin("global-hash-paths", function(paths) {
			if(this.varExpression) paths.push(this.varExpression);
			return paths;
		});
		mainTemplate.plugin("hash", hash => {
			hash.update("set var");
			hash.update('${this.varExpression}');
			hash.update('${this.copyObject}');
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.SourceMapDevToolPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>SourceMapDevToolPlugin (options)](#apidoc.element.webpack.SourceMapDevToolPlugin)
- description and source-code
```javascript
function SourceMapDevToolPlugin(options) {
	if(arguments.length > 1)
		throw new Error("SourceMapDevToolPlugin only takes one argument (pass an options object)");
	if(typeof options === "string") {
		options = {
			sourceMapFilename: options
		};
	}
	if(!options) options = {};
	this.sourceMapFilename = options.filename;
	this.sourceMappingURLComment = options.append === false ? false : options.append || "\n//# sourceMappingURL=[url]";
	this.moduleFilenameTemplate = options.moduleFilenameTemplate || "webpack:///[resourcePath]";
	this.fallbackModuleFilenameTemplate = options.fallbackModuleFilenameTemplate || "webpack:///[resourcePath]?[hash]";
	this.options = options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.UmdMainTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>UmdMainTemplatePlugin (name, options)](#apidoc.element.webpack.UmdMainTemplatePlugin)
- description and source-code
```javascript
class UmdMainTemplatePlugin {
	constructor(name, options) {
		this.name = name;
		this.optionalAmdExternalAsGlobal = options.optionalAmdExternalAsGlobal;
		this.namedDefine = options.namedDefine;
		this.auxiliaryComment = options.auxiliaryComment;
	}

	apply(compilation) {
		const mainTemplate = compilation.mainTemplate;
		compilation.templatesPlugin("render-with-entry", function(source, chunk, hash) {
			let externals = chunk.modules.filter(m => m.external);
			const optionalExternals = [];
			let requiredExternals = [];
			if(this.optionalAmdExternalAsGlobal) {
				externals.forEach(m => {
					if(m.optional) {
						optionalExternals.push(m);
					} else {
						requiredExternals.push(m);
					}
				});
				externals = requiredExternals.concat(optionalExternals);
			} else {
				requiredExternals = externals;
			}

			function replaceKeys(str) {
				return mainTemplate.applyPluginsWaterfall("asset-path", str, {
					hash,
					chunk
				});
			}

			function externalsDepsArray(modules) {
				return '[${replaceKeys(modules.map(m => JSON.stringify(typeof m.request === "object" ? m.request.amd : m.request)).join(", "))}]';
			}

			function externalsRootArray(modules) {
				return replaceKeys(modules.map(m => {
					let request = m.request;
					if(typeof request === "object") request = request.root;
					return 'root${accessorToObjectAccess([].concat(request))}';
				}).join(", "));
			}

			function externalsRequireArray(type) {
				return replaceKeys(externals.map(m => {
					let expr;
					let request = m.request;
					if(typeof request === "object") request = request[type];
					if(Array.isArray(request)) {
						expr = 'require(${JSON.stringify(request[0])})${accessorToObjectAccess(request.slice(1))}';
					} else
						expr = 'require(${JSON.stringify(request)})';
					if(m.optional) {
						expr = '(function webpackLoadOptionalExternalModule() { try { return ${expr}; } catch(e) {} }())';
					}
					return expr;
				}).join(", "));
			}

			function externalsArguments(modules) {
				return modules.map(m => Template.toIdentifier('__WEBPACK_EXTERNAL_MODULE_${m.id}__')).join(", ");
			}

			function libraryName(library) {
				return JSON.stringify(replaceKeys([].concat(library).pop()));
			}

			let amdFactory;
			if(optionalExternals.length > 0) {
				const wrapperArguments = externalsArguments(requiredExternals);
				const factoryArguments = requiredExternals.length > 0 ?
					externalsArguments(requiredExternals) + ", " + externalsRootArray(optionalExternals) :
					externalsRootArray(optionalExternals);
				amdFactory = 'function webpackLoadOptionalExternalModuleAmd(${wrapperArguments}) {\n' +
					'			return factory(${factoryArguments});\n' +
					"		}";
			} else {
				amdFactory = "factory";
			}

			return new ConcatSource(new OriginalSource(
				"(function webpackUniversalModuleDefinition(root, factory) {\n" +
				(this.auxiliaryComment &&
					typeof this.auxiliaryComment === "string" ?
					"   //" + this.auxiliaryComment + "\n" :
					this.auxiliaryComment.commonjs2 ?
					"   //" + this.auxiliaryComment.commonjs2 + "\n" :
					""
				) +
				"	if(typeof exports === 'object' && typeof module === 'object')\n" +
				"		module.exports = factory(" + externalsRequireArray("commonjs2") + ");\n" +
				(this.auxiliaryComment &&
					typeof this.auxiliaryComment === "string" ?
					"   //" + this.auxiliaryComment + "\n" :
					this.auxiliaryComment.amd ?
					"   //" + this.auxiliaryComment.amd + "\n" :
					""
				) +
				"	else if(typeof define === 'function' && define.amd)\n" +
				(requiredExternals.length > 0 ?
					(this.name && this.namedDefine === true ?
						"		define(" + libraryName(this.name) + ", " + externalsDepsArray(requiredExternals) + ", " + amdFactory + ");\n" :
						"		define(" + externalsDepsArray(requiredExternals) + ", " + amdFactory + ");\n"
					) :
					(this.name && this.namedDefine === true ?
						"		define(" + libraryName(this.name) + ", [], " + amdFactory + ");\n" :
						" ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.WatchIgnorePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>WatchIgnorePlugin (paths)](#apidoc.element.webpack.WatchIgnorePlugin)
- description and source-code
```javascript
class WatchIgnorePlugin {
	constructor(paths) {
		this.paths = paths;
	}

	apply(compiler) {
		compiler.plugin("after-environment", () => {
			compiler.watchFileSystem = new IgnoringWatchFileSystem(compiler.watchFileSystem, this.paths);
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.WebpackOptionsApply"></a>[function <span class="apidocSignatureSpan">webpack.</span>WebpackOptionsApply ()](#apidoc.element.webpack.WebpackOptionsApply)
- description and source-code
```javascript
class WebpackOptionsApply extends OptionsApply {
	constructor() {
		super();
	}

	process(options, compiler) {
		let ExternalsPlugin;
		compiler.outputPath = options.output.path;
		compiler.recordsInputPath = options.recordsInputPath || options.recordsPath;
		compiler.recordsOutputPath = options.recordsOutputPath || options.recordsPath;
		compiler.name = options.name;
		compiler.dependencies = options.dependencies;
		if(typeof options.target === "string") {
			let JsonpTemplatePlugin;
			let NodeSourcePlugin;
			let NodeTargetPlugin;
			let NodeTemplatePlugin;

			switch(options.target) {
				case "web":
					JsonpTemplatePlugin = require("./JsonpTemplatePlugin");
					NodeSourcePlugin = require("./node/NodeSourcePlugin");
					compiler.apply(
						new JsonpTemplatePlugin(options.output),
						new FunctionModulePlugin(options.output),
						new NodeSourcePlugin(options.node),
						new LoaderTargetPlugin("web")
					);
					break;
				case "webworker":
					{
						let WebWorkerTemplatePlugin = require("./webworker/WebWorkerTemplatePlugin");
						NodeSourcePlugin = require("./node/NodeSourcePlugin");
						compiler.apply(
							new WebWorkerTemplatePlugin(options.output),
							new FunctionModulePlugin(options.output),
							new NodeSourcePlugin(options.node),
							new LoaderTargetPlugin("webworker")
						);
						break;
					}
				case "node":
				case "async-node":
					NodeTemplatePlugin = require("./node/NodeTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					compiler.apply(
						new NodeTemplatePlugin({
							asyncChunkLoading: options.target === "async-node"
						}),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new LoaderTargetPlugin("node")
					);
					break;
				case "node-webkit":
					JsonpTemplatePlugin = require("./JsonpTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					ExternalsPlugin = require("./ExternalsPlugin");
					compiler.apply(
						new JsonpTemplatePlugin(options.output),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new ExternalsPlugin("commonjs", "nw.gui"),
						new LoaderTargetPlugin("node-webkit")
					);
					break;
				case "atom":
				case "electron":
				case "electron-main":
					NodeTemplatePlugin = require("./node/NodeTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					ExternalsPlugin = require("./ExternalsPlugin");
					compiler.apply(
						new NodeTemplatePlugin({
							asyncChunkLoading: true
						}),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new ExternalsPlugin("commonjs", [
							"app",
							"auto-updater",
							"browser-window",
							"content-tracing",
							"dialog",
							"electron",
							"global-shortcut",
							"ipc",
							"ipc-main",
							"menu",
							"menu-item",
							"power-monitor",
							"power-save-blocker",
							"protocol",
							"session",
							"web-contents",
							"tray",
							"clipboard",
							"crash-reporter",
							"native-image",
							"screen",
							"shell"
						]),
						new LoaderTargetPlugin(options.target)
					);
					break;
				case "electron-renderer":
					JsonpTemplatePlugin = require("./JsonpTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					ExternalsPlugin = require("./ExternalsPlugin");
					compiler.apply(
						new JsonpTemplatePlugin(options.output),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new ExternalsPlugin("commonjs", [
							"desktop-capturer",
							"electron",
							"ipc",
							"ipc-renderer",
							"remote",
							"web-frame",
							"clipboard",
							"crash-reporter",
							"native-image",
							"screen",
							"shell"
						]),
						new LoaderTargetPlugin(options.target)
					);
					break;
				default:
					throw new Error("Unsupported target '" + options.target ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.WebpackOptionsDefaulter"></a>[function <span class="apidocSignatureSpan">webpack.</span>WebpackOptionsDefaulter ()](#apidoc.element.webpack.WebpackOptionsDefaulter)
- description and source-code
```javascript
class WebpackOptionsDefaulter extends OptionsDefaulter {
	constructor() {
		super();
		this.set("devtool", false);
		this.set("cache", true);

		this.set("context", process.cwd());
		this.set("target", "web");

		this.set("module.unknownContextRequest", ".");
		this.set("module.unknownContextRegExp", false);
		this.set("module.unknownContextRecursive", true);
		this.set("module.unknownContextCritical", true);
		this.set("module.exprContextRequest", ".");
		this.set("module.exprContextRegExp", false);
		this.set("module.exprContextRecursive", true);
		this.set("module.exprContextCritical", true);
		this.set("module.wrappedContextRegExp", /.*/);
		this.set("module.wrappedContextRecursive", true);
		this.set("module.wrappedContextCritical", false);
		this.set("module.strictExportPresence", false);

		this.set("module.unsafeCache", true);

		this.set("output", "call", (value, options) => {
			if(typeof value === "string") {
				return {
					filename: value
				};
			} else if(typeof value !== "object") {
				return {};
			} else {
				return value;
			}
		});
		this.set("output.filename", "[name].js");
		this.set("output.chunkFilename", "make", (options) => {
			const filename = options.output.filename;
			return filename.indexOf("[name]") >= 0 ? filename.replace("[name]", "[id]") : "[id]." + filename;
		});
		this.set("output.library", "");
		this.set("output.hotUpdateFunction", "make", (options) => {
			return Template.toIdentifier("webpackHotUpdate" + options.output.library);
		});
		this.set("output.jsonpFunction", "make", (options) => {
			return Template.toIdentifier("webpackJsonp" + options.output.library);
		});
		this.set("output.libraryTarget", "var");
		this.set("output.path", process.cwd());
		this.set("output.sourceMapFilename", "[file].map[query]");
		this.set("output.hotUpdateChunkFilename", "[id].[hash].hot-update.js");
		this.set("output.hotUpdateMainFilename", "[hash].hot-update.json");
		this.set("output.crossOriginLoading", false);
		this.set("output.hashFunction", "md5");
		this.set("output.hashDigest", "hex");
		this.set("output.hashDigestLength", 20);
		this.set("output.devtoolLineToLine", false);
		this.set("output.strictModuleExceptionHandling", false);

		this.set("node", {});
		this.set("node.console", false);
		this.set("node.process", true);
		this.set("node.global", true);
		this.set("node.Buffer", true);
		this.set("node.setImmediate", true);
		this.set("node.__filename", "mock");
		this.set("node.__dirname", "mock");

		this.set("performance.maxAssetSize", 250000);
		this.set("performance.maxEntrypointSize", 250000);
		this.set("performance.hints", false);

		this.set("resolve", {});
		this.set("resolve.unsafeCache", true);
		this.set("resolve.modules", ["node_modules"]);
		this.set("resolve.extensions", [".js", ".json"]);
		this.set("resolve.aliasFields", "make", (options) => {
			if(options.target === "web" || options.target === "webworker")
				return ["browser"];
			else
				return [];
		});
		this.set("resolve.mainFields", "make", (options) => {
			if(options.target === "web" || options.target === "webworker")
				return ["browser", "module", "main"];
			else
				return ["module", "main"];
		});
		this.set("resolveLoader", {});
		this.set("resolveLoader.unsafeCache", true);
		this.set("resolveLoader.mainFields", ["loader", "main"]);
		this.set("resolveLoader.extensions", [".js", ".json"]);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.WebpackOptionsValidationError"></a>[function <span class="apidocSignatureSpan">webpack.</span>WebpackOptionsValidationError (validationErrors)](#apidoc.element.webpack.WebpackOptionsValidationError)
- description and source-code
```javascript
class WebpackOptionsValidationError extends Error {

	constructor(validationErrors) {
		super();

		this.name = "WebpackOptionsValidationError";

		this.message = "Invalid configuration object. " +
			"Webpack has been initialised using a configuration object that does not match the API schema.\n" +
			validationErrors.map(err => " - " + indent(WebpackOptionsValidationError.formatValidationError(err), "   ", false)).join("\n");
		this.validationErrors = validationErrors;

		Error.captureStackTrace(this, this.constructor);
	}

	static formatSchema(schema, prevSchemas) {
		prevSchemas = prevSchemas || [];

		const formatInnerSchema = (innerSchema, addSelf) => {
			if(!addSelf) return WebpackOptionsValidationError.formatSchema(innerSchema, prevSchemas);
			if(prevSchemas.indexOf(innerSchema) >= 0) return "(recursive)";
			return WebpackOptionsValidationError.formatSchema(innerSchema, prevSchemas.concat(schema));
		};

		if(schema.type === "string") {
			if(schema.minLength === 1)
				return "non-empty string";
			else if(schema.minLength > 1)
				return 'string (min length ${schema.minLength})';
			return "string";
		} else if(schema.type === "boolean") {
			return "boolean";
		} else if(schema.type === "number") {
			return "number";
		} else if(schema.type === "object") {
			if(schema.properties) {
				const required = schema.required || [];
				return 'object { ${Object.keys(schema.properties).map(property => {
					if(required.indexOf(property) < 0) return property + "?";
					return property;
				}).concat(schema.additionalProperties ? ["..."] : []).join(", ")} }';
			}
			if(schema.additionalProperties) {
				return 'object { <key>: ${formatInnerSchema(schema.additionalProperties)} }';
			}
			return "object";
		} else if(schema.type === "array") {
			return '[${formatInnerSchema(schema.items)}]';
		}

		switch(schema.instanceof) {
			case "Function":
				return "function";
			case "RegExp":
				return "RegExp";
		}
		if(schema.$ref) return formatInnerSchema(getSchemaPart(schema.$ref), true);
		if(schema.allOf) return schema.allOf.map(formatInnerSchema).join(" & ");
		if(schema.oneOf) return schema.oneOf.map(formatInnerSchema).join(" | ");
		if(schema.anyOf) return schema.anyOf.map(formatInnerSchema).join(" | ");
		if(schema.enum) return schema.enum.map(item => JSON.stringify(item)).join(" | ");
		return JSON.stringify(schema, 0, 2);
	}

	static formatValidationError(err) {
		const dataPath = 'configuration${err.dataPath}';
		if(err.keyword === "additionalProperties") {
			const baseMessage = '${dataPath} has an unknown property '${err.params.additionalProperty}'. These properties are valid:\n${getSchemaPartText
(err.parentSchema)}';
			if(!err.dataPath) {
				switch(err.params.additionalProperty) {
					case "debug":
						return '${baseMessage}\n' +
							"The 'debug' property was removed in webpack 2.\n" +
							"Loaders should be updated to allow passing this option via loader options in module.rules.\n" +
							"Until loaders are updated one can use the LoaderOptionsPlugin to switch loaders into debug mode:\n" +
							"plugins: [\n" +
							"  new webpack.LoaderOptionsPlugin({\n" +
							"    debug: true\n" +
							"  })\n" +
							"]";
				}
				return baseMessage + "\n" +
					"For typos: please correct them.\n" +
					"For loader options: webpack 2 no longer allows custom properties in configuration.\n" +
					"  Loaders should be updated to allow passing options via loader options in module.rules.\n" +
					"  Until loaders are updated one can use the LoaderOptionsPlugin to pass these options to the loader:\n" +
					"  plugins: [\n" +
					"    new webpack.LoaderOptionsPlugin({\n" +
					"      // test: /\\.xxx$/, // may apply this only for some modules\n" +
					"      options: {\n" +
					'        ${err.params.additionalProperty}: ...\n' +
					"      }\n" +
					"    })\n" +
					"  ]";
			}
			return baseMessage;
		} else if(err.keyword === "oneOf" || err.keyword === "anyOf") {
			if(err.children && err ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.validate"></a>[function <span class="apidocSignatureSpan">webpack.</span>validate ()](#apidoc.element.webpack.validate)
- description and source-code
```javascript
validate = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.validateSchema"></a>[function <span class="apidocSignatureSpan">webpack.</span>validateSchema (schema, options)](#apidoc.element.webpack.validateSchema)
- description and source-code
```javascript
function validateSchema(schema, options) {
	if(Array.isArray(options)) {
		const errors = options.map((options) => validateObject(schema, options));
		errors.forEach((list, idx) => {
			list.forEach(function applyPrefix(err) {
				err.dataPath = '[${idx}]${err.dataPath}';
				if(err.children) {
					err.children.forEach(applyPrefix);
				}
			});
		});
		return errors.reduce((arr, items) => {
			return arr.concat(items);
		}, []);
	} else {
		return validateObject(schema, options);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.webpack_web"></a>[function <span class="apidocSignatureSpan">webpack.</span>webpack_web (options, callback)](#apidoc.element.webpack.webpack_web)
- description and source-code
```javascript
function webpack(options, callback) {
	new WebpackOptionsDefaulter().process(options);

	const compiler = new Compiler();
	compiler.options = options;
	compiler.options = new WebpackOptionsApply().process(options, compiler);
	new WebEnvironmentPlugin(options.inputFileSystem, options.outputFileSystem).apply(compiler);
	if(callback) {
		compiler.run(callback);
	}
	return compiler;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.Compiler"></a>[module webpack.Compiler](#apidoc.module.webpack.Compiler)

#### <a name="apidoc.element.webpack.Compiler.Compiler"></a>[function <span class="apidocSignatureSpan">webpack.</span>Compiler ()](#apidoc.element.webpack.Compiler.Compiler)
- description and source-code
```javascript
function Compiler() {
	Tapable.call(this);

	this.outputPath = "";
	this.outputFileSystem = null;
	this.inputFileSystem = null;

	this.recordsInputPath = null;
	this.recordsOutputPath = null;
	this.records = {};

	this.fileTimestamps = {};
	this.contextTimestamps = {};

	this.resolvers = {
		normal: null,
		loader: null,
		context: null
	};
	var deprecationReported = false;
	this.parser = {
		plugin: function(hook, fn) {
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.plugin(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.plugin(hook, fn);
				});
			});
		}.bind(this),
		apply: function() {
			var args = arguments;
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.apply(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.apply.apply(parser, args);
				});
			});
		}.bind(this)
	};

	this.options = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.Watching"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.</span>Watching (compiler, watchOptions, handler)](#apidoc.element.webpack.Compiler.Watching)
- description and source-code
```javascript
function Watching(compiler, watchOptions, handler) {
	this.startTime = null;
	this.invalid = false;
	this.error = null;
	this.stats = null;
	this.handler = handler;
	this.closed = false;
	if(typeof watchOptions === "number") {
		this.watchOptions = {
			aggregateTimeout: watchOptions
		};
	} else if(watchOptions && typeof watchOptions === "object") {
		this.watchOptions = Object.assign({}, watchOptions);
	} else {
		this.watchOptions = {};
	}
	this.watchOptions.aggregateTimeout = this.watchOptions.aggregateTimeout || 200;
	this.compiler = compiler;
	this.running = true;
	this.compiler.readRecords(function(err) {
		if(err) return this._done(err);

		this._go();
	}.bind(this));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.Compiler.Watching"></a>[module webpack.Compiler.Watching](#apidoc.module.webpack.Compiler.Watching)

#### <a name="apidoc.element.webpack.Compiler.Watching.Watching"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.</span>Watching (compiler, watchOptions, handler)](#apidoc.element.webpack.Compiler.Watching.Watching)
- description and source-code
```javascript
function Watching(compiler, watchOptions, handler) {
	this.startTime = null;
	this.invalid = false;
	this.error = null;
	this.stats = null;
	this.handler = handler;
	this.closed = false;
	if(typeof watchOptions === "number") {
		this.watchOptions = {
			aggregateTimeout: watchOptions
		};
	} else if(watchOptions && typeof watchOptions === "object") {
		this.watchOptions = Object.assign({}, watchOptions);
	} else {
		this.watchOptions = {};
	}
	this.watchOptions.aggregateTimeout = this.watchOptions.aggregateTimeout || 200;
	this.compiler = compiler;
	this.running = true;
	this.compiler.readRecords(function(err) {
		if(err) return this._done(err);

		this._go();
	}.bind(this));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.Compiler.Watching.prototype"></a>[module webpack.Compiler.Watching.prototype](#apidoc.module.webpack.Compiler.Watching.prototype)

#### <a name="apidoc.element.webpack.Compiler.Watching.prototype._done"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>_done (err, compilation)](#apidoc.element.webpack.Compiler.Watching.prototype._done)
- description and source-code
```javascript
_done = function (err, compilation) {
	this.running = false;
	if(this.invalid) return this._go();
	this.error = err || null;
	this.stats = compilation ? compilation.getStats() : null;
	if(this.stats) {
		this.stats.startTime = this.startTime;
		this.stats.endTime = new Date().getTime();
	}
	if(this.stats)
		this.compiler.applyPlugins("done", this.stats);
	else
		this.compiler.applyPlugins("failed", this.error);
	this.handler(this.error, this.stats);
	if(!this.error && !this.closed)
		this.watch(compilation.fileDependencies, compilation.contextDependencies, compilation.missingDependencies);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.Watching.prototype._go"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>_go ()](#apidoc.element.webpack.Compiler.Watching.prototype._go)
- description and source-code
```javascript
_go = function () {
	var self = this;
	self.startTime = new Date().getTime();
	self.running = true;
	self.invalid = false;
	self.compiler.applyPluginsAsync("watch-run", self, function(err) {
		if(err) return self._done(err);
		self.compiler.compile(function onCompiled(err, compilation) {
			if(err) return self._done(err);
			if(self.invalid) return self._done();

			if(self.compiler.applyPluginsBailResult("should-emit", compilation) === false) {
				return self._done(null, compilation);
			}

			self.compiler.emitAssets(compilation, function(err) {
				if(err) return self._done(err);
				if(self.invalid) return self._done();

				self.compiler.emitRecords(function(err) {
					if(err) return self._done(err);

					if(compilation.applyPluginsBailResult("need-additional-pass")) {
						compilation.needAdditionalPass = true;

						var stats = compilation.getStats();
						stats.startTime = self.startTime;
						stats.endTime = new Date().getTime();
						self.compiler.applyPlugins("done", stats);

						self.compiler.applyPluginsAsync("additional-pass", function(err) {
							if(err) return self._done(err);
							self.compiler.compile(onCompiled);
						});
						return;
					}
					return self._done(null, compilation);
				});
			});
		});
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.Watching.prototype.close"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>close (callback)](#apidoc.element.webpack.Compiler.Watching.prototype.close)
- description and source-code
```javascript
close = function (callback) {
	if(callback === undefined) callback = function() {};

	this.closed = true;
	if(this.watcher) {
		this.watcher.close();
		this.watcher = null;
	}
	if(this.pausedWatcher) {
		this.pausedWatcher.close();
		this.pausedWatcher = null;
	}
	if(this.running) {
		this.invalid = true;
		this._done = () => {
			this.compiler.applyPlugins("watch-close");
			callback();
		};
	} else {
		this.compiler.applyPlugins("watch-close");
		callback();
	}
}
```
- example usage
```shell
...
		this.watchings.forEach((watching) => watching.invalidate());
	}

	close(callback) {
		if(callback === undefined) callback = () => { /*do nothing*/ };

		async.forEach(this.watchings, (watching, finishedCallback) => {
			watching.close(finishedCallback);
		}, err => {
			this.compiler.applyPlugins("watch-close");
			callback(err);
		});

	}
}
...
```

#### <a name="apidoc.element.webpack.Compiler.Watching.prototype.invalidate"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>invalidate ()](#apidoc.element.webpack.Compiler.Watching.prototype.invalidate)
- description and source-code
```javascript
invalidate = function () {
	if(this.watcher) {
		this.pausedWatcher = this.watcher;
		this.watcher.pause();
		this.watcher = null;
	}
	if(this.running) {
		this.invalid = true;
		return false;
	} else {
		this._go();
	}
}
```
- example usage
```shell
...
class MultiWatching {
	constructor(watchings, compiler) {
		this.watchings = watchings;
		this.compiler = compiler;
	}

	invalidate() {
		this.watchings.forEach((watching) => watching.invalidate());
	}

	close(callback) {
		if(callback === undefined) callback = () => { /*do nothing*/ };

		async.forEach(this.watchings, (watching, finishedCallback) => {
			watching.close(finishedCallback);
...
```

#### <a name="apidoc.element.webpack.Compiler.Watching.prototype.watch"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.Watching.prototype.</span>watch (files, dirs, missing)](#apidoc.element.webpack.Compiler.Watching.prototype.watch)
- description and source-code
```javascript
watch = function (files, dirs, missing) {
	this.pausedWatcher = null;
	this.watcher = this.compiler.watchFileSystem.watch(files, dirs, missing, this.startTime, this.watchOptions, function(err, filesModified
, contextModified, missingModified, fileTimestamps, contextTimestamps) {
		this.pausedWatcher = this.watcher;
		this.watcher = null;
		if(err) return this.handler(err);

		this.compiler.fileTimestamps = fileTimestamps;
		this.compiler.contextTimestamps = contextTimestamps;
		this.invalidate();
	}.bind(this), function(fileName, changeTime) {
		this.compiler.applyPlugins("invalid", fileName, changeTime);
	}.bind(this));
}
```
- example usage
```shell
...
		const ignored = path => this.paths.some(p => p instanceof RegExp ? p.test(path) : path.indexOf(p) === 0);

		const notIgnored = path => !ignored(path);

		const ignoredFiles = files.filter(ignored);
		const ignoredDirs = dirs.filter(ignored);

		this.wfs.watch(files.filter(notIgnored), dirs.filter(notIgnored), missing, startTime, options, (err, filesModified, dirsModified
, missingModified, fileTimestamps, dirTimestamps) => {
			if(err) return callback(err);

			ignoredFiles.forEach(path => {
				fileTimestamps[path] = 1;
			});

			ignoredDirs.forEach(path => {
...
```



# <a name="apidoc.module.webpack.Compiler.prototype"></a>[module webpack.Compiler.prototype](#apidoc.module.webpack.Compiler.prototype)

#### <a name="apidoc.element.webpack.Compiler.prototype.compile"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>compile (callback)](#apidoc.element.webpack.Compiler.prototype.compile)
- description and source-code
```javascript
compile = function (callback) {
	var self = this;
	var params = self.newCompilationParams();
	self.applyPluginsAsync("before-compile", params, function(err) {
		if(err) return callback(err);

		self.applyPlugins("compile", params);

		var compilation = self.newCompilation(params);

		self.applyPluginsParallel("make", compilation, function(err) {
			if(err) return callback(err);

			compilation.finish();

			compilation.seal(function(err) {
				if(err) return callback(err);

				self.applyPluginsAsync("after-compile", compilation, function(err) {
					if(err) return callback(err);

					return callback(null, compilation);
				});
			});
		});
	});
}
```
- example usage
```shell
...
		}, []);
	} else {
		return validateObject(schema, options);
	}
}

function validateObject(schema, options) {
	const validate = ajv.compile(schema);
	const valid = validate(options);
	return valid ? [] : filterErrors(validate.errors);
}

function filterErrors(errors) {
	let newErrors = [];
	errors.forEach((err) => {
...
```

#### <a name="apidoc.element.webpack.Compiler.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>constructor ()](#apidoc.element.webpack.Compiler.prototype.constructor)
- description and source-code
```javascript
function Compiler() {
	Tapable.call(this);

	this.outputPath = "";
	this.outputFileSystem = null;
	this.inputFileSystem = null;

	this.recordsInputPath = null;
	this.recordsOutputPath = null;
	this.records = {};

	this.fileTimestamps = {};
	this.contextTimestamps = {};

	this.resolvers = {
		normal: null,
		loader: null,
		context: null
	};
	var deprecationReported = false;
	this.parser = {
		plugin: function(hook, fn) {
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.plugin(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.plugin(hook, fn);
				});
			});
		}.bind(this),
		apply: function() {
			var args = arguments;
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.apply(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.apply.apply(parser, args);
				});
			});
		}.bind(this)
	};

	this.options = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.createChildCompiler"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createChildCompiler (compilation, compilerName, outputOptions, plugins)](#apidoc.element.webpack.Compiler.prototype.createChildCompiler)
- description and source-code
```javascript
createChildCompiler = function (compilation, compilerName, outputOptions, plugins) {
	var childCompiler = new Compiler();
	if(Array.isArray(plugins)) {
		plugins.forEach(plugin => childCompiler.apply(plugin));
	}
	for(var name in this._plugins) {
		if(["make", "compile", "emit", "after-emit", "invalid", "done", "this-compilation"].indexOf(name) < 0)
			childCompiler._plugins[name] = this._plugins[name].slice();
	}
	childCompiler.name = compilerName;
	childCompiler.outputPath = this.outputPath;
	childCompiler.inputFileSystem = this.inputFileSystem;
	childCompiler.outputFileSystem = null;
	childCompiler.resolvers = this.resolvers;
	childCompiler.fileTimestamps = this.fileTimestamps;
	childCompiler.contextTimestamps = this.contextTimestamps;
	if(!this.records[compilerName]) this.records[compilerName] = [];
	this.records[compilerName].push(childCompiler.records = {});
	childCompiler.options = Object.create(this.options);
	childCompiler.options.output = Object.create(childCompiler.options.output);
	for(name in outputOptions) {
		childCompiler.options.output[name] = outputOptions[name];
	}
	childCompiler.parentCompilation = compilation;
	return childCompiler;
}
```
- example usage
```shell
...
	}

	getStats() {
		return new Stats(this);
	}

	createChildCompiler(name, outputOptions) {
		return this.compiler.createChildCompiler(this, name, outputOptions);
	}

	checkConstraints() {
		const usedIds = {};

		const modules = this.modules;
		for(let indexModule = 0; indexModule < modules.length; indexModule++) {
...
```

#### <a name="apidoc.element.webpack.Compiler.prototype.createCompilation"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createCompilation ()](#apidoc.element.webpack.Compiler.prototype.createCompilation)
- description and source-code
```javascript
createCompilation = function () {
	return new Compilation(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.createContextModuleFactory"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createContextModuleFactory ()](#apidoc.element.webpack.Compiler.prototype.createContextModuleFactory)
- description and source-code
```javascript
createContextModuleFactory = function () {
	var contextModuleFactory = new ContextModuleFactory(this.resolvers, this.inputFileSystem);
	this.applyPlugins("context-module-factory", contextModuleFactory);
	return contextModuleFactory;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.createNormalModuleFactory"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>createNormalModuleFactory ()](#apidoc.element.webpack.Compiler.prototype.createNormalModuleFactory)
- description and source-code
```javascript
createNormalModuleFactory = function () {
	var normalModuleFactory = new NormalModuleFactory(this.options.context, this.resolvers, this.options.module || {});
	this.applyPlugins("normal-module-factory", normalModuleFactory);
	return normalModuleFactory;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.emitAssets"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>emitAssets (compilation, callback)](#apidoc.element.webpack.Compiler.prototype.emitAssets)
- description and source-code
```javascript
emitAssets = function (compilation, callback) {
	var outputPath;

	this.applyPluginsAsync("emit", compilation, function(err) {
		if(err) return callback(err);
		outputPath = compilation.getPath(this.outputPath);
		this.outputFileSystem.mkdirp(outputPath, emitFiles.bind(this));
	}.bind(this));

	function emitFiles(err) {
		if(err) return callback(err);

		require("async").forEach(Object.keys(compilation.assets), function(file, callback) {

			var targetFile = file;
			var queryStringIdx = targetFile.indexOf("?");
			if(queryStringIdx >= 0) {
				targetFile = targetFile.substr(0, queryStringIdx);
			}

			if(targetFile.match(/\/|\\/)) {
				var dir = path.dirname(targetFile);
				this.outputFileSystem.mkdirp(this.outputFileSystem.join(outputPath, dir), writeOut.bind(this));
			} else writeOut.call(this);

			function writeOut(err) {
				if(err) return callback(err);
				var targetPath = this.outputFileSystem.join(outputPath, targetFile);
				var source = compilation.assets[file];
				if(source.existsAt === targetPath) {
					source.emitted = false;
					return callback();
				}
				var content = source.source();

				if(!Buffer.isBuffer(content)) {
					content = new Buffer(content, "utf8"); //eslint-disable-line
				}

				source.existsAt = targetPath;
				source.emitted = true;
				this.outputFileSystem.writeFile(targetPath, content, callback);
			}

		}.bind(this), function(err) {
			if(err) return callback(err);

			afterEmit.call(this);
		}.bind(this));
	}

	function afterEmit() {
		this.applyPluginsAsyncSeries1("after-emit", compilation, function(err) {
			if(err) return callback(err);

			return callback();
		});
	}

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.emitRecords"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>emitRecords (callback)](#apidoc.element.webpack.Compiler.prototype.emitRecords)
- description and source-code
```javascript
function emitRecords(callback) {
	if(!this.recordsOutputPath) return callback();
	var idx1 = this.recordsOutputPath.lastIndexOf("/");
	var idx2 = this.recordsOutputPath.lastIndexOf("\\");
	var recordsOutputPathDirectory = null;
	if(idx1 > idx2) recordsOutputPathDirectory = this.recordsOutputPath.substr(0, idx1);
	if(idx1 < idx2) recordsOutputPathDirectory = this.recordsOutputPath.substr(0, idx2);
	if(!recordsOutputPathDirectory) return writeFile.call(this);
	this.outputFileSystem.mkdirp(recordsOutputPathDirectory, function(err) {
		if(err) return callback(err);
		writeFile.call(this);
	}.bind(this));

	function writeFile() {
		this.outputFileSystem.writeFile(this.recordsOutputPath, JSON.stringify(this.records, undefined, 2), callback);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.isChild"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>isChild ()](#apidoc.element.webpack.Compiler.prototype.isChild)
- description and source-code
```javascript
isChild = function () {
	return !!this.parentCompilation;
}
```
- example usage
```shell
...
				if(ident) {
					const idx = activeModules.indexOf(ident);
					if(idx >= 0) activeModules.splice(idx, 1);
				}
				update();
			};
			compiler.plugin("compilation", function(compilation) {
				if(compilation.compiler.isChild()) return;
				lastModulesCount = moduleCount;
				moduleCount = 0;
				doneModules = 0;
				handler(0, "compiling");
				compilation.plugin("build-module", function(module) {
					moduleCount++;
					const ident = module.identifier();
...
```

#### <a name="apidoc.element.webpack.Compiler.prototype.newCompilation"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>newCompilation (params)](#apidoc.element.webpack.Compiler.prototype.newCompilation)
- description and source-code
```javascript
newCompilation = function (params) {
	var compilation = this.createCompilation();
	compilation.fileTimestamps = this.fileTimestamps;
	compilation.contextTimestamps = this.contextTimestamps;
	compilation.name = this.name;
	compilation.records = this.records;
	compilation.compilationDependencies = params.compilationDependencies;
	this.applyPlugins("this-compilation", compilation, params);
	this.applyPlugins("compilation", compilation, params);
	return compilation;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.newCompilationParams"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>newCompilationParams ()](#apidoc.element.webpack.Compiler.prototype.newCompilationParams)
- description and source-code
```javascript
newCompilationParams = function () {
	var params = {
		normalModuleFactory: this.createNormalModuleFactory(),
		contextModuleFactory: this.createContextModuleFactory(),
		compilationDependencies: []
	};
	return params;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.purgeInputFileSystem"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>purgeInputFileSystem ()](#apidoc.element.webpack.Compiler.prototype.purgeInputFileSystem)
- description and source-code
```javascript
purgeInputFileSystem = function () {
	if(this.inputFileSystem && this.inputFileSystem.purge)
		this.inputFileSystem.purge();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.readRecords"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>readRecords (callback)](#apidoc.element.webpack.Compiler.prototype.readRecords)
- description and source-code
```javascript
function readRecords(callback) {
	var self = this;
	if(!self.recordsInputPath) {
		self.records = {};
		return callback();
	}
	self.inputFileSystem.stat(self.recordsInputPath, function(err) {
		// It doesn't exist
		// We can ignore self.
		if(err) return callback();

		self.inputFileSystem.readFile(self.recordsInputPath, function(err, content) {
			if(err) return callback(err);

			try {
				self.records = JSON.parse(content);
			} catch(e) {
				e.message = "Cannot parse records: " + e.message;
				return callback(e);
			}

			return callback();
		});
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.run"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>run (callback)](#apidoc.element.webpack.Compiler.prototype.run)
- description and source-code
```javascript
run = function (callback) {
	var self = this;
	var startTime = new Date().getTime();

	self.applyPluginsAsync("before-run", self, function(err) {
		if(err) return callback(err);

		self.applyPluginsAsync("run", self, function(err) {
			if(err) return callback(err);

			self.readRecords(function(err) {
				if(err) return callback(err);

				self.compile(function onCompiled(err, compilation) {
					if(err) return callback(err);

					if(self.applyPluginsBailResult("should-emit", compilation) === false) {
						var stats = compilation.getStats();
						stats.startTime = startTime;
						stats.endTime = new Date().getTime();
						self.applyPlugins("done", stats);
						return callback(null, stats);
					}

					self.emitAssets(compilation, function(err) {
						if(err) return callback(err);

						if(compilation.applyPluginsBailResult("need-additional-pass")) {
							compilation.needAdditionalPass = true;

							var stats = compilation.getStats();
							stats.startTime = startTime;
							stats.endTime = new Date().getTime();
							self.applyPlugins("done", stats);

							self.applyPluginsAsync("additional-pass", function(err) {
								if(err) return callback(err);
								self.compile(onCompiled);
							});
							return;
						}

						self.emitRecords(function(err) {
							if(err) return callback(err);

							var stats = compilation.getStats();
							stats.startTime = startTime;
							stats.endTime = new Date().getTime();
							self.applyPlugins("done", stats);
							return callback(null, stats);
						});
					});
				});
			});
		});
	});
}
```
- example usage
```shell
...
	new WebpackOptionsDefaulter().process(options);

	const compiler = new Compiler();
	compiler.options = options;
	compiler.options = new WebpackOptionsApply().process(options, compiler);
	new WebEnvironmentPlugin(options.inputFileSystem, options.outputFileSystem).apply(compiler);
	if(callback) {
		compiler.run(callback);
	}
	return compiler;
}
module.exports = webpack;

webpack.WebpackOptionsDefaulter = WebpackOptionsDefaulter;
webpack.WebpackOptionsApply = WebpackOptionsApply;
...
```

#### <a name="apidoc.element.webpack.Compiler.prototype.runAsChild"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>runAsChild (callback)](#apidoc.element.webpack.Compiler.prototype.runAsChild)
- description and source-code
```javascript
runAsChild = function (callback) {
	this.compile(function(err, compilation) {
		if(err) return callback(err);

		this.parentCompilation.children.push(compilation);
		Object.keys(compilation.assets).forEach(function(name) {
			this.parentCompilation.assets[name] = compilation.assets[name];
		}.bind(this));

		var entries = Object.keys(compilation.entrypoints).map(function(name) {
			return compilation.entrypoints[name].chunks;
		}).reduce(function(array, chunks) {
			return array.concat(chunks);
		}, []);

		return callback(null, entries, compilation);
	}.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Compiler.prototype.watch"></a>[function <span class="apidocSignatureSpan">webpack.Compiler.prototype.</span>watch (watchOptions, handler)](#apidoc.element.webpack.Compiler.prototype.watch)
- description and source-code
```javascript
watch = function (watchOptions, handler) {
	this.fileTimestamps = {};
	this.contextTimestamps = {};
	var watching = new Watching(this, watchOptions, handler);
	return watching;
}
```
- example usage
```shell
...
		const ignored = path => this.paths.some(p => p instanceof RegExp ? p.test(path) : path.indexOf(p) === 0);

		const notIgnored = path => !ignored(path);

		const ignoredFiles = files.filter(ignored);
		const ignoredDirs = dirs.filter(ignored);

		this.wfs.watch(files.filter(notIgnored), dirs.filter(notIgnored), missing, startTime, options, (err, filesModified, dirsModified
, missingModified, fileTimestamps, dirTimestamps) => {
			if(err) return callback(err);

			ignoredFiles.forEach(path => {
				fileTimestamps[path] = 1;
			});

			ignoredDirs.forEach(path => {
...
```



# <a name="apidoc.module.webpack.ContextModuleFactory"></a>[module webpack.ContextModuleFactory](#apidoc.module.webpack.ContextModuleFactory)

#### <a name="apidoc.element.webpack.ContextModuleFactory.ContextModuleFactory"></a>[function <span class="apidocSignatureSpan">webpack.</span>ContextModuleFactory (resolvers)](#apidoc.element.webpack.ContextModuleFactory.ContextModuleFactory)
- description and source-code
```javascript
function ContextModuleFactory(resolvers) {
	Tapable.call(this);
	this.resolvers = resolvers;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.ContextModuleFactory.prototype"></a>[module webpack.ContextModuleFactory.prototype](#apidoc.module.webpack.ContextModuleFactory.prototype)

#### <a name="apidoc.element.webpack.ContextModuleFactory.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.ContextModuleFactory.prototype.</span>constructor (resolvers)](#apidoc.element.webpack.ContextModuleFactory.prototype.constructor)
- description and source-code
```javascript
function ContextModuleFactory(resolvers) {
	Tapable.call(this);
	this.resolvers = resolvers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ContextModuleFactory.prototype.create"></a>[function <span class="apidocSignatureSpan">webpack.ContextModuleFactory.prototype.</span>create (data, callback)](#apidoc.element.webpack.ContextModuleFactory.prototype.create)
- description and source-code
```javascript
create = function (data, callback) {
	var module = this;
	var context = data.context;
	var dependencies = data.dependencies;
	var dependency = dependencies[0];
	this.applyPluginsAsyncWaterfall("before-resolve", {
		context: context,
		request: dependency.request,
		recursive: dependency.recursive,
		regExp: dependency.regExp,
		async: dependency.async,
		dependencies: dependencies
	}, function(err, result) {
		if(err) return callback(err);

		// Ignored
		if(!result) return callback();

		var context = result.context;
		var request = result.request;
		var recursive = result.recursive;
		var regExp = result.regExp;
		var asyncContext = result.async;
		var dependencies = result.dependencies;

		var loaders, resource, loadersPrefix = "";
		var idx = request.lastIndexOf("!");
		if(idx >= 0) {
			loaders = request.substr(0, idx + 1);
			for(var i = 0; i < loaders.length && loaders[i] === "!"; i++) {
				loadersPrefix += "!";
			}
			loaders = loaders.substr(i).replace(/!+$/, "").replace(/!!+/g, "!");
			if(loaders === "") loaders = [];
			else loaders = loaders.split("!");
			resource = request.substr(idx + 1);
		} else {
			loaders = [];
			resource = request;
		}

		var resolvers = module.resolvers;

		async.parallel([
			function(callback) {
				resolvers.context.resolve({}, context, resource, function(err, result) {
					if(err) return callback(err);
					callback(null, result);
				});
			},
			function(callback) {
				async.map(loaders, function(loader, callback) {
					resolvers.loader.resolve({}, context, loader, function(err, result) {
						if(err) return callback(err);
						callback(null, result);
					});
				}, callback);
			}
		], function(err, result) {
			if(err) return callback(err);

			module.applyPluginsAsyncWaterfall("after-resolve", {
				loaders: loadersPrefix + result[1].join("!") + (result[1].length > 0 ? "!" : ""),
				resource: result[0],
				recursive: recursive,
				regExp: regExp,
				async: asyncContext,
				dependencies: dependencies,
				resolveDependencies: module.resolveDependencies.bind(module)
			}, function(err, result) {
				if(err) return callback(err);

				// Ignored
				if(!result) return callback();

				return callback(null, new ContextModule(result.resolveDependencies, result.resource, result.recursive, result.regExp, result
.loaders, result.async));
			});
		});
	});
}
```
- example usage
```shell
...
			const warningAndCallback = function warningAndCallback(err) {
				err.origin = module;
				_this.warnings.push(err);
				callback();
			};

			const factory = item[0];
			factory.create({
				contextInfo: {
					issuer: module.nameForCondition && module.nameForCondition(),
					compiler: _this.compiler.name
				},
				context: module.context,
				dependencies: dependencies
			}, function factoryCallback(err, dependentModule) {
...
```

#### <a name="apidoc.element.webpack.ContextModuleFactory.prototype.resolveDependencies"></a>[function <span class="apidocSignatureSpan">webpack.ContextModuleFactory.prototype.</span>resolveDependencies (fs, resource, recursive, regExp, callback)](#apidoc.element.webpack.ContextModuleFactory.prototype.resolveDependencies)
- description and source-code
```javascript
function resolveDependencies(fs, resource, recursive, regExp, callback) {
	if(!regExp || !resource)
		return callback(null, []);
	(function addDirectory(directory, callback) {
		fs.readdir(directory, function(err, files) {
			if(err) return callback(err);
			if(!files || files.length === 0) return callback(null, []);
			async.map(files.filter(function(p) {
				return p.indexOf(".") !== 0;
			}), function(seqment, callback) {

				var subResource = path.join(directory, seqment);

				fs.stat(subResource, function(err, stat) {
					if(err) return callback(err);

					if(stat.isDirectory()) {

						if(!recursive) return callback();
						addDirectory.call(this, subResource, callback);

					} else if(stat.isFile()) {

						var obj = {
							context: resource,
							request: "." + subResource.substr(resource.length).replace(/\\/g, "/")
						};

						this.applyPluginsAsyncWaterfall("alternatives", [obj], function(err, alternatives) {
							if(err) return callback(err);
							alternatives = alternatives.filter(function(obj) {
								return regExp.test(obj.request);
							}).map(function(obj) {
								var dep = new ContextElementDependency(obj.request);
								dep.optional = true;
								return dep;
							});
							callback(null, alternatives);
						});

					} else callback();

				}.bind(this));

			}.bind(this), function(err, result) {
				if(err) return callback(err);

				if(!result) return callback(null, []);

				callback(null, result.filter(function(i) {
					return !!i;
				}).reduce(function(a, i) {
					return a.concat(i);
				}, []));
			});
		}.bind(this));
	}.call(this, resource, callback));
}
```
- example usage
```shell
...
		this.built = false;
		super.unbuild();
	}

	build(options, compilation, resolver, fs, callback) {
		this.built = true;
		this.builtTime = new Date().getTime();
		this.resolveDependencies(fs, this.context, this.recursive, this.regExp, (err, dependencies) => {
			if(err) return callback(err);

			if(!dependencies) {
				this.dependencies = [];
				callback();
				return;
			}
...
```



# <a name="apidoc.module.webpack.DelegatedModule"></a>[module webpack.DelegatedModule](#apidoc.module.webpack.DelegatedModule)

#### <a name="apidoc.element.webpack.DelegatedModule.DelegatedModule"></a>[function <span class="apidocSignatureSpan">webpack.</span>DelegatedModule (sourceRequest, data, type, userRequest)](#apidoc.element.webpack.DelegatedModule.DelegatedModule)
- description and source-code
```javascript
function DelegatedModule(sourceRequest, data, type, userRequest) {
	Module.call(this);
	this.sourceRequest = sourceRequest;
	this.request = data.id;
	this.meta = data.meta;
	this.type = type;
	this.userRequest = userRequest;
	this.built = false;
	this.delegateData = data;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.DelegatedModule.prototype"></a>[module webpack.DelegatedModule.prototype](#apidoc.module.webpack.DelegatedModule.prototype)

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.build"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>build (options, compilation, resolver, fs, callback)](#apidoc.element.webpack.DelegatedModule.prototype.build)
- description and source-code
```javascript
build = function (options, compilation, resolver, fs, callback) {
	this.built = true;
	this.builtTime = new Date().getTime();
	this.usedExports = true;
	this.providedExports = this.delegateData.exports || true;
	this.dependencies.length = 0;
	this.addDependency(new DelegatedSourceDependency(this.sourceRequest));
	callback();
}
```
- example usage
```shell
...
		if(module.building) return module.building.push(thisCallback);
		const building = module.building = [thisCallback];

		function callback(err) {
			module.building = undefined;
			building.forEach(cb => cb(err));
		}
		module.build(this.options, this, this.resolvers.normal, this.inputFileSystem, (error) => {
			const errors = module.errors;
			for(let indexError = 0; indexError < errors.length; indexError++) {
				const err = errors[indexError];
				err.origin = origin;
				err.dependencies = dependencies;
				if(optional)
					this.warnings.push(err);
...
```

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>constructor (sourceRequest, data, type, userRequest)](#apidoc.element.webpack.DelegatedModule.prototype.constructor)
- description and source-code
```javascript
function DelegatedModule(sourceRequest, data, type, userRequest) {
	Module.call(this);
	this.sourceRequest = sourceRequest;
	this.request = data.id;
	this.meta = data.meta;
	this.type = type;
	this.userRequest = userRequest;
	this.built = false;
	this.delegateData = data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.identifier"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>identifier ()](#apidoc.element.webpack.DelegatedModule.prototype.identifier)
- description and source-code
```javascript
identifier = function () {
	return "delegated " + JSON.stringify(this.request) + " from " + this.sourceRequest;
}
```
- example usage
```shell
...
			'Use equal casing. Compare these module identifiers:\n${modulesList}';
		this.origin = this.module = sortedModules[0];
		Error.captureStackTrace(this, CaseSensitiveModulesWarning);
	}

	_sort(modules) {
		return modules.slice().sort((a, b) => {
			a = a.identifier();
			b = b.identifier();
			/* istanbul ignore next */
			if(a < b) return -1;
			/* istanbul ignore next */
			if(a > b) return 1;
			/* istanbul ignore next */
			return 0;
...
```

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.needRebuild"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>needRebuild ()](#apidoc.element.webpack.DelegatedModule.prototype.needRebuild)
- description and source-code
```javascript
needRebuild = function () {
	return false;
}
```
- example usage
```shell
...
		}
		const cacheName = (cacheGroup || "m") + identifier;
		if(this.cache && this.cache[cacheName]) {
			const cacheModule = this.cache[cacheName];

			let rebuild = true;
			if(!cacheModule.error && cacheModule.cacheable && this.fileTimestamps && this.contextTimestamps) {
				rebuild = cacheModule.needRebuild(this.fileTimestamps, this.contextTimestamps);
			}

			if(!rebuild) {
				cacheModule.disconnect();
				this._modules[identifier] = cacheModule;
				this.modules.push(cacheModule);
				cacheModule.errors.forEach(err => this.errors.push(err), this);
...
```

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.readableIdentifier"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>readableIdentifier ()](#apidoc.element.webpack.DelegatedModule.prototype.readableIdentifier)
- description and source-code
```javascript
readableIdentifier = function () {
	return "delegated " + this.userRequest + " from " + this.sourceRequest;
}
```
- example usage
```shell
...
			source.add("\n\n/***/ })");
			return source;
		});

		moduleTemplate.plugin("package", function(moduleSource, module) {
			if(this.outputOptions.pathinfo) {
				const source = new ConcatSource();
				const req = module.readableIdentifier(this.requestShortener);
				if(Array.isArray(module.providedExports))
					source.add("/* exports provided: " + module.providedExports.join(", ") + " */\n");
				else if(module.providedExports)
					source.add("/* unknown exports provided */\n");
				if(Array.isArray(module.usedExports))
					source.add("/* exports used: " + module.usedExports.join(", ") + " */\n");
				else if(module.usedExports)
...
```

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.size"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>size ()](#apidoc.element.webpack.DelegatedModule.prototype.size)
- description and source-code
```javascript
size = function () {
	return 42;
}
```
- example usage
```shell
...

		return size * multiplicator + overhead;
	}

	modulesSize() {
		let count = 0;
		for(let i = 0; i < this.modules.length; i++) {
			count += this.modules[i].size();
		}
		return count;
	}

	size(options) {
		return this.addMultiplierAndOverhead(this.modulesSize(), options);
	}
...
```

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.source"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>source ()](#apidoc.element.webpack.DelegatedModule.prototype.source)
- description and source-code
```javascript
source = function () {
	var sourceModule = this.dependencies[0].module;
	var str;
	if(!sourceModule) {
		str = WebpackMissingModule.moduleCode(this.sourceRequest);
	} else {
		str = "module.exports = (__webpack_require__(" + sourceModule.id + "))";
		switch(this.type) {
			case "require":
				str += "(" + JSON.stringify(this.request) + ");";
				break;
			case "object":
				str += "[" + JSON.stringify(this.request) + "];";
				break;
		}
	}
	if(this.useSourceMap) {
		return new OriginalSource(str, this.identifier());
	} else {
		return new RawSource(str);
	}
}
```
- example usage
```shell
...
	constructor(sourceUrlComment, moduleFilenameTemplate) {
		this.sourceUrlComment = sourceUrlComment || "\n//# sourceURL=[url]";
		this.moduleFilenameTemplate = moduleFilenameTemplate || "webpack:///[resourcePath]?[loaders]";
	}

	apply(moduleTemplate) {
		moduleTemplate.plugin("module", (source, module) => {
			const content = source.source();
			const str = ModuleFilenameHelpers.createFilename(module, this.moduleFilenameTemplate, moduleTemplate.requestShortener);
			const footer = ["\n",
				ModuleFilenameHelpers.createFooter(module, moduleTemplate.requestShortener),
				this.sourceUrlComment.replace(/\[url\]/g, encodeURI(str).replace(/%2F/g, "/").replace(/%20/g, "_").replace(/%5E/g, "^").replace
(/%5C/g, "\\").replace(/^\//, ""))
			].join("\n");
			return new RawSource('eval(${JSON.stringify(content + footer)});');
		});
...
```

#### <a name="apidoc.element.webpack.DelegatedModule.prototype.unbuild"></a>[function <span class="apidocSignatureSpan">webpack.DelegatedModule.prototype.</span>unbuild ()](#apidoc.element.webpack.DelegatedModule.prototype.unbuild)
- description and source-code
```javascript
unbuild = function () {
	this.built = false;
	Module.prototype.unbuild.call(this);
}
```
- example usage
```shell
...
				cacheModule.errors.forEach(err => this.errors.push(err), this);
				cacheModule.warnings.forEach(err => this.warnings.push(err), this);
				return cacheModule;
			} else {
				module.lastId = cacheModule.id;
			}
		}
		module.unbuild();
		this._modules[identifier] = module;
		if(this.cache) {
			this.cache[cacheName] = module;
		}
		this.modules.push(module);
		return true;
	}
...
```



# <a name="apidoc.module.webpack.DependenciesBlock"></a>[module webpack.DependenciesBlock](#apidoc.module.webpack.DependenciesBlock)

#### <a name="apidoc.element.webpack.DependenciesBlock.DependenciesBlock"></a>[function <span class="apidocSignatureSpan">webpack.</span>DependenciesBlock ()](#apidoc.element.webpack.DependenciesBlock.DependenciesBlock)
- description and source-code
```javascript
function DependenciesBlock() {
	this.dependencies = [];
	this.blocks = [];
	this.variables = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.DependenciesBlock.prototype"></a>[module webpack.DependenciesBlock.prototype](#apidoc.module.webpack.DependenciesBlock.prototype)

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.addBlock"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>addBlock (block)](#apidoc.element.webpack.DependenciesBlock.prototype.addBlock)
- description and source-code
```javascript
addBlock = function (block) {
	this.blocks.push(block);
	block.parent = this;
}
```
- example usage
```shell
...
		otherChunk.chunks.length = 0;

		otherChunk.blocks.forEach(b => {
			b.chunks = b.chunks ? b.chunks.map(c => {
				return c === otherChunk ? this : c;
			}) : [this];
			b.chunkReason = reason;
			this.addBlock(b);
		});
		otherChunk.blocks.length = 0;

		otherChunk.origins.forEach(origin => {
			this.origins.push(origin);
		});
		this.origins.forEach(origin => {
...
```

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.addDependency"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>addDependency (dependency)](#apidoc.element.webpack.DependenciesBlock.prototype.addDependency)
- description and source-code
```javascript
addDependency = function (dependency) {
	this.dependencies.push(dependency);
}
```
- example usage
```shell
...
					const dep = new ConstDependency("require", expr.callee.range);
					dep.loc = expr.loc;
					if(parser.state.current.dependencies.length > 1) {
						const last = parser.state.current.dependencies[parser.state.current.dependencies.length - 1];
						if(last.critical && last.request === "." && last.userRequest === "." && last.recursive)
							parser.state.current.dependencies.pop();
					}
					parser.state.current.addDependency(dep);
					return true;
				});
			});

			params.normalModuleFactory.plugin("after-resolve", (data, done) => {
				// if this is a json file and there are no loaders active, we use the json-loader in order to avoid parse errors
				// @see https://github.com/webpack/webpack/issues/3363
...
```

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.addVariable"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>addVariable (name, expression, dependencies)](#apidoc.element.webpack.DependenciesBlock.prototype.addVariable)
- description and source-code
```javascript
addVariable = function (name, expression, dependencies) {
	for(var i = 0; i < this.variables.length; i++) {
		var v = this.variables[i];
		if(v.name === name && v.expression === expression) return;
	}
	this.variables.push(new DependenciesBlockVariable(name, expression, dependencies));
}
```
- example usage
```shell
...
				});
				parser.plugin("evaluate Identifier __resourceQuery", function(expr) {
					if(!this.state.module) return;
					return ParserHelpers.evaluateToString(getQuery(this.state.module.resource))(expr);
				});
				parser.plugin("expression __resourceQuery", function() {
					if(!this.state.module) return;
					this.state.current.addVariable("__resourceQuery", JSON.stringify(getQuery(this.state.module.resource)));
					return true;
				});
			});
		});
	}
}
...
```

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>disconnect ()](#apidoc.element.webpack.DependenciesBlock.prototype.disconnect)
- description and source-code
```javascript
disconnect = function () {
	function disconnect(i) {
		i.disconnect();
	}
	this.dependencies.forEach(disconnect);
	this.blocks.forEach(disconnect);
	this.variables.forEach(disconnect);
}
```
- example usage
```shell
...
		hash.update(this.chunks && this.chunks.map((chunk) => {
			return typeof chunk.id === "number" ? chunk.id : "";
		}).join(",") || "");
		super.updateHash(hash);
	}
	disconnect() {
		this.chunks = null;
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
		super.unseal();
	}
	sortItems() {
		super.sortItems();
...
```

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.hasDependencies"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>hasDependencies (filter)](#apidoc.element.webpack.DependenciesBlock.prototype.hasDependencies)
- description and source-code
```javascript
hasDependencies = function (filter) {
	if(filter) {
		if(this.dependencies.some(filter)) return true;
	} else {
		if(this.dependencies.length > 0) return true;
	}

	return this.blocks.concat(this.variables).some(function(item) {
		return item.hasDependencies(filter);
	});
}
```
- example usage
```shell
...
	if(filter) {
		if(this.dependencies.some(filter)) return true;
	} else {
		if(this.dependencies.length > 0) return true;
	}

	return this.blocks.concat(this.variables).some(function(item) {
		return item.hasDependencies(filter);
	});
};

DependenciesBlock.prototype.sortItems = function() {
	this.blocks.forEach(function(block) {
		block.sortItems();
	});
...
```

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.sortItems"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>sortItems ()](#apidoc.element.webpack.DependenciesBlock.prototype.sortItems)
- description and source-code
```javascript
sortItems = function () {
	this.blocks.forEach(function(block) {
		block.sortItems();
	});
}
```
- example usage
```shell
...
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
		super.unseal();
	}
	sortItems() {
		super.sortItems();
		if(this.chunks) {
			this.chunks.sort((a, b) => {
				let i = 0;
				while(true) { // eslint-disable-line no-constant-condition
					if(!a.modules[i] && !b.modules[i]) return 0;
					if(!a.modules[i]) return -1;
					if(!b.modules[i]) return 1;
...
```

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.unseal"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>unseal ()](#apidoc.element.webpack.DependenciesBlock.prototype.unseal)
- description and source-code
```javascript
unseal = function () {
	function unseal(i) {
		i.unseal();
	}
	this.blocks.forEach(unseal);
}
```
- example usage
```shell
...
	}
	disconnect() {
		this.chunks = null;
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
		super.unseal();
	}
	sortItems() {
		super.sortItems();
		if(this.chunks) {
			this.chunks.sort((a, b) => {
				let i = 0;
				while(true) { // eslint-disable-line no-constant-condition
...
```

#### <a name="apidoc.element.webpack.DependenciesBlock.prototype.updateHash"></a>[function <span class="apidocSignatureSpan">webpack.DependenciesBlock.prototype.</span>updateHash (hash)](#apidoc.element.webpack.DependenciesBlock.prototype.updateHash)
- description and source-code
```javascript
updateHash = function (hash) {
	this.dependencies.forEach(function(d) {
		d.updateHash(hash);
	});
	this.blocks.forEach(function(b) {
		b.updateHash(hash);
	});
	this.variables.forEach(function(v) {
		v.updateHash(hash);
	});
}
```
- example usage
```shell
...
		throw new Error("'chunk' was been renamed to 'chunks' and is now an array");
	}
	updateHash(hash) {
		hash.update(this.chunkName || "");
		hash.update(this.chunks && this.chunks.map((chunk) => {
			return typeof chunk.id === "number" ? chunk.id : "";
		}).join(",") || "");
		super.updateHash(hash);
	}
	disconnect() {
		this.chunks = null;
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
...
```



# <a name="apidoc.module.webpack.Dependency"></a>[module webpack.Dependency](#apidoc.module.webpack.Dependency)

#### <a name="apidoc.element.webpack.Dependency.Dependency"></a>[function <span class="apidocSignatureSpan">webpack.</span>Dependency ()](#apidoc.element.webpack.Dependency.Dependency)
- description and source-code
```javascript
class Dependency {
	constructor() {
		this.module = null;
	}

	isEqualResource() {
		return false;
	}

	// Returns the referenced module and export
	getReference() {
		if(!this.module) return null;
		return {
			module: this.module,
			importedNames: true, // true: full object, false: only sideeffects/no export, array of strings: the exports with this names
		};
	}

	// Returns the exported names
	getExports() {
		return null;
	}

	getWarnings() {
		return null;
	}

	getErrors() {
		return null;
	}

	updateHash(hash) {
		hash.update((this.module && this.module.id) + "");
	}

	disconnect() {
		this.module = null;
	}

	compare(a, b) {
		return compareLocations(a.loc, b.loc);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Dependency.compare"></a>[function <span class="apidocSignatureSpan">webpack.Dependency.</span>compare (a, b)](#apidoc.element.webpack.Dependency.compare)
- description and source-code
```javascript
(a, b) => compareLocations(a.loc, b.loc)
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.DynamicEntryPlugin"></a>[module webpack.DynamicEntryPlugin](#apidoc.module.webpack.DynamicEntryPlugin)

#### <a name="apidoc.element.webpack.DynamicEntryPlugin.DynamicEntryPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>DynamicEntryPlugin (context, entry)](#apidoc.element.webpack.DynamicEntryPlugin.DynamicEntryPlugin)
- description and source-code
```javascript
class DynamicEntryPlugin {
	constructor(context, entry) {
		this.context = context;
		this.entry = entry;
	}

	apply(compiler) {
		compiler.plugin("compilation", (compilation, params) => {
			const multiModuleFactory = new MultiModuleFactory();
			const normalModuleFactory = params.normalModuleFactory;

			compilation.dependencyFactories.set(MultiEntryDependency, multiModuleFactory);
			compilation.dependencyFactories.set(SingleEntryDependency, normalModuleFactory);
		});

		compiler.plugin("make", (compilation, callback) => {
			const addEntry = (entry, name) => {
				const dep = DynamicEntryPlugin.createDependency(entry, name);
				return new Promise((resolve, reject) => {
					compilation.addEntry(this.context, dep, name, (err) => {
						if(err) return reject(err);
						resolve();
					});
				});
			};

			Promise.resolve(this.entry()).then((entry) => {
				if(typeof entry === "string" || Array.isArray(entry)) {
					addEntry(entry, "main").then(() => callback(), callback);
				} else if(typeof entry === "object") {
					Promise.all(Object.keys(entry).map((name) => {
						return addEntry(entry[name], name);
					})).then(() => callback(), callback);
				}
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.DynamicEntryPlugin.createDependency"></a>[function <span class="apidocSignatureSpan">webpack.DynamicEntryPlugin.</span>createDependency (entry, name)](#apidoc.element.webpack.DynamicEntryPlugin.createDependency)
- description and source-code
```javascript
createDependency = function (entry, name) {
	if(Array.isArray(entry))
		return MultiEntryPlugin.createDependency(entry, name);
	else
		return SingleEntryPlugin.createDependency(entry, name);
}
```
- example usage
```shell
...

			compilation.dependencyFactories.set(MultiEntryDependency, multiModuleFactory);
			compilation.dependencyFactories.set(SingleEntryDependency, normalModuleFactory);
		});

		compiler.plugin("make", (compilation, callback) => {
			const addEntry = (entry, name) => {
				const dep = DynamicEntryPlugin.createDependency(entry, name);
				return new Promise((resolve, reject) => {
					compilation.addEntry(this.context, dep, name, (err) => {
						if(err) return reject(err);
						resolve();
					});
				});
			};
...
```



# <a name="apidoc.module.webpack.EntryModuleNotFoundError"></a>[module webpack.EntryModuleNotFoundError](#apidoc.module.webpack.EntryModuleNotFoundError)

#### <a name="apidoc.element.webpack.EntryModuleNotFoundError.EntryModuleNotFoundError"></a>[function <span class="apidocSignatureSpan">webpack.</span>EntryModuleNotFoundError (err)](#apidoc.element.webpack.EntryModuleNotFoundError.EntryModuleNotFoundError)
- description and source-code
```javascript
function EntryModuleNotFoundError(err) {
	Error.call(this);
	this.name = "EntryModuleNotFoundError";
	this.message = "Entry module not found: " + err;
	this.details = err.details;
	this.error = err;
	Error.captureStackTrace(this, EntryModuleNotFoundError);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.EntryModuleNotFoundError.prototype"></a>[module webpack.EntryModuleNotFoundError.prototype](#apidoc.module.webpack.EntryModuleNotFoundError.prototype)

#### <a name="apidoc.element.webpack.EntryModuleNotFoundError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.EntryModuleNotFoundError.prototype.</span>constructor (err)](#apidoc.element.webpack.EntryModuleNotFoundError.prototype.constructor)
- description and source-code
```javascript
function EntryModuleNotFoundError(err) {
	Error.call(this);
	this.name = "EntryModuleNotFoundError";
	this.message = "Entry module not found: " + err;
	this.details = err.details;
	this.error = err;
	Error.captureStackTrace(this, EntryModuleNotFoundError);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.ErrorHelpers"></a>[module webpack.ErrorHelpers](#apidoc.module.webpack.ErrorHelpers)

#### <a name="apidoc.element.webpack.ErrorHelpers.cleanUp"></a>[function <span class="apidocSignatureSpan">webpack.ErrorHelpers.</span>cleanUp (stack, message)](#apidoc.element.webpack.ErrorHelpers.cleanUp)
- description and source-code
```javascript
(stack, message) => {
	stack = exports.cutOffLoaderExecution(stack);
	stack = exports.cutOffMessage(stack, message);
	return stack;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ErrorHelpers.cutOffLoaderExecution"></a>[function <span class="apidocSignatureSpan">webpack.ErrorHelpers.</span>cutOffLoaderExecution (stack)](#apidoc.element.webpack.ErrorHelpers.cutOffLoaderExecution)
- description and source-code
```javascript
(stack) => {
	stack = stack.split("\n");
	for(let i = 0; i < stack.length; i++)
		if(stack[i].indexOf(loaderFlag) >= 0)
			stack.length = i;
	return stack.join("\n");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ErrorHelpers.cutOffMessage"></a>[function <span class="apidocSignatureSpan">webpack.ErrorHelpers.</span>cutOffMessage (stack, message)](#apidoc.element.webpack.ErrorHelpers.cutOffMessage)
- description and source-code
```javascript
(stack, message) => {
	const nextLine = stack.indexOf("\n");
	if(nextLine === -1) {
		return stack === message ? "" : stack;
	} else {
		const firstLine = stack.substr(0, nextLine);
		return firstLine === message ? stack.substr(nextLine + 1) : stack;
	}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.ExternalModuleFactoryPlugin"></a>[module webpack.ExternalModuleFactoryPlugin](#apidoc.module.webpack.ExternalModuleFactoryPlugin)

#### <a name="apidoc.element.webpack.ExternalModuleFactoryPlugin.ExternalModuleFactoryPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>ExternalModuleFactoryPlugin (type, externals)](#apidoc.element.webpack.ExternalModuleFactoryPlugin.ExternalModuleFactoryPlugin)
- description and source-code
```javascript
function ExternalModuleFactoryPlugin(type, externals) {
	this.type = type;
	this.externals = externals;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.ExternalModuleFactoryPlugin.prototype"></a>[module webpack.ExternalModuleFactoryPlugin.prototype](#apidoc.module.webpack.ExternalModuleFactoryPlugin.prototype)

#### <a name="apidoc.element.webpack.ExternalModuleFactoryPlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.ExternalModuleFactoryPlugin.prototype.</span>apply (normalModuleFactory)](#apidoc.element.webpack.ExternalModuleFactoryPlugin.prototype.apply)
- description and source-code
```javascript
apply = function (normalModuleFactory) {
	var globalType = this.type;
	normalModuleFactory.plugin("factory", function(factory) {
		return function(data, callback) {
			var context = data.context;
			var dependency = data.dependencies[0];

			function handleExternal(value, type, callback) {
				if(typeof type === "function") {
					callback = type;
					type = undefined;
				}
				if(value === false) return factory(data, callback);
				if(value === true) value = dependency.request;
				if(typeof type === "undefined" && /^[a-z0-9]+ /.test(value)) {
					var idx = value.indexOf(" ");
					type = value.substr(0, idx);
					value = value.substr(idx + 1);
				}
				callback(null, new ExternalModule(value, type || globalType));
				return true;
			}
			(function handleExternals(externals, callback) {
				if(typeof externals === "string") {
					if(externals === dependency.request) {
						return handleExternal(dependency.request, callback);
					}
				} else if(Array.isArray(externals)) {
					var i = 0;
					(function next() {
						var handleExternalsAndCallback = function handleExternalsAndCallback(err, module) {
							if(err) return callback(err);
							if(!module) {
								if(async) {
									async = false;
									return;
								}
								return next();
							}
							callback(null, module);
						};

						do {
							var async = true;
							if(i >= externals.length) return callback();
							handleExternals(externals[i++], handleExternalsAndCallback);
						} while (!async); // eslint-disable-line keyword-spacing
						async = false;
					}());
					return;
				} else if(externals instanceof RegExp) {
					if(externals.test(dependency.request)) {
						return handleExternal(dependency.request, callback);
					}
				} else if(typeof externals === "function") {
					externals.call(null, context, dependency.request, function(err, value, type) {
						if(err) return callback(err);
						if(typeof value !== "undefined") {
							handleExternal(value, type, callback);
						} else {
							callback();
						}
					});
					return;
				} else if(typeof externals === "object" && Object.prototype.hasOwnProperty.call(externals, dependency.request)) {
					return handleExternal(externals[dependency.request], callback);
				}
				callback();
			}(this.externals, function(err, module) {
				if(err) return callback(err);
				if(!module) return handleExternal(false, callback);
				return callback(null, module);
			}));
		}.bind(this);
	}.bind(this));
}
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.FlagDependencyUsagePlugin"></a>[module webpack.FlagDependencyUsagePlugin](#apidoc.module.webpack.FlagDependencyUsagePlugin)

#### <a name="apidoc.element.webpack.FlagDependencyUsagePlugin.FlagDependencyUsagePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>FlagDependencyUsagePlugin ()](#apidoc.element.webpack.FlagDependencyUsagePlugin.FlagDependencyUsagePlugin)
- description and source-code
```javascript
function FlagDependencyUsagePlugin() {

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.FlagDependencyUsagePlugin.prototype"></a>[module webpack.FlagDependencyUsagePlugin.prototype](#apidoc.module.webpack.FlagDependencyUsagePlugin.prototype)

#### <a name="apidoc.element.webpack.FlagDependencyUsagePlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.FlagDependencyUsagePlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.FlagDependencyUsagePlugin.prototype.apply)
- description and source-code
```javascript
apply = function (compiler) {
	compiler.plugin("compilation", function(compilation) {
		compilation.plugin("optimize-modules-advanced", function(modules) {

			modules.forEach(function(module) {
				module.used = false;
			});

			var queue = [];
			compilation.chunks.forEach(function(chunk) {
				if(chunk.entryModule) {
					processModule(chunk.entryModule, true);
				}
			});

			while(queue.length) {
				var queueItem = queue.pop();
				processDependenciesBlock(queueItem[0], queueItem[1]);
			}

			function processModule(module, usedExports) {
				module.used = true;
				if(module.usedExports === true)
					return;
				else if(usedExports === true)
					module.usedExports = true;
				else if(Array.isArray(usedExports)) {
					var old = module.usedExports ? module.usedExports.length : -1;
					module.usedExports = addToSet(module.usedExports || [], usedExports);
					if(module.usedExports.length === old)
						return;
				} else if(Array.isArray(module.usedExports))
					return;
				else
					module.usedExports = false;

				queue.push([module, module.usedExports]);
			}

			function processDependenciesBlock(depBlock, usedExports) {
				depBlock.dependencies.forEach(function(dep) {
					processDependency(dep, usedExports);
				});
				depBlock.variables.forEach(function(variable) {
					variable.dependencies.forEach(function(dep) {
						processDependency(dep, usedExports);
					});
				});
				depBlock.blocks.forEach(function(block) {
					queue.push([block, usedExports]);
				});
			}

			function processDependency(dep, usedExports) {
				var reference = dep.getReference && dep.getReference();
				if(!reference) return;
				var module = reference.module;
				var importedNames = reference.importedNames;
				var oldUsed = module.used;
				var oldUsedExports = module.usedExports;
				if(!oldUsed || (importedNames && (!oldUsedExports || !isSubset(oldUsedExports, importedNames)))) {
					processModule(module, importedNames);
				}
			}

		});

		function addToSet(a, b) {
			b.forEach(function(item) {
				if(a.indexOf(item) < 0)
					a.push(item);
			});
			return a;
		}

		function isSubset(biggerSet, subset) {
			if(biggerSet === true) return true;
			if(subset === true) return false;
			return subset.every(function(item) {
				return biggerSet.indexOf(item) >= 0;
			});
		}
	});
}
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.HotModuleReplacementPlugin"></a>[module webpack.HotModuleReplacementPlugin](#apidoc.module.webpack.HotModuleReplacementPlugin)

#### <a name="apidoc.element.webpack.HotModuleReplacementPlugin.HotModuleReplacementPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>HotModuleReplacementPlugin (options)](#apidoc.element.webpack.HotModuleReplacementPlugin.HotModuleReplacementPlugin)
- description and source-code
```javascript
function HotModuleReplacementPlugin(options) {
	options = options || {};
	this.multiStep = options.multiStep;
	this.fullBuildTimeout = options.fullBuildTimeout || 200;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.HotModuleReplacementPlugin.prototype"></a>[module webpack.HotModuleReplacementPlugin.prototype](#apidoc.module.webpack.HotModuleReplacementPlugin.prototype)

#### <a name="apidoc.element.webpack.HotModuleReplacementPlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.HotModuleReplacementPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.HotModuleReplacementPlugin.prototype.apply)
- description and source-code
```javascript
apply = function (compiler) {
	var multiStep = this.multiStep;
	var fullBuildTimeout = this.fullBuildTimeout;
	var hotUpdateChunkFilename = compiler.options.output.hotUpdateChunkFilename;
	var hotUpdateMainFilename = compiler.options.output.hotUpdateMainFilename;
	compiler.plugin("compilation", function(compilation, params) {
		var hotUpdateChunkTemplate = compilation.hotUpdateChunkTemplate;
		if(!hotUpdateChunkTemplate) return;

		var normalModuleFactory = params.normalModuleFactory;

		compilation.dependencyFactories.set(ConstDependency, new NullFactory());
		compilation.dependencyTemplates.set(ConstDependency, new ConstDependency.Template());

		compilation.dependencyFactories.set(ModuleHotAcceptDependency, normalModuleFactory);
		compilation.dependencyTemplates.set(ModuleHotAcceptDependency, new ModuleHotAcceptDependency.Template());

		compilation.dependencyFactories.set(ModuleHotDeclineDependency, normalModuleFactory);
		compilation.dependencyTemplates.set(ModuleHotDeclineDependency, new ModuleHotDeclineDependency.Template());

		compilation.plugin("record", function(compilation, records) {
			if(records.hash === this.hash) return;
			records.hash = compilation.hash;
			records.moduleHashs = {};
			this.modules.forEach(function(module) {
				var identifier = module.identifier();
				var hash = require("crypto").createHash("md5");
				module.updateHash(hash);
				records.moduleHashs[identifier] = hash.digest("hex");
			});
			records.chunkHashs = {};
			this.chunks.forEach(function(chunk) {
				records.chunkHashs[chunk.id] = chunk.hash;
			});
			records.chunkModuleIds = {};
			this.chunks.forEach(function(chunk) {
				records.chunkModuleIds[chunk.id] = chunk.modules.map(function(m) {
					return m.id;
				});
			});
		});
		var initialPass = false;
		var recompilation = false;
		compilation.plugin("after-hash", function() {
			var records = this.records;
			if(!records) {
				initialPass = true;
				return;
			}
			if(!records.hash)
				initialPass = true;
			var preHash = records.preHash || "x";
			var prepreHash = records.prepreHash || "x";
			if(preHash === this.hash) {
				recompilation = true;
				this.modifyHash(prepreHash);
				return;
			}
			records.prepreHash = records.hash || "x";
			records.preHash = this.hash;
			this.modifyHash(records.prepreHash);
		});
		compilation.plugin("should-generate-chunk-assets", function() {
			if(multiStep && !recompilation && !initialPass)
				return false;
		});
		compilation.plugin("need-additional-pass", function() {
			if(multiStep && !recompilation && !initialPass)
				return true;
		});
		compiler.plugin("additional-pass", function(callback) {
			if(multiStep)
				return setTimeout(callback, fullBuildTimeout);
			return callback();
		});
		compilation.plugin("additional-chunk-assets", function() {
			var records = this.records;
			if(records.hash === this.hash) return;
			if(!records.moduleHashs || !records.chunkHashs || !records.chunkModuleIds) return;
			this.modules.forEach(function(module) {
				var identifier = module.identifier();
				var hash = require("crypto").createHash("md5");
				module.updateHash(hash);
				hash = hash.digest("hex");
				module.hotUpdate = records.moduleHashs[identifier] !== hash;
			});
			var hotUpdateMainContent = {
				h: this.hash,
				c: {}
			};
			Object.keys(records.chunkHashs).forEach(function(chunkId) {
				chunkId = +chunkId;
				var currentChunk = this.chunks.filter(function(chunk) {
					return chunk.id === chunkId;
				})[0];
				if(currentChunk) {
					var newModules = currentChunk.modules.filter(function(module) {
						return module.hotUpdate;
					});
					var allModules = {};
					currentChunk.modules.forEach(function(module) {
						allModules[module.id] = true;
					});
					var removedModules = records.chunkModuleIds[chunkId].filter(function(id) {
						return !allModules[id];
					});
					if(newModules.length > 0 || removedModules.length > 0) {
						var source = hotUpdateChunkTemplate.render(chunkId, newModules, r ...
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.JsonpChunkTemplatePlugin"></a>[module webpack.JsonpChunkTemplatePlugin](#apidoc.module.webpack.JsonpChunkTemplatePlugin)

#### <a name="apidoc.element.webpack.JsonpChunkTemplatePlugin.JsonpChunkTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>JsonpChunkTemplatePlugin ()](#apidoc.element.webpack.JsonpChunkTemplatePlugin.JsonpChunkTemplatePlugin)
- description and source-code
```javascript
function JsonpChunkTemplatePlugin() {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.JsonpChunkTemplatePlugin.prototype"></a>[module webpack.JsonpChunkTemplatePlugin.prototype](#apidoc.module.webpack.JsonpChunkTemplatePlugin.prototype)

#### <a name="apidoc.element.webpack.JsonpChunkTemplatePlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.JsonpChunkTemplatePlugin.prototype.</span>apply (chunkTemplate)](#apidoc.element.webpack.JsonpChunkTemplatePlugin.prototype.apply)
- description and source-code
```javascript
apply = function (chunkTemplate) {
	chunkTemplate.plugin("render", function(modules, chunk) {
		var jsonpFunction = this.outputOptions.jsonpFunction;
		var source = new ConcatSource();
		source.add(jsonpFunction + "(" + JSON.stringify(chunk.ids) + ",");
		source.add(modules);
		var entries = [chunk.entryModule].filter(Boolean).map(function(m) {
			return m.id;
		});
		if(entries.length > 0) {
			source.add("," + JSON.stringify(entries));
		}
		source.add(")");
		return source;
	});
	chunkTemplate.plugin("hash", function(hash) {
		hash.update("JsonpChunkTemplatePlugin");
		hash.update("3");
		hash.update(this.outputOptions.jsonpFunction + "");
		hash.update(this.outputOptions.library + "");
	});
}
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.JsonpMainTemplatePlugin"></a>[module webpack.JsonpMainTemplatePlugin](#apidoc.module.webpack.JsonpMainTemplatePlugin)

#### <a name="apidoc.element.webpack.JsonpMainTemplatePlugin.JsonpMainTemplatePlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>JsonpMainTemplatePlugin ()](#apidoc.element.webpack.JsonpMainTemplatePlugin.JsonpMainTemplatePlugin)
- description and source-code
```javascript
function JsonpMainTemplatePlugin() {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.JsonpMainTemplatePlugin.prototype"></a>[module webpack.JsonpMainTemplatePlugin.prototype](#apidoc.module.webpack.JsonpMainTemplatePlugin.prototype)

#### <a name="apidoc.element.webpack.JsonpMainTemplatePlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.JsonpMainTemplatePlugin.prototype.</span>apply (mainTemplate)](#apidoc.element.webpack.JsonpMainTemplatePlugin.prototype.apply)
- description and source-code
```javascript
apply = function (mainTemplate) {
	mainTemplate.plugin("local-vars", function(source, chunk) {
		if(chunk.chunks.length > 0) {
			return this.asString([
				source,
				"",
				"// objects to store loaded and loading chunks",
				"var installedChunks = {",
				this.indent(
					chunk.ids.map(function(id) {
						return id + ": 0";
					}).join(",\n")
				),
				"};"
			]);
		}
		return source;
	});
	mainTemplate.plugin("jsonp-script", function(_, chunk, hash) {
		var chunkFilename = this.outputOptions.chunkFilename;
		var chunkMaps = chunk.getChunkMaps();
		var crossOriginLoading = this.outputOptions.crossOriginLoading;
		var chunkLoadTimeout = this.outputOptions.chunkLoadTimeout || 120000;
		return this.asString([
			"var script = document.createElement('script');",
			"script.type = 'text/javascript';",
			"script.charset = 'utf-8';",
			"script.async = true;",
			"script.timeout = " + chunkLoadTimeout + ";",
			crossOriginLoading ? "script.crossOrigin = '" + crossOriginLoading + "';" : "",
			"if (" + this.requireFn + ".nc) {",
			this.indent("script.setAttribute(\"nonce\", " + this.requireFn + ".nc);"),
			"}",
			"script.src = " + this.requireFn + ".p + " +
			this.applyPluginsWaterfall("asset-path", JSON.stringify(chunkFilename), {
				hash: "\" + " + this.renderCurrentHashCode(hash) + " + \"",
				hashWithLength: function(length) {
					return "\" + " + this.renderCurrentHashCode(hash, length) + " + \"";
				}.bind(this),
				chunk: {
					id: "\" + chunkId + \"",
					hash: "\" + " + JSON.stringify(chunkMaps.hash) + "[chunkId] + \"",
					hashWithLength: function(length) {
						var shortChunkHashMap = {};
						Object.keys(chunkMaps.hash).forEach(function(chunkId) {
							if(typeof chunkMaps.hash[chunkId] === "string")
								shortChunkHashMap[chunkId] = chunkMaps.hash[chunkId].substr(0, length);
						});
						return "\" + " + JSON.stringify(shortChunkHashMap) + "[chunkId] + \"";
					},
					name: "\" + (" + JSON.stringify(chunkMaps.name) + "[chunkId]||chunkId) + \""
				}
			}) + ";",
			"var timeout = setTimeout(onScriptComplete, " + chunkLoadTimeout + ");",
			"script.onerror = script.onload = onScriptComplete;",
			"function onScriptComplete() {",
			this.indent([
				"// avoid mem leaks in IE.",
				"script.onerror = script.onload = null;",
				"clearTimeout(timeout);",
				"var chunk = installedChunks[chunkId];",
				"if(chunk !== 0) {",
				this.indent([
					"if(chunk) chunk[1](new Error('Loading chunk ' + chunkId + ' failed.'));",
					"installedChunks[chunkId] = undefined;"
				]),
				"}"
			]),
			"};",
		]);
	});
	mainTemplate.plugin("require-ensure", function(_, chunk, hash) {
		return this.asString([
			"if(installedChunks[chunkId] === 0)",
			this.indent([
				"return Promise.resolve();"
			]),
			"",
			"// a Promise means \"currently loading\".",
			"if(installedChunks[chunkId]) {",
			this.indent([
				"return installedChunks[chunkId][2];"
			]),
			"}",
			"",
			"// setup Promise in chunk cache",
			"var promise = new Promise(function(resolve, reject) {",
			this.indent([
				"installedChunks[chunkId] = [resolve, reject];"
			]),
			"});",
			"installedChunks[chunkId][2] = promise;",
			"",
			"// start chunk loading",
			"var head = document.getElementsByTagName('head')[0];",
			this.applyPluginsWaterfall("jsonp-script", "", chunk, hash),
			"head.appendChild(script);",
			"",
			"return promise;"
		]);
	});
	mainTemplate.plugin("require-extensions", function(source, chunk) {
		if(chunk.chunks.length === 0) return source;
		return this.asString([
			source,
			"",
			"// on error function for async loading",
			this.requireFn + ".oe = function(err) { console.error(err); throw err; };"
		]);
	});
	mainTemplate.plugin("bootstrap", function(source, chunk, hash) {
		if(chunk.chunks.length > 0) {
			var jsonpFunction = this.outputOptions.jsonpFunction;
			return this.asString([
				source,
				"",
				"// install a JSONP callback for chunk loading",
				"var parentJsonpFunction = win ...
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.LibManifestPlugin"></a>[module webpack.LibManifestPlugin](#apidoc.module.webpack.LibManifestPlugin)

#### <a name="apidoc.element.webpack.LibManifestPlugin.LibManifestPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>LibManifestPlugin (options)](#apidoc.element.webpack.LibManifestPlugin.LibManifestPlugin)
- description and source-code
```javascript
function LibManifestPlugin(options) {
	this.options = options;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.LibManifestPlugin.prototype"></a>[module webpack.LibManifestPlugin.prototype](#apidoc.module.webpack.LibManifestPlugin.prototype)

#### <a name="apidoc.element.webpack.LibManifestPlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.LibManifestPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.LibManifestPlugin.prototype.apply)
- description and source-code
```javascript
apply = function (compiler) {
	compiler.plugin("emit", function(compilation, callback) {
		async.forEach(compilation.chunks, function(chunk, callback) {
			if(!chunk.isInitial()) {
				callback();
				return;
			}
			var targetPath = compilation.getPath(this.options.path, {
				hash: compilation.hash,
				chunk: chunk
			});
			var name = this.options.name && compilation.getPath(this.options.name, {
				hash: compilation.hash,
				chunk: chunk
			});
			var manifest = {
				name: name,
				type: this.options.type,
				content: chunk.modules.reduce(function(obj, module) {
					if(module.libIdent) {
						var ident = module.libIdent({
							context: this.options.context || compiler.options.context
						});
						if(ident) {
							obj[ident] = {
								id: module.id,
								meta: module.meta,
								exports: Array.isArray(module.providedExports) ? module.providedExports : undefined
							};
						}
					}
					return obj;
				}.bind(this), {})
			};
			var content = new Buffer(JSON.stringify(manifest, null, 2), "utf8"); //eslint-disable-line
			compiler.outputFileSystem.mkdirp(path.dirname(targetPath), function(err) {
				if(err) return callback(err);
				compiler.outputFileSystem.writeFile(targetPath, content, callback);
			});
		}.bind(this), callback);
	}.bind(this));
}
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.MemoryOutputFileSystem"></a>[module webpack.MemoryOutputFileSystem](#apidoc.module.webpack.MemoryOutputFileSystem)

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.MemoryOutputFileSystem"></a>[function <span class="apidocSignatureSpan">webpack.</span>MemoryOutputFileSystem (data)](#apidoc.element.webpack.MemoryOutputFileSystem.MemoryOutputFileSystem)
- description and source-code
```javascript
function MemoryFileSystem(data) {
	this.data = data || {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.MemoryOutputFileSystem.prototype"></a>[module webpack.MemoryOutputFileSystem.prototype](#apidoc.module.webpack.MemoryOutputFileSystem.prototype)

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype._remove"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>_remove (_path, name, testFn)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype._remove)
- description and source-code
```javascript
_remove = function (_path, name, testFn) {
	var path = pathToArray(_path);
	if(path.length === 0) {
		throw new MemoryFileSystemError(errors.code.EPERM, _path);
	}
	var current = this.data;
	for(var i = 0; i < path.length - 1; i++) {
		if(!isDir(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.ENOENT, _path);
		current = current[path[i]];
	}
	if(!testFn(current[path[i]]))
		throw new MemoryFileSystemError(errors.code.ENOENT, _path);
	delete current[path[i]];
	return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.createReadStream"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>createReadStream (path, options)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.createReadStream)
- description and source-code
```javascript
createReadStream = function (path, options) {
	var stream = new ReadableStream();
	var done = false;
	var data;
	try {
		data = this.readFileSync(path);
	} catch (e) {
		stream._read = function() {
			if (done) {
				return;
			}
			done = true;
			this.emit('error', e);
			this.push(null);
		};
		return stream;
	}
	options = options || { };
	options.start = options.start || 0;
	options.end = options.end || data.length;
	stream._read = function() {
		if (done) {
			return;
		}
		done = true;
		this.push(data.slice(options.start, options.end));
		this.push(null);
	};
	return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.createWriteStream"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>createWriteStream (path, options)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.createWriteStream)
- description and source-code
```javascript
createWriteStream = function (path, options) {
	var stream = new WritableStream(), self = this;
	try {
		// Zero the file and make sure it is writable
		this.writeFileSync(path, new Buffer(0));
	} catch(e) {
		// This or setImmediate?
		stream.once('prefinish', function() {
			stream.emit('error', e);
		});
		return stream;
	}
	var bl = [ ], len = 0;
	stream._write = function(chunk, encoding, callback) {
		bl.push(chunk);
		len += chunk.length;
		self.writeFile(path, Buffer.concat(bl, len), callback);
	}
	return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.exists"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>exists (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.exists)
- description and source-code
```javascript
exists = function (path, callback) {
	return callback(this.existsSync(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.existsSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>existsSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.existsSync)
- description and source-code
```javascript
existsSync = function (_path) {
	return !!this.meta(_path);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.join"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>join (path, request)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.join)
- description and source-code
```javascript
function join(path, request) {
	if(!request) return normalize(path);
	if(absoluteWinRegExp.test(request)) return normalize(request.replace(/\//g, "\\"));
	if(absoluteNixRegExp.test(request)) return normalize(request);
	if(path == "/") return normalize(path + request);
	if(absoluteWinRegExp.test(path)) return normalize(path.replace(/\//g, "\\") + "\\" + request.replace(/\//g, "\\"));
	if(absoluteNixRegExp.test(path)) return normalize(path + "/" + request);
	return normalize(path + "/" + request);
}
```
- example usage
```shell
...
		compilation.templatesPlugin("render-with-entry", (source, chunk, hash) => {
			const externals = chunk.modules.filter((m) => m.external);
			const externalsDepsArray = JSON.stringify(externals.map((m) =>
				typeof m.request === "object" ? m.request.amd : m.request
			));
			const externalsArguments = externals.map((m) =>
				Template.toIdentifier('__WEBPACK_EXTERNAL_MODULE_${m.id}__')
			).join(", ");

			if(this.name) {
				const name = mainTemplate.applyPluginsWaterfall("asset-path", this.name, {
					hash,
					chunk
				});
...
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.meta"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>meta (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.meta)
- description and source-code
```javascript
meta = function (_path) {
	var path = pathToArray(_path);
	var current = this.data;
	for(var i = 0; i < path.length - 1; i++) {
		if(!isDir(current[path[i]]))
			return;
		current = current[path[i]];
	}
	return current[path[i]];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdir"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdir (path, optArg, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdir)
- description and source-code
```javascript
mkdir = function (path, optArg, callback) {
		if(!callback) {
			callback = optArg;
			optArg = undefined;
		}
		try {
			var result = this[fn + "Sync"](path, optArg);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdirSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirSync)
- description and source-code
```javascript
mkdirSync = function (_path) {
	var path = pathToArray(_path);
	if(path.length === 0) return;
	var current = this.data;
	for(var i = 0; i < path.length - 1; i++) {
		if(!isDir(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.ENOENT, _path);
		current = current[path[i]];
	}
	if(isDir(current[path[i]]))
		throw new MemoryFileSystemError(errors.code.EEXIST, _path);
	else if(isFile(current[path[i]]))
		throw new MemoryFileSystemError(errors.code.ENOTDIR, _path);
	current[path[i]] = {"":true};
	return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirp"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdirp (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirp)
- description and source-code
```javascript
mkdirp = function (path, callback) {
		try {
			var result = this[fn + "Sync"](path);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirpSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>mkdirpSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.mkdirpSync)
- description and source-code
```javascript
mkdirpSync = function (_path) {
	var path = pathToArray(_path);
	if(path.length === 0) return;
	var current = this.data;
	for(var i = 0; i < path.length; i++) {
		if(isFile(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.ENOTDIR, _path);
		else if(!isDir(current[path[i]]))
			current[path[i]] = {"":true};
		current = current[path[i]];
	}
	return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.normalize"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>normalize (path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.normalize)
- description and source-code
```javascript
function normalize(path) {
	var parts = path.split(/(\\+|\/+)/);
	if(parts.length === 1)
		return path;
	var result = [];
	var absolutePathStart = 0;
	for(var i = 0, sep = false; i < parts.length; i++, sep = !sep) {
		var part = parts[i];
		if(i === 0 && /^([A-Z]:)?$/i.test(part)) {
			result.push(part);
			absolutePathStart = 2;
		} else if(sep) {
			result.push(part[0]);
		} else if(part === "..") {
			switch(result.length) {
				case 0:
					// i. e. ".." => ".."
					// i. e. "../a/b/c" => "../a/b/c"
					result.push(part);
					break;
				case 2:
					// i. e. "a/.." => ""
					// i. e. "/.." => "/"
					// i. e. "C:\.." => "C:\"
					// i. e. "a/../b/c" => "b/c"
					// i. e. "/../b/c" => "/b/c"
					// i. e. "C:\..\a\b\c" => "C:\a\b\c"
					i++;
					sep = !sep;
					result.length = absolutePathStart;
					break;
				case 4:
					// i. e. "a/b/.." => "a"
					// i. e. "/a/.." => "/"
					// i. e. "C:\a\.." => "C:\"
					// i. e. "/a/../b/c" => "/b/c"
					if(absolutePathStart === 0) {
						result.length -= 3;
					} else {
						i++;
						sep = !sep;
						result.length = 2;
					}
					break;
				default:
					// i. e. "/a/b/.." => "/a"
					// i. e. "/a/b/../c" => "/a/c"
					result.length -= 3;
					break;
			}
		} else if(part === ".") {
			switch(result.length) {
				case 0:
					// i. e. "." => "."
					// i. e. "./a/b/c" => "./a/b/c"
					result.push(part);
					break;
				case 2:
					// i. e. "a/." => "a"
					// i. e. "/." => "/"
					// i. e. "C:\." => "C:\"
					// i. e. "C:\.\a\b\c" => "C:\a\b\c"
					if(absolutePathStart === 0) {
						result.length--;
					} else {
						i++;
						sep = !sep;
					}
					break;
				default:
					// i. e. "a/b/." => "a/b"
					// i. e. "/a/." => "/"
					// i. e. "C:\a\." => "C:\"
					// i. e. "a/./b/c" => "a/b/c"
					// i. e. "/a/./b/c" => "/a/b/c"
					result.length--;
					break;
			}
		} else if(part) {
			result.push(part);
		}
	}
	if(result.length === 1 && /^[A-Za-z]:$/.test(result))
		return result[0] + "\\";
	return result.join("");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.pathToArray"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>pathToArray (path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.pathToArray)
- description and source-code
```javascript
function pathToArray(path) {
	path = normalize(path);
	var nix = /^\//.test(path);
	if(!nix) {
		if(!/^[A-Za-z]:/.test(path)) {
			throw new MemoryFileSystemError(errors.code.EINVAL, path);
		}
		path = path.replace(/[\\\/]+/g, "\\"); // multi slashs
		path = path.split(/[\\\/]/);
		path[0] = path[0].toUpperCase();
	} else {
		path = path.replace(/\/+/g, "/"); // multi slashs
		path = path.substr(1).split("/");
	}
	if(!path[path.length-1]) path.pop();
	return path;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.readFile"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readFile (path, optArg, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readFile)
- description and source-code
```javascript
readFile = function (path, optArg, callback) {
		if(!callback) {
			callback = optArg;
			optArg = undefined;
		}
		try {
			var result = this[fn + "Sync"](path, optArg);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
...
			compilation.dependencyFactories.set(DelegatedSourceDependency, normalModuleFactory);
		});

		compiler.plugin("before-compile", (params, callback) => {
			const manifest = this.options.manifest;
			if(typeof manifest === "string") {
				params.compilationDependencies.push(manifest);
				compiler.inputFileSystem.readFile(manifest, function(err, result) {
					if(err) return callback(err);
					params["dll reference " + manifest] = JSON.parse(result.toString("utf-8"));
					return callback();
				});
			} else {
				return callback();
			}
...
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.readFileSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readFileSync (_path, encoding)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readFileSync)
- description and source-code
```javascript
readFileSync = function (_path, encoding) {
	var path = pathToArray(_path);
	var current = this.data;
	for(var i = 0; i < path.length - 1; i++) {
		if(!isDir(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.ENOENT, _path);
		current = current[path[i]];
	}
	if(!isFile(current[path[i]])) {
		if(isDir(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.EISDIR, _path);
		else
			throw new MemoryFileSystemError(errors.code.ENOENT, _path);
	}
	current = current[path[i]];
	return encoding ? current.toString(encoding) : current;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.readdir"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readdir (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readdir)
- description and source-code
```javascript
readdir = function (path, callback) {
		try {
			var result = this[fn + "Sync"](path);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
...
	});
};

ContextModuleFactory.prototype.resolveDependencies = function resolveDependencies(fs, resource, recursive, regExp, callback) {
	if(!regExp || !resource)
		return callback(null, []);
	(function addDirectory(directory, callback) {
		fs.readdir(directory, function(err, files) {
			if(err) return callback(err);
			if(!files || files.length === 0) return callback(null, []);
			async.map(files.filter(function(p) {
				return p.indexOf(".") !== 0;
			}), function(seqment, callback) {

				var subResource = path.join(directory, seqment);
...
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.readdirSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readdirSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readdirSync)
- description and source-code
```javascript
readdirSync = function (_path) {
	if(_path === "/") return Object.keys(this.data).filter(Boolean);
	var path = pathToArray(_path);
	var current = this.data;
	for(var i = 0; i < path.length - 1; i++) {
		if(!isDir(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.ENOENT, _path);
		current = current[path[i]];
	}
	if(!isDir(current[path[i]])) {
		if(isFile(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.ENOTDIR, _path);
		else
			throw new MemoryFileSystemError(errors.code.ENOENT, _path);
	}
	return Object.keys(current[path[i]]).filter(Boolean);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.readlink"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readlink (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readlink)
- description and source-code
```javascript
readlink = function (path, callback) {
		try {
			var result = this[fn + "Sync"](path);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.readlinkSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>readlinkSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.readlinkSync)
- description and source-code
```javascript
readlinkSync = function (_path) {
	throw new MemoryFileSystemError(errors.code.ENOSYS, _path);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.rmdir"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>rmdir (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.rmdir)
- description and source-code
```javascript
rmdir = function (path, callback) {
		try {
			var result = this[fn + "Sync"](path);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.rmdirSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>rmdirSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.rmdirSync)
- description and source-code
```javascript
rmdirSync = function (_path) {
	return this._remove(_path, "Directory", isDir);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.stat"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>stat (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.stat)
- description and source-code
```javascript
stat = function (path, callback) {
		try {
			var result = this[fn + "Sync"](path);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
...
				callback();
			});
			compiler.plugin("run", (compiler, callback) => {
				if(!compiler._lastCompilationFileDependencies) return callback();
				const fs = compiler.inputFileSystem;
				const fileTs = compiler.fileTimestamps = {};
				async.forEach(compiler._lastCompilationFileDependencies, (file, callback) => {
					fs.stat(file, (err, stat) => {
						if(err) {
							if(err.code === "ENOENT") return callback();
							return callback(err);
						}

						if(stat.mtime)
							this.applyMtime(+stat.mtime);
...
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.statSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>statSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.statSync)
- description and source-code
```javascript
statSync = function (_path) {
	var current = this.meta(_path);
	if(_path === "/" || isDir(current)) {
		return {
			isFile: falseFn,
			isDirectory: trueFn,
			isBlockDevice: falseFn,
			isCharacterDevice: falseFn,
			isSymbolicLink: falseFn,
			isFIFO: falseFn,
			isSocket: falseFn
		};
	} else if(isFile(current)) {
		return {
			isFile: trueFn,
			isDirectory: falseFn,
			isBlockDevice: falseFn,
			isCharacterDevice: falseFn,
			isSymbolicLink: falseFn,
			isFIFO: falseFn,
			isSocket: falseFn
		};
	} else {
		throw new MemoryFileSystemError(errors.code.ENOENT, _path);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.unlink"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>unlink (path, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.unlink)
- description and source-code
```javascript
unlink = function (path, callback) {
		try {
			var result = this[fn + "Sync"](path);
		} catch(e) {
			setImmediate(function() {
				callback(e);
			});

			return;
		}
		setImmediate(function() {
			callback(null, result);
		});
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.unlinkSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>unlinkSync (_path)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.unlinkSync)
- description and source-code
```javascript
unlinkSync = function (_path) {
	return this._remove(_path, "File", isFile);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.writeFile"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>writeFile (path, content, encoding, callback)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.writeFile)
- description and source-code
```javascript
writeFile = function (path, content, encoding, callback) {
	if(!callback) {
		callback = encoding;
		encoding = undefined;
	}
	try {
		this.writeFileSync(path, content, encoding);
	} catch(e) {
		return callback(e);
	}
	return callback();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MemoryOutputFileSystem.prototype.writeFileSync"></a>[function <span class="apidocSignatureSpan">webpack.MemoryOutputFileSystem.prototype.</span>writeFileSync (_path, content, encoding)](#apidoc.element.webpack.MemoryOutputFileSystem.prototype.writeFileSync)
- description and source-code
```javascript
writeFileSync = function (_path, content, encoding) {
	if(!content && !encoding) throw new Error("No content");
	var path = pathToArray(_path);
	if(path.length === 0) {
		throw new MemoryFileSystemError(errors.code.EISDIR, _path);
	}
	var current = this.data;
	for(var i = 0; i < path.length - 1; i++) {
		if(!isDir(current[path[i]]))
			throw new MemoryFileSystemError(errors.code.ENOENT, _path);
		current = current[path[i]];
	}
	if(isDir(current[path[i]]))
		throw new MemoryFileSystemError(errors.code.EISDIR, _path);
	current[path[i]] = encoding || typeof content === "string" ? new Buffer(content, encoding) : content;
	return;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.Module"></a>[module webpack.Module](#apidoc.module.webpack.Module)

#### <a name="apidoc.element.webpack.Module.Module"></a>[function <span class="apidocSignatureSpan">webpack.</span>Module ()](#apidoc.element.webpack.Module.Module)
- description and source-code
```javascript
function Module() {
	DependenciesBlock.call(this);
	this.context = null;
	this.reasons = [];
	this.debugId = debugId++;
	this.lastId = -1;
	this.id = null;
	this.portableId = null;
	this.index = null;
	this.index2 = null;
	this.depth = null;
	this.used = null;
	this.usedExports = null;
	this.providedExports = null;
	this.chunks = [];
	this.warnings = [];
	this.dependenciesWarnings = [];
	this.errors = [];
	this.dependenciesErrors = [];
	this.strict = false;
	this.meta = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.Module.prototype"></a>[module webpack.Module.prototype](#apidoc.module.webpack.Module.prototype)

#### <a name="apidoc.element.webpack.Module.prototype.addChunk"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>addChunk (chunk)](#apidoc.element.webpack.Module.prototype.addChunk)
- description and source-code
```javascript
addChunk = function (chunk) {
	var idx = this.chunks.indexOf(chunk);
	if(idx < 0)
		this.chunks.push(chunk);
}
```
- example usage
```shell
...
				/**
				 * remove this chunk as "intermediary" and connect
				 * it "sub chunks" and parents directly
				 */
				// add parent to each "sub chunk"
				chunk.addParent(parentChunk);
				// add "sub chunk" to parent
				parentChunk.addChunk(chunk);
			});
		});

		/**
		 * we need to iterate again over the chunks
		 * to remove this from the chunks parents.
		 * This can not be done in the above loop
...
```

#### <a name="apidoc.element.webpack.Module.prototype.addReason"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>addReason (module, dependency)](#apidoc.element.webpack.Module.prototype.addReason)
- description and source-code
```javascript
addReason = function (module, dependency) {
	this.reasons.push(new ModuleReason(module, dependency));
}
```
- example usage
```shell
...
					}
				}

				function iterationDependencies(depend) {
					for(let index = 0; index < depend.length; index++) {
						const dep = depend[index];
						dep.module = dependentModule;
						dependentModule.addReason(module, dep);
					}
				}

				if(err) {
					return errorOrWarningAndCallback(new ModuleNotFoundError(module, err, dependencies));
				}
				if(!dependentModule) {
...
```

#### <a name="apidoc.element.webpack.Module.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>constructor ()](#apidoc.element.webpack.Module.prototype.constructor)
- description and source-code
```javascript
function Module() {
	DependenciesBlock.call(this);
	this.context = null;
	this.reasons = [];
	this.debugId = debugId++;
	this.lastId = -1;
	this.id = null;
	this.portableId = null;
	this.index = null;
	this.index2 = null;
	this.depth = null;
	this.used = null;
	this.usedExports = null;
	this.providedExports = null;
	this.chunks = [];
	this.warnings = [];
	this.dependenciesWarnings = [];
	this.errors = [];
	this.dependenciesErrors = [];
	this.strict = false;
	this.meta = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Module.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>disconnect ()](#apidoc.element.webpack.Module.prototype.disconnect)
- description and source-code
```javascript
disconnect = function () {
	this.reasons.length = 0;
	this.lastId = this.id;
	this.id = null;
	this.index = null;
	this.index2 = null;
	this.depth = null;
	this.used = null;
	this.usedExports = null;
	this.providedExports = null;
	this.chunks.length = 0;
	DependenciesBlock.prototype.disconnect.call(this);
}
```
- example usage
```shell
...
		hash.update(this.chunks && this.chunks.map((chunk) => {
			return typeof chunk.id === "number" ? chunk.id : "";
		}).join(",") || "");
		super.updateHash(hash);
	}
	disconnect() {
		this.chunks = null;
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
		super.unseal();
	}
	sortItems() {
		super.sortItems();
...
```

#### <a name="apidoc.element.webpack.Module.prototype.hasReasonForChunk"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>hasReasonForChunk (chunk)](#apidoc.element.webpack.Module.prototype.hasReasonForChunk)
- description and source-code
```javascript
hasReasonForChunk = function (chunk) {
	for(var i = 0; i < this.reasons.length; i++) {
		var r = this.reasons[i];
		if(r.chunks) {
			if(r.chunks.indexOf(chunk) >= 0)
				return true;
		} else if(r.module.chunks.indexOf(chunk) >= 0)
			return true;
	}
	return false;
}
```
- example usage
```shell
...
			if(err) return callback(err);

			this.processModuleDependencies(module, (err) => {
				if(err) return callback(err);
				deps.forEach(d => {
					if(d.module && d.module.removeReason(module, d)) {
						module.chunks.forEach(chunk => {
							if(!d.module.hasReasonForChunk(chunk)) {
								if(d.module.removeChunk(chunk)) {
									this.removeChunkFromDependencies(d.module, chunk);
								}
							}
						});
					}
				});
...
```

#### <a name="apidoc.element.webpack.Module.prototype.isProvided"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>isProvided (exportName)](#apidoc.element.webpack.Module.prototype.isProvided)
- description and source-code
```javascript
isProvided = function (exportName) {
	if(!Array.isArray(this.providedExports))
		return null;
	return this.providedExports.indexOf(exportName) >= 0;
}
```
- example usage
```shell
...
	if(this.used === null) return exportName;
	if(!exportName) return this.used ? true : false;
	if(!this.used) return false;
	if(!this.usedExports) return false;
	if(this.usedExports === true) return exportName;
	var idx = this.usedExports.indexOf(exportName);
	if(idx < 0) return false;
	if(this.isProvided(exportName))
		return Template.numberToIdentifer(idx);
	return exportName;
};

Module.prototype.isProvided = function(exportName) {
	if(!Array.isArray(this.providedExports))
		return null;
...
```

#### <a name="apidoc.element.webpack.Module.prototype.isUsed"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>isUsed (exportName)](#apidoc.element.webpack.Module.prototype.isUsed)
- description and source-code
```javascript
isUsed = function (exportName) {
	if(this.used === null) return exportName;
	if(!exportName) return this.used ? true : false;
	if(!this.used) return false;
	if(!this.usedExports) return false;
	if(this.usedExports === true) return exportName;
	var idx = this.usedExports.indexOf(exportName);
	if(idx < 0) return false;
	if(this.isProvided(exportName))
		return Template.numberToIdentifer(idx);
	return exportName;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Module.prototype.needRebuild"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>needRebuild (fileTimestamps, contextTimestamps)](#apidoc.element.webpack.Module.prototype.needRebuild)
- description and source-code
```javascript
needRebuild = function (fileTimestamps, contextTimestamps) {
	return true;
}
```
- example usage
```shell
...
		}
		const cacheName = (cacheGroup || "m") + identifier;
		if(this.cache && this.cache[cacheName]) {
			const cacheModule = this.cache[cacheName];

			let rebuild = true;
			if(!cacheModule.error && cacheModule.cacheable && this.fileTimestamps && this.contextTimestamps) {
				rebuild = cacheModule.needRebuild(this.fileTimestamps, this.contextTimestamps);
			}

			if(!rebuild) {
				cacheModule.disconnect();
				this._modules[identifier] = cacheModule;
				this.modules.push(cacheModule);
				cacheModule.errors.forEach(err => this.errors.push(err), this);
...
```

#### <a name="apidoc.element.webpack.Module.prototype.removeChunk"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>removeChunk (chunk)](#apidoc.element.webpack.Module.prototype.removeChunk)
- description and source-code
```javascript
removeChunk = function (chunk) {
	var idx = this.chunks.indexOf(chunk);
	if(idx >= 0) {
		this.chunks.splice(idx, 1);
		chunk.removeModule(this);
		return true;
	}
	return false;
}
```
- example usage
```shell
...
		return this.addToCollection(this.blocks, block);
	}

	removeModule(module) {
		const idx = this.modules.indexOf(module);
		if(idx >= 0) {
			this.modules.splice(idx, 1);
			module.removeChunk(this);
			return true;
		}
		return false;
	}

	removeChunk(chunk) {
		const idx = this.chunks.indexOf(chunk);
...
```

#### <a name="apidoc.element.webpack.Module.prototype.removeReason"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>removeReason (module, dependency)](#apidoc.element.webpack.Module.prototype.removeReason)
- description and source-code
```javascript
removeReason = function (module, dependency) {
	for(var i = 0; i < this.reasons.length; i++) {
		var r = this.reasons[i];
		if(r.module === module && r.dependency === dependency) {
			this.reasons.splice(i, 1);
			return true;
		}
	}
	return false;
}
```
- example usage
```shell
...
		const deps = module.dependencies.slice();
		this.buildModule(module, false, module, null, (err) => {
			if(err) return callback(err);

			this.processModuleDependencies(module, (err) => {
				if(err) return callback(err);
				deps.forEach(d => {
					if(d.module && d.module.removeReason(module, d)) {
						module.chunks.forEach(chunk => {
							if(!d.module.hasReasonForChunk(chunk)) {
								if(d.module.removeChunk(chunk)) {
									this.removeChunkFromDependencies(d.module, chunk);
								}
							}
						});
...
```

#### <a name="apidoc.element.webpack.Module.prototype.rewriteChunkInReasons"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>rewriteChunkInReasons (oldChunk, newChunks)](#apidoc.element.webpack.Module.prototype.rewriteChunkInReasons)
- description and source-code
```javascript
rewriteChunkInReasons = function (oldChunk, newChunks) {
	this.reasons.forEach(function(r) {
		if(!r.chunks) {
			if(r.module.chunks.indexOf(oldChunk) < 0)
				return;
			r.chunks = r.module.chunks;
		}
		r.chunks = r.chunks.reduce(function(arr, c) {
			addToSet(arr, c !== oldChunk ? [c] : newChunks);
			return arr;
		}, []);
	});
}
```
- example usage
```shell
...
		});
	}

	moveModule(module, otherChunk) {
		module.removeChunk(this);
		module.addChunk(otherChunk);
		otherChunk.addModule(module);
		module.rewriteChunkInReasons(this, [otherChunk]);
	}

	replaceChunk(oldChunk, newChunk) {
		const idx = this.chunks.indexOf(oldChunk);
		if(idx >= 0) {
			this.chunks.splice(idx, 1);
		}
...
```

#### <a name="apidoc.element.webpack.Module.prototype.sortItems"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>sortItems ()](#apidoc.element.webpack.Module.prototype.sortItems)
- description and source-code
```javascript
sortItems = function () {
	DependenciesBlock.prototype.sortItems.call(this);
	this.chunks.sort(byId);
	this.reasons.sort(function(a, b) {
		return byId(a.module, b.module);
	});
}
```
- example usage
```shell
...
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
		super.unseal();
	}
	sortItems() {
		super.sortItems();
		if(this.chunks) {
			this.chunks.sort((a, b) => {
				let i = 0;
				while(true) { // eslint-disable-line no-constant-condition
					if(!a.modules[i] && !b.modules[i]) return 0;
					if(!a.modules[i]) return -1;
					if(!b.modules[i]) return 1;
...
```

#### <a name="apidoc.element.webpack.Module.prototype.toString"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>toString ()](#apidoc.element.webpack.Module.prototype.toString)
- description and source-code
```javascript
toString = function () {
	return "Module[" + (this.id || this.debugId) + "]";
}
```
- example usage
```shell
...
						return JSON.stringify(key) + ":" + toCode(code);
					}).join(",") + "})";
				}

				function toCode(code) {
					if(code === null) return "null";
					else if(code === undefined) return "undefined";
					else if(code instanceof RegExp && code.toString) return code.toString();
					else if(typeof code === "function" && code.toString) return "(" + code.toString() + ")";
					else if(typeof code === "object") return stringifyObj(code);
					else return code + "";
				}

				function applyDefineKey(prefix, key) {
					const splittedKey = key.split(".");
...
```

#### <a name="apidoc.element.webpack.Module.prototype.unbuild"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>unbuild ()](#apidoc.element.webpack.Module.prototype.unbuild)
- description and source-code
```javascript
unbuild = function () {
	this.disconnect();
}
```
- example usage
```shell
...
				cacheModule.errors.forEach(err => this.errors.push(err), this);
				cacheModule.warnings.forEach(err => this.warnings.push(err), this);
				return cacheModule;
			} else {
				module.lastId = cacheModule.id;
			}
		}
		module.unbuild();
		this._modules[identifier] = module;
		if(this.cache) {
			this.cache[cacheName] = module;
		}
		this.modules.push(module);
		return true;
	}
...
```

#### <a name="apidoc.element.webpack.Module.prototype.unseal"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>unseal ()](#apidoc.element.webpack.Module.prototype.unseal)
- description and source-code
```javascript
unseal = function () {
	this.lastId = this.id;
	this.id = null;
	this.index = null;
	this.index2 = null;
	this.depth = null;
	this.chunks.length = 0;
	DependenciesBlock.prototype.unseal.call(this);
}
```
- example usage
```shell
...
	}
	disconnect() {
		this.chunks = null;
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
		super.unseal();
	}
	sortItems() {
		super.sortItems();
		if(this.chunks) {
			this.chunks.sort((a, b) => {
				let i = 0;
				while(true) { // eslint-disable-line no-constant-condition
...
```

#### <a name="apidoc.element.webpack.Module.prototype.updateHash"></a>[function <span class="apidocSignatureSpan">webpack.Module.prototype.</span>updateHash (hash)](#apidoc.element.webpack.Module.prototype.updateHash)
- description and source-code
```javascript
updateHash = function (hash) {
	hash.update(this.id + "" + this.used);
	hash.update(JSON.stringify(this.usedExports));
	DependenciesBlock.prototype.updateHash.call(this, hash);
}
```
- example usage
```shell
...
		throw new Error("'chunk' was been renamed to 'chunks' and is now an array");
	}
	updateHash(hash) {
		hash.update(this.chunkName || "");
		hash.update(this.chunks && this.chunks.map((chunk) => {
			return typeof chunk.id === "number" ? chunk.id : "";
		}).join(",") || "");
		super.updateHash(hash);
	}
	disconnect() {
		this.chunks = null;
		super.disconnect();
	}
	unseal() {
		this.chunks = null;
...
```



# <a name="apidoc.module.webpack.ModuleFilenameHelpers"></a>[module webpack.ModuleFilenameHelpers](#apidoc.module.webpack.ModuleFilenameHelpers)

#### <a name="apidoc.element.webpack.ModuleFilenameHelpers.createFilename"></a>[function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>createFilename (module, moduleFilenameTemplate, requestShortener)](#apidoc.element.webpack.ModuleFilenameHelpers.createFilename)
- description and source-code
```javascript
function createFilename(module, moduleFilenameTemplate, requestShortener) {
	var absoluteResourcePath;
	var hash;
	var identifier;
	var moduleId;
	var shortIdentifier;
	if(!module) module = "";
	if(typeof module === "string") {
		shortIdentifier = requestShortener.shorten(module);
		identifier = shortIdentifier;
		moduleId = "";
		absoluteResourcePath = module.split("!").pop();
		hash = getHash(identifier);
	} else {
		shortIdentifier = module.readableIdentifier(requestShortener);
		identifier = requestShortener.shorten(module.identifier());
		moduleId = module.id;
		absoluteResourcePath = module.resourcePath || module.identifier().split("!").pop();
		hash = getHash(identifier);
	}
	var resource = shortIdentifier.split("!").pop();
	var loaders = getBefore(shortIdentifier, "!");
	var allLoaders = getBefore(identifier, "!");
	var query = getAfter(resource, "?");
	var resourcePath = resource.substr(0, resource.length - query.length);
	if(typeof moduleFilenameTemplate === "function") {
		return moduleFilenameTemplate({
			identifier: identifier,
			shortIdentifier: shortIdentifier,
			resource: resource,
			resourcePath: resourcePath,
			absoluteResourcePath: absoluteResourcePath,
			allLoaders: allLoaders,
			query: query,
			moduleId: moduleId,
			hash: hash
		});
	}
	return moduleFilenameTemplate
		.replace(ModuleFilenameHelpers.REGEXP_ALL_LOADERS_RESOURCE, identifier)
		.replace(ModuleFilenameHelpers.REGEXP_LOADERS_RESOURCE, shortIdentifier)
		.replace(ModuleFilenameHelpers.REGEXP_RESOURCE, resource)
		.replace(ModuleFilenameHelpers.REGEXP_RESOURCE_PATH, resourcePath)
		.replace(ModuleFilenameHelpers.REGEXP_ABSOLUTE_RESOURCE_PATH, absoluteResourcePath)
		.replace(ModuleFilenameHelpers.REGEXP_ALL_LOADERS, allLoaders)
		.replace(ModuleFilenameHelpers.REGEXP_LOADERS, loaders)
		.replace(ModuleFilenameHelpers.REGEXP_QUERY, query)
		.replace(ModuleFilenameHelpers.REGEXP_ID, moduleId)
		.replace(ModuleFilenameHelpers.REGEXP_HASH, hash);
}
```
- example usage
```shell
...
		this.sourceUrlComment = sourceUrlComment || "\n//# sourceURL=[url]";
		this.moduleFilenameTemplate = moduleFilenameTemplate || "webpack:///[resourcePath]?[loaders]";
	}

	apply(moduleTemplate) {
		moduleTemplate.plugin("module", (source, module) => {
			const content = source.source();
			const str = ModuleFilenameHelpers.createFilename(module, this.moduleFilenameTemplate, moduleTemplate.requestShortener);
			const footer = ["\n",
				ModuleFilenameHelpers.createFooter(module, moduleTemplate.requestShortener),
				this.sourceUrlComment.replace(/\[url\]/g, encodeURI(str).replace(/%2F/g, "/").replace(/%20/g, "_").replace(/%5E/g, "^").replace
(/%5C/g, "\\").replace(/^\//, ""))
			].join("\n");
			return new RawSource('eval(${JSON.stringify(content + footer)});');
		});
		moduleTemplate.plugin("hash", hash => {
...
```

#### <a name="apidoc.element.webpack.ModuleFilenameHelpers.createFooter"></a>[function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>createFooter (module, requestShortener)](#apidoc.element.webpack.ModuleFilenameHelpers.createFooter)
- description and source-code
```javascript
function createFooter(module, requestShortener) {
	if(!module) module = "";
	if(typeof module === "string") {
		return [
			"// WEBPACK FOOTER //",
			"// " + requestShortener.shorten(module)
		].join("\n");
	} else {
		return [
			"//////////////////",
			"// WEBPACK FOOTER",
			"// " + module.readableIdentifier(requestShortener),
			"// module id = " + module.id,
			"// module chunks = " + module.chunks.map(function(c) {
				return c.id;
			}).join(" ")
		].join("\n");
	}
}
```
- example usage
```shell
...
	}

	apply(moduleTemplate) {
		moduleTemplate.plugin("module", (source, module) => {
			const content = source.source();
			const str = ModuleFilenameHelpers.createFilename(module, this.moduleFilenameTemplate, moduleTemplate.requestShortener);
			const footer = ["\n",
				ModuleFilenameHelpers.createFooter(module, moduleTemplate.requestShortener),
				this.sourceUrlComment.replace(/\[url\]/g, encodeURI(str).replace(/%2F/g, "/").replace(/%20/g, "_").replace(/%5E/g, "^").replace
(/%5C/g, "\\").replace(/^\//, ""))
			].join("\n");
			return new RawSource('eval(${JSON.stringify(content + footer)});');
		});
		moduleTemplate.plugin("hash", hash => {
			hash.update("EvalDevToolModuleTemplatePlugin");
			hash.update("2");
...
```

#### <a name="apidoc.element.webpack.ModuleFilenameHelpers.matchObject"></a>[function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>matchObject (obj, str)](#apidoc.element.webpack.ModuleFilenameHelpers.matchObject)
- description and source-code
```javascript
function matchObject(obj, str) {
	if(obj.test)
		if(!ModuleFilenameHelpers.matchPart(str, obj.test)) return false;
	if(obj.include)
		if(!ModuleFilenameHelpers.matchPart(str, obj.include)) return false;
	if(obj.exclude)
		if(ModuleFilenameHelpers.matchPart(str, obj.exclude)) return false;
	return true;
}
```
- example usage
```shell
...
	apply(compiler) {
		const options = this.options;
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("normal-module-loader", (context, module) => {
				const resource = module.resource;
				if(!resource) return;
				const i = resource.indexOf("?");
				if(ModuleFilenameHelpers.matchObject(options, i < 0 ? resource : resource.substr(0, i))) {
					const filterSet = new Set(["include", "exclude", "test"]);
					Object.keys(options)
						.filter((key) => !filterSet.has(key))
						.forEach((key) => context[key] = options[key]);
				}
			});
		});
...
```

#### <a name="apidoc.element.webpack.ModuleFilenameHelpers.matchPart"></a>[function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>matchPart (str, test)](#apidoc.element.webpack.ModuleFilenameHelpers.matchPart)
- description and source-code
```javascript
function matchPart(str, test) {
	if(!test) return true;
	test = asRegExp(test);
	if(Array.isArray(test)) {
		return test.map(asRegExp).filter(function(regExp) {
			return regExp.test(str);
		}).length > 0;
	} else {
		return test.test(str);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ModuleFilenameHelpers.replaceDuplicates"></a>[function <span class="apidocSignatureSpan">webpack.ModuleFilenameHelpers.</span>replaceDuplicates (array, fn, comparator)](#apidoc.element.webpack.ModuleFilenameHelpers.replaceDuplicates)
- description and source-code
```javascript
function replaceDuplicates(array, fn, comparator) {
	var countMap = {};
	var posMap = {};
	array.forEach(function(item, idx) {
		countMap[item] = (countMap[item] || []);
		countMap[item].push(idx);
		posMap[item] = 0;
	});
	if(comparator) {
		Object.keys(countMap).forEach(function(item) {
			countMap[item].sort(comparator);
		});
	}
	return array.map(function(item, i) {
		if(countMap[item].length > 1) {
			if(comparator && countMap[item][0] === i)
				return item;
			return fn(item, i, posMap[item]++);
		} else return item;
	});
}
```
- example usage
```shell
...
			const modules = sourceMap.sources.map(function(source) {
				const module = self.compilation.findModule(source);
				return module || source;
			});
			let moduleFilenames = modules.map(function(module) {
				return ModuleFilenameHelpers.createFilename(module, self.moduleFilenameTemplate, this.requestShortener);
			}, this);
			moduleFilenames = ModuleFilenameHelpers.replaceDuplicates(moduleFilenames, function(filename, i, n) {
				for(let j = 0; j < n; j++)
					filename += "*";
				return filename;
			});
			sourceMap.sources = moduleFilenames;
			if(sourceMap.sourcesContent) {
				sourceMap.sourcesContent = sourceMap.sourcesContent.map(function(content, i) {
...
```



# <a name="apidoc.module.webpack.MultiCompiler"></a>[module webpack.MultiCompiler](#apidoc.module.webpack.MultiCompiler)

#### <a name="apidoc.element.webpack.MultiCompiler.MultiCompiler"></a>[function <span class="apidocSignatureSpan">webpack.</span>MultiCompiler (compilers)](#apidoc.element.webpack.MultiCompiler.MultiCompiler)
- description and source-code
```javascript
function MultiCompiler(compilers) {
	Tapable.call(this);
	if(!Array.isArray(compilers)) {
		compilers = Object.keys(compilers).map(function(name) {
			compilers[name].name = name;
			return compilers[name];
		});
	}
	this.compilers = compilers;

	function delegateProperty(name) {
		Object.defineProperty(this, name, {
			configurable: false,
			get: function() {
				throw new Error("Cannot read " + name + " of a MultiCompiler");
			},
			set: function(value) {
				this.compilers.forEach(function(compiler) {
					compiler[name] = value;
				});
			}.bind(this)
		});
	}
	delegateProperty.call(this, "outputFileSystem");
	delegateProperty.call(this, "inputFileSystem");

	Object.defineProperty(this, "outputPath", {
		configurable: false,
		get: function() {
			var commonPath = compilers[0].outputPath;
			for(var i = 1; i < compilers.length; i++) {
				while(compilers[i].outputPath.indexOf(commonPath) !== 0 && /[\/\\]/.test(commonPath)) {
					commonPath = commonPath.replace(/[\/\\][^\/\\]*$/, "");
				}
			}
			if(!commonPath && compilers[0].outputPath[0] === "/") return "/";
			return commonPath;
		}
	});

	var doneCompilers = 0;
	var compilerStats = [];
	this.compilers.forEach(function(compiler, idx) {
		var compilerDone = false;
		compiler.plugin("done", function(stats) {
			if(!compilerDone) {
				compilerDone = true;
				doneCompilers++;
			}
			compilerStats[idx] = stats;
			if(doneCompilers === this.compilers.length) {
				this.applyPlugins("done", new MultiStats(compilerStats));
			}
		}.bind(this));
		compiler.plugin("invalid", function() {
			if(compilerDone) {
				compilerDone = false;
				doneCompilers--;
			}
			this.applyPlugins("invalid");
		}.bind(this));
	}, this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.MultiCompiler.prototype"></a>[module webpack.MultiCompiler.prototype](#apidoc.module.webpack.MultiCompiler.prototype)

#### <a name="apidoc.element.webpack.MultiCompiler.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>constructor (compilers)](#apidoc.element.webpack.MultiCompiler.prototype.constructor)
- description and source-code
```javascript
function MultiCompiler(compilers) {
	Tapable.call(this);
	if(!Array.isArray(compilers)) {
		compilers = Object.keys(compilers).map(function(name) {
			compilers[name].name = name;
			return compilers[name];
		});
	}
	this.compilers = compilers;

	function delegateProperty(name) {
		Object.defineProperty(this, name, {
			configurable: false,
			get: function() {
				throw new Error("Cannot read " + name + " of a MultiCompiler");
			},
			set: function(value) {
				this.compilers.forEach(function(compiler) {
					compiler[name] = value;
				});
			}.bind(this)
		});
	}
	delegateProperty.call(this, "outputFileSystem");
	delegateProperty.call(this, "inputFileSystem");

	Object.defineProperty(this, "outputPath", {
		configurable: false,
		get: function() {
			var commonPath = compilers[0].outputPath;
			for(var i = 1; i < compilers.length; i++) {
				while(compilers[i].outputPath.indexOf(commonPath) !== 0 && /[\/\\]/.test(commonPath)) {
					commonPath = commonPath.replace(/[\/\\][^\/\\]*$/, "");
				}
			}
			if(!commonPath && compilers[0].outputPath[0] === "/") return "/";
			return commonPath;
		}
	});

	var doneCompilers = 0;
	var compilerStats = [];
	this.compilers.forEach(function(compiler, idx) {
		var compilerDone = false;
		compiler.plugin("done", function(stats) {
			if(!compilerDone) {
				compilerDone = true;
				doneCompilers++;
			}
			compilerStats[idx] = stats;
			if(doneCompilers === this.compilers.length) {
				this.applyPlugins("done", new MultiStats(compilerStats));
			}
		}.bind(this));
		compiler.plugin("invalid", function() {
			if(compilerDone) {
				compilerDone = false;
				doneCompilers--;
			}
			this.applyPlugins("invalid");
		}.bind(this));
	}, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MultiCompiler.prototype.purgeInputFileSystem"></a>[function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>purgeInputFileSystem ()](#apidoc.element.webpack.MultiCompiler.prototype.purgeInputFileSystem)
- description and source-code
```javascript
purgeInputFileSystem = function () {
	this.compilers.forEach(function(compiler) {
		if(compiler.inputFileSystem && compiler.inputFileSystem.purge)
			compiler.inputFileSystem.purge();
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.MultiCompiler.prototype.run"></a>[function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>run (callback)](#apidoc.element.webpack.MultiCompiler.prototype.run)
- description and source-code
```javascript
run = function (callback) {
	var allStats = this.compilers.map(function() {
		return null;
	});

	runWithDependencies(this.compilers, function(compiler, callback) {
		var compilerIdx = this.compilers.indexOf(compiler);
		compiler.run(function(err, stats) {
			if(err) return callback(err);
			allStats[compilerIdx] = stats;
			callback();
		});
	}.bind(this), function(err) {
		if(err) return callback(err);
		callback(null, new MultiStats(allStats));
	});
}
```
- example usage
```shell
...
	new WebpackOptionsDefaulter().process(options);

	const compiler = new Compiler();
	compiler.options = options;
	compiler.options = new WebpackOptionsApply().process(options, compiler);
	new WebEnvironmentPlugin(options.inputFileSystem, options.outputFileSystem).apply(compiler);
	if(callback) {
		compiler.run(callback);
	}
	return compiler;
}
module.exports = webpack;

webpack.WebpackOptionsDefaulter = WebpackOptionsDefaulter;
webpack.WebpackOptionsApply = WebpackOptionsApply;
...
```

#### <a name="apidoc.element.webpack.MultiCompiler.prototype.watch"></a>[function <span class="apidocSignatureSpan">webpack.MultiCompiler.prototype.</span>watch (watchOptions, handler)](#apidoc.element.webpack.MultiCompiler.prototype.watch)
- description and source-code
```javascript
watch = function (watchOptions, handler) {
	var watchings = [];
	var allStats = this.compilers.map(function() {
		return null;
	});
	var compilerStatus = this.compilers.map(function() {
		return false;
	});

	runWithDependencies(this.compilers, function(compiler, callback) {
		var compilerIdx = this.compilers.indexOf(compiler);
		var firstRun = true;
		var watching = compiler.watch(watchOptions, function(err, stats) {
			if(err)
				handler(err);
			if(stats) {
				allStats[compilerIdx] = stats;
				compilerStatus[compilerIdx] = "new";
				if(compilerStatus.every(Boolean)) {
					var freshStats = allStats.filter(function(s, idx) {
						return compilerStatus[idx] === "new";
					});
					compilerStatus.fill(true);
					var multiStats = new MultiStats(freshStats);
					handler(null, multiStats);
				}
			}
			if(firstRun && !err) {
				firstRun = false;
				callback();
			}
		});
		watchings.push(watching);
	}.bind(this), function() {
		// ignore
	});

	return new MultiWatching(watchings, this);
}
```
- example usage
```shell
...
		const ignored = path => this.paths.some(p => p instanceof RegExp ? p.test(path) : path.indexOf(p) === 0);

		const notIgnored = path => !ignored(path);

		const ignoredFiles = files.filter(ignored);
		const ignoredDirs = dirs.filter(ignored);

		this.wfs.watch(files.filter(notIgnored), dirs.filter(notIgnored), missing, startTime, options, (err, filesModified, dirsModified
, missingModified, fileTimestamps, dirTimestamps) => {
			if(err) return callback(err);

			ignoredFiles.forEach(path => {
				fileTimestamps[path] = 1;
			});

			ignoredDirs.forEach(path => {
...
```



# <a name="apidoc.module.webpack.NodeStuffPlugin"></a>[module webpack.NodeStuffPlugin](#apidoc.module.webpack.NodeStuffPlugin)

#### <a name="apidoc.element.webpack.NodeStuffPlugin.NodeStuffPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>NodeStuffPlugin (options)](#apidoc.element.webpack.NodeStuffPlugin.NodeStuffPlugin)
- description and source-code
```javascript
function NodeStuffPlugin(options) {
	this.options = options;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.NodeStuffPlugin.prototype"></a>[module webpack.NodeStuffPlugin.prototype](#apidoc.module.webpack.NodeStuffPlugin.prototype)

#### <a name="apidoc.element.webpack.NodeStuffPlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.NodeStuffPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.NodeStuffPlugin.prototype.apply)
- description and source-code
```javascript
apply = function (compiler) {
	var options = this.options;
	compiler.plugin("compilation", function(compilation, params) {
		compilation.dependencyFactories.set(ConstDependency, new NullFactory());
		compilation.dependencyTemplates.set(ConstDependency, new ConstDependency.Template());

		params.normalModuleFactory.plugin("parser", function(parser, parserOptions) {

			if(parserOptions.node === false)
				return;

			var localOptions = options;
			if(parserOptions.node)
				localOptions = Object.assign({}, localOptions, parserOptions.node);

			function setConstant(expressionName, value) {
				parser.plugin("expression " + expressionName, function() {
					this.state.current.addVariable(expressionName, JSON.stringify(value));
					return true;
				});
			}

			function setModuleConstant(expressionName, fn) {
				parser.plugin("expression " + expressionName, function() {
					this.state.current.addVariable(expressionName, JSON.stringify(fn(this.state.module)));
					return true;
				});
			}
			var context = compiler.context;
			if(localOptions.__filename === "mock") {
				setConstant("__filename", "/index.js");
			} else if(localOptions.__filename) {
				setModuleConstant("__filename", function(module) {
					return path.relative(context, module.resource);
				});
			}
			parser.plugin("evaluate Identifier __filename", function(expr) {
				if(!this.state.module) return;
				var resource = this.state.module.resource;
				var i = resource.indexOf("?");
				return ParserHelpers.evaluateToString(i < 0 ? resource : resource.substr(0, i))(expr);
			});
			if(localOptions.__dirname === "mock") {
				setConstant("__dirname", "/");
			} else if(localOptions.__dirname) {
				setModuleConstant("__dirname", function(module) {
					return path.relative(context, module.context);
				});
			}
			parser.plugin("evaluate Identifier __dirname", function(expr) {
				if(!this.state.module) return;
				return ParserHelpers.evaluateToString(this.state.module.context)(expr);
			});
			parser.plugin("expression require.main", ParserHelpers.toConstantDependency("__webpack_require__.c[__webpack_require__.s]"));
			parser.plugin(
				"expression require.extensions",
				ParserHelpers.expressionIsUnsupported("require.extensions is not supported by webpack. Use a loader instead.")
			);
			parser.plugin("expression module.loaded", ParserHelpers.toConstantDependency("module.l"));
			parser.plugin("expression module.id", ParserHelpers.toConstantDependency("module.i"));
			parser.plugin("expression module.exports", function() {
				var module = this.state.module;
				var isHarmony = module.meta && module.meta.harmonyModule;
				if(!isHarmony)
					return true;
			});
			parser.plugin("evaluate Identifier module.hot", ParserHelpers.evaluateToBoolean(false));
			parser.plugin("expression module", function() {
				var module = this.state.module;
				var isHarmony = module.meta && module.meta.harmonyModule;
				var moduleJsPath = path.join(__dirname, "..", "buildin", isHarmony ? "harmony-module.js" : "module.js");
				if(module.context) {
					moduleJsPath = path.relative(this.state.module.context, moduleJsPath);
					if(!/^[A-Z]:/i.test(moduleJsPath)) {
						moduleJsPath = "./" + moduleJsPath.replace(/\\/g, "/");
					}
				}
				return ParserHelpers.addParsedVariableToModule(this, "module", "require(" + JSON.stringify(moduleJsPath) + ")(module)");
			});
		});
	});
}
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.NormalModuleFactory"></a>[module webpack.NormalModuleFactory](#apidoc.module.webpack.NormalModuleFactory)

#### <a name="apidoc.element.webpack.NormalModuleFactory.NormalModuleFactory"></a>[function <span class="apidocSignatureSpan">webpack.</span>NormalModuleFactory (context, resolvers, options)](#apidoc.element.webpack.NormalModuleFactory.NormalModuleFactory)
- description and source-code
```javascript
function NormalModuleFactory(context, resolvers, options) {
	Tapable.call(this);
	this.resolvers = resolvers;
	this.ruleSet = new RuleSet(options.rules || options.loaders);
	this.cachePredicate = typeof options.unsafeCache === "function" ? options.unsafeCache : Boolean.bind(null, options.unsafeCache);
	this.context = context || "";
	this.parserCache = {};
	this.plugin("factory", function() {
		var _this = this;
		return function(result, callback) {
			var resolver = _this.applyPluginsWaterfall0("resolver", null);

			// Ignored
			if(!resolver) return callback();

			resolver(result, function onDoneResolving(err, data) {
				if(err) return callback(err);

				// Ignored
				if(!data) return callback();

				// direct module
				if(typeof data.source === "function")
					return callback(null, data);

				_this.applyPluginsAsyncWaterfall("after-resolve", data, function(err, result) {
					if(err) return callback(err);

					// Ignored
					if(!result) return callback();

					var createdModule = _this.applyPluginsBailResult("create-module", result);
					if(!createdModule) {

						if(!result.request) {
							return callback(new Error("Empty dependency (no request)"));
						}

						createdModule = new NormalModule(
							result.request,
							result.userRequest,
							result.rawRequest,
							result.loaders,
							result.resource,
							result.parser
						);
					}

					createdModule = _this.applyPluginsWaterfall0("module", createdModule);

					return callback(null, createdModule);
				});
			});
		};
	});
	this.plugin("resolver", function() {
		var _this = this;
		return function(data, callback) {
			var contextInfo = data.contextInfo;
			var context = data.context;
			var request = data.request;
			var resolveContextInfo = {};

			var noAutoLoaders = /^-?!/.test(request);
			var noPrePostAutoLoaders = /^!!/.test(request);
			var noPostAutoLoaders = /^-!/.test(request);
			var elements = request.replace(/^-?!+/, "").replace(/!!+/g, "!").split("!");
			var resource = elements.pop();
			elements = elements.map(identToLoaderRequest);

			async.parallel([
				function(callback) {
					_this.resolveRequestArray(resolveContextInfo, context, elements, _this.resolvers.loader, callback);
				},
				function(callback) {
					if(resource === "" || resource[0] === "?")
						return callback(null, {
							resource: resource
						});

					_this.resolvers.normal.resolve(resolveContextInfo, context, resource, function(err, resource, resourceResolveData) {
						if(err) return callback(err);
						callback(null, {
							resourceResolveData: resourceResolveData,
							resource: resource,
						});
					});
				}
			], function(err, results) {
				if(err) return callback(err);
				var loaders = results[0];
				var resourceResolveData = results[1].resourceResolveData;
				resource = results[1].resource;

				// translate option idents
				try {
					loaders.forEach(function(item) {
						if(typeof item.options === "string" && /^\?/.test(item.options)) {
							item.options = _this.ruleSet.findOptionsByIdent(item.options.substr(1));
						}
					});
				} catch(e) {
					return callback(e);
				}

				if(resource === false)
					return callback(null,
						new RawModule("/* (ignored) */",
							"ignored " + context + " " + request,
							request + " (ignored)")); // ignored

				var userRequest = loaders.map(loaderToIdent).concat([resource]).join("!");

				var resourcePath = resource;
				var resourceQuery = "";
				var queryIndex = resourcePath.indexOf("?");
				if(queryIndex >= 0) {
					resourceQuery = resourcePath.substr(queryIndex);
					resourcePath = resourcePath.substr(0, queryIndex);
				}

				var result = _this.ruleSet.exec({
					resource: resourcePath,
					resourceQuery: resourceQuery,
					issuer: contextInfo.issuer,
					compiler: contextInfo.compiler
				});
				var settings = {};
				var useLoadersPost = [];
				var useLoaders = [];
				var useLoadersPre = [];
				result.forEac ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.NormalModuleFactory.prototype"></a>[module webpack.NormalModuleFactory.prototype](#apidoc.module.webpack.NormalModuleFactory.prototype)

#### <a name="apidoc.element.webpack.NormalModuleFactory.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>constructor (context, resolvers, options)](#apidoc.element.webpack.NormalModuleFactory.prototype.constructor)
- description and source-code
```javascript
function NormalModuleFactory(context, resolvers, options) {
	Tapable.call(this);
	this.resolvers = resolvers;
	this.ruleSet = new RuleSet(options.rules || options.loaders);
	this.cachePredicate = typeof options.unsafeCache === "function" ? options.unsafeCache : Boolean.bind(null, options.unsafeCache);
	this.context = context || "";
	this.parserCache = {};
	this.plugin("factory", function() {
		var _this = this;
		return function(result, callback) {
			var resolver = _this.applyPluginsWaterfall0("resolver", null);

			// Ignored
			if(!resolver) return callback();

			resolver(result, function onDoneResolving(err, data) {
				if(err) return callback(err);

				// Ignored
				if(!data) return callback();

				// direct module
				if(typeof data.source === "function")
					return callback(null, data);

				_this.applyPluginsAsyncWaterfall("after-resolve", data, function(err, result) {
					if(err) return callback(err);

					// Ignored
					if(!result) return callback();

					var createdModule = _this.applyPluginsBailResult("create-module", result);
					if(!createdModule) {

						if(!result.request) {
							return callback(new Error("Empty dependency (no request)"));
						}

						createdModule = new NormalModule(
							result.request,
							result.userRequest,
							result.rawRequest,
							result.loaders,
							result.resource,
							result.parser
						);
					}

					createdModule = _this.applyPluginsWaterfall0("module", createdModule);

					return callback(null, createdModule);
				});
			});
		};
	});
	this.plugin("resolver", function() {
		var _this = this;
		return function(data, callback) {
			var contextInfo = data.contextInfo;
			var context = data.context;
			var request = data.request;
			var resolveContextInfo = {};

			var noAutoLoaders = /^-?!/.test(request);
			var noPrePostAutoLoaders = /^!!/.test(request);
			var noPostAutoLoaders = /^-!/.test(request);
			var elements = request.replace(/^-?!+/, "").replace(/!!+/g, "!").split("!");
			var resource = elements.pop();
			elements = elements.map(identToLoaderRequest);

			async.parallel([
				function(callback) {
					_this.resolveRequestArray(resolveContextInfo, context, elements, _this.resolvers.loader, callback);
				},
				function(callback) {
					if(resource === "" || resource[0] === "?")
						return callback(null, {
							resource: resource
						});

					_this.resolvers.normal.resolve(resolveContextInfo, context, resource, function(err, resource, resourceResolveData) {
						if(err) return callback(err);
						callback(null, {
							resourceResolveData: resourceResolveData,
							resource: resource,
						});
					});
				}
			], function(err, results) {
				if(err) return callback(err);
				var loaders = results[0];
				var resourceResolveData = results[1].resourceResolveData;
				resource = results[1].resource;

				// translate option idents
				try {
					loaders.forEach(function(item) {
						if(typeof item.options === "string" && /^\?/.test(item.options)) {
							item.options = _this.ruleSet.findOptionsByIdent(item.options.substr(1));
						}
					});
				} catch(e) {
					return callback(e);
				}

				if(resource === false)
					return callback(null,
						new RawModule("/* (ignored) */",
							"ignored " + context + " " + request,
							request + " (ignored)")); // ignored

				var userRequest = loaders.map(loaderToIdent).concat([resource]).join("!");

				var resourcePath = resource;
				var resourceQuery = "";
				var queryIndex = resourcePath.indexOf("?");
				if(queryIndex >= 0) {
					resourceQuery = resourcePath.substr(queryIndex);
					resourcePath = resourcePath.substr(0, queryIndex);
				}

				var result = _this.ruleSet.exec({
					resource: resourcePath,
					resourceQuery: resourceQuery,
					issuer: contextInfo.issuer,
					compiler: contextInfo.compiler
				});
				var settings = {};
				var useLoadersPost = [];
				var useLoaders = [];
				var useLoadersPre = [];
				result.forEac ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.NormalModuleFactory.prototype.create"></a>[function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>create (data, callback)](#apidoc.element.webpack.NormalModuleFactory.prototype.create)
- description and source-code
```javascript
create = function (data, callback) {
	var _this = this;
	var dependencies = data.dependencies;
	var cacheEntry = dependencies[0].__NormalModuleFactoryCache;
	if(cacheEntry) return callback(null, cacheEntry);
	var context = data.context || this.context;
	var request = dependencies[0].request;
	var contextInfo = data.contextInfo || {};
	_this.applyPluginsAsyncWaterfall("before-resolve", {
		contextInfo: contextInfo,
		context: context,
		request: request,
		dependencies: dependencies
	}, function(err, result) {
		if(err) return callback(err);

		// Ignored
		if(!result) return callback();

		var factory = _this.applyPluginsWaterfall0("factory", null);

		// Ignored
		if(!factory) return callback();

		factory(result, function(err, module) {
			if(err) return callback(err);

			if(module && _this.cachePredicate(module)) {
				dependencies.forEach(function(d) {
					d.__NormalModuleFactoryCache = module;
				});
			}

			callback(null, module);
		});

	});
}
```
- example usage
```shell
...
			const warningAndCallback = function warningAndCallback(err) {
				err.origin = module;
				_this.warnings.push(err);
				callback();
			};

			const factory = item[0];
			factory.create({
				contextInfo: {
					issuer: module.nameForCondition && module.nameForCondition(),
					compiler: _this.compiler.name
				},
				context: module.context,
				dependencies: dependencies
			}, function factoryCallback(err, dependentModule) {
...
```

#### <a name="apidoc.element.webpack.NormalModuleFactory.prototype.createParser"></a>[function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>createParser (parserOptions)](#apidoc.element.webpack.NormalModuleFactory.prototype.createParser)
- description and source-code
```javascript
function createParser(parserOptions) {
	var parser = new Parser();
	this.applyPlugins2("parser", parser, parserOptions || {});
	return parser;
}
```
- example usage
```shell
...
			ident = parserOptions.ident;
		else
			ident = JSON.stringify(parserOptions);
	}
	var parser = this.parserCache[ident];
	if(parser)
		return parser;
	return this.parserCache[ident] = this.createParser(parserOptions);
};

NormalModuleFactory.prototype.createParser = function createParser(parserOptions) {
	var parser = new Parser();
	this.applyPlugins2("parser", parser, parserOptions || {});
	return parser;
};
...
```

#### <a name="apidoc.element.webpack.NormalModuleFactory.prototype.getParser"></a>[function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>getParser (parserOptions)](#apidoc.element.webpack.NormalModuleFactory.prototype.getParser)
- description and source-code
```javascript
function getParser(parserOptions) {
	var ident = "null";
	if(parserOptions) {
		if(parserOptions.ident)
			ident = parserOptions.ident;
		else
			ident = JSON.stringify(parserOptions);
	}
	var parser = this.parserCache[ident];
	if(parser)
		return parser;
	return this.parserCache[ident] = this.createParser(parserOptions);
}
```
- example usage
```shell
...
						request: loaders.map(loaderToIdent).concat([resource]).join("!"),
						dependencies: data.dependencies,
						userRequest: userRequest,
						rawRequest: request,
						loaders: loaders,
						resource: resource,
						resourceResolveData: resourceResolveData,
						parser: _this.getParser(settings.parser)
					});
				}
			});
		};
	});
}
module.exports = NormalModuleFactory;
...
```

#### <a name="apidoc.element.webpack.NormalModuleFactory.prototype.resolveRequestArray"></a>[function <span class="apidocSignatureSpan">webpack.NormalModuleFactory.prototype.</span>resolveRequestArray (contextInfo, context, array, resolver, callback)](#apidoc.element.webpack.NormalModuleFactory.prototype.resolveRequestArray)
- description and source-code
```javascript
function resolveRequestArray(contextInfo, context, array, resolver, callback) {
	if(array.length === 0) return callback(null, []);
	async.map(array, function(item, callback) {
		resolver.resolve(contextInfo, context, item.loader, function(err, result) {
			if(err && /^[^/]*$/.test(item.loader) && !/-loader$/.test(item.loader)) {
				return resolver.resolve(contextInfo, context, item.loader + "-loader", function(err2) {
					if(!err2) {
						err.message = err.message + "\n" +
							"BREAKING CHANGE: It's no longer allowed to omit the '-loader' suffix when using loaders.\n" +
							"                 You need to specify '" + item.loader + "-loader' instead of '" + item.loader + "',\n" +
							"                 see https://webpack.js.org/guides/migrating/#automatic-loader-module-name-extension-removed";
					}
					callback(err);
				});
			}
			if(err) return callback(err);

			var optionsOnly = item.options ? {
				options: item.options
			} : undefined;
			return callback(null, Object.assign({}, item, identToLoaderRequest(result), optionsOnly));
		});
	}, callback);
}
```
- example usage
```shell
...
			var noPostAutoLoaders = /^-!/.test(request);
			var elements = request.replace(/^-?!+/, "").replace(/!!+/g, "!").split("!");
			var resource = elements.pop();
			elements = elements.map(identToLoaderRequest);

			async.parallel([
				function(callback) {
					_this.resolveRequestArray(resolveContextInfo, context, elements, _this.resolvers.loader, callback);
				},
				function(callback) {
					if(resource === "" || resource[0] === "?")
						return callback(null, {
							resource: resource
						});
...
```



# <a name="apidoc.module.webpack.Parser"></a>[module webpack.Parser](#apidoc.module.webpack.Parser)

#### <a name="apidoc.element.webpack.Parser.Parser"></a>[function <span class="apidocSignatureSpan">webpack.</span>Parser (options)](#apidoc.element.webpack.Parser.Parser)
- description and source-code
```javascript
function Parser(options) {
	Tapable.call(this);
	this.options = options;
	this.initializeEvaluating();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.Parser.prototype"></a>[module webpack.Parser.prototype](#apidoc.module.webpack.Parser.prototype)

#### <a name="apidoc.element.webpack.Parser.prototype.constructor"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>constructor (options)](#apidoc.element.webpack.Parser.prototype.constructor)
- description and source-code
```javascript
function Parser(options) {
	Tapable.call(this);
	this.options = options;
	this.initializeEvaluating();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.enterArrayPattern"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterArrayPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterArrayPattern)
- description and source-code
```javascript
function enterArrayPattern(pattern, onIdent) {
	for(var elementIndex = 0, len = pattern.elements.length; elementIndex < len; elementIndex++) {
		var element = pattern.elements[elementIndex];
		this.enterPattern(element, onIdent);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.enterAssignmentPattern"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterAssignmentPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterAssignmentPattern)
- description and source-code
```javascript
function enterAssignmentPattern(pattern, onIdent) {
	this.enterPattern(pattern.left, onIdent);
	this.walkExpression(pattern.right);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.enterIdentifier"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterIdentifier (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterIdentifier)
- description and source-code
```javascript
function enterIdentifier(pattern, onIdent) {
	onIdent(pattern.name, pattern);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.enterObjectPattern"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterObjectPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterObjectPattern)
- description and source-code
```javascript
function enterObjectPattern(pattern, onIdent) {
	for(var propIndex = 0, len = pattern.properties.length; propIndex < len; propIndex++) {
		var prop = pattern.properties[propIndex];
		this.enterPattern(prop.value, onIdent);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.enterPattern"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterPattern (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterPattern)
- description and source-code
```javascript
function enterPattern(pattern, onIdent) {
	if(pattern && this["enter" + pattern.type])
		this["enter" + pattern.type](pattern, onIdent);
}
```
- example usage
```shell
...
					if(!_this.applyPluginsBailResult1("rename " + renameIdentifier, declarator.init)) {
						_this.scope.renames["$" + declarator.id.name] = _this.scope.renames["$" + renameIdentifier] || renameIdentifier;
						var idx = _this.scope.definitions.indexOf(declarator.id.name);
						if(idx >= 0) _this.scope.definitions.splice(idx, 1);
					}
				} else {
					_this.walkPattern(declarator.id);
					_this.enterPattern(declarator.id, function(name, decl) {
						if(!_this.applyPluginsBailResult1("var " + name, decl)) {
							_this.scope.renames["$" + name] = undefined;
							_this.scope.definitions.push(name);
						}
					});
					if(declarator.init)
						_this.walkExpression(declarator.init);
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.enterRestElement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>enterRestElement (pattern, onIdent)](#apidoc.element.webpack.Parser.prototype.enterRestElement)
- description and source-code
```javascript
function enterRestElement(pattern, onIdent) {
	this.enterPattern(pattern.argument, onIdent);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.evaluate"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>evaluate (source)](#apidoc.element.webpack.Parser.prototype.evaluate)
- description and source-code
```javascript
function evaluate(source) {
	var ast = acorn.parse("(" + source + ")", {
		ranges: true,
		locations: true,
		ecmaVersion: 2017,
		sourceType: "module",
		plugins: {
			dynamicImport: true
		}
	});
	if(!ast || typeof ast !== "object" || ast.type !== "Program")
		throw new Error("evaluate: Source couldn't be parsed");
	if(ast.body.length !== 1 || ast.body[0].type !== "ExpressionStatement")
		throw new Error("evaluate: Source is not a expression");
	return this.evaluateExpression(ast.body[0].expression);
}
```
- example usage
```shell
...
							 * e.g.: new DefinePlugin({
							 * "a": "b",
							 * "b": "a"
							 * });
							 */
							if(recurse) return;
							recurse = true;
							const res = parser.evaluate(code);
							recurse = false;
							res.setRange(expr.range);
							return res;
						});
						parser.plugin("expression " + key, ParserHelpers.toConstantDependency(code));
					}
					const typeofCode = isTypeof ? code : "typeof (" + code + ")";
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.evaluateExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>evaluateExpression (expression)](#apidoc.element.webpack.Parser.prototype.evaluateExpression)
- description and source-code
```javascript
function evaluateExpression(expression) {
	try {
		var result = this.applyPluginsBailResult1("evaluate " + expression.type, expression);
		if(result !== undefined)
			return result;
	} catch(e) {
		console.warn(e);
		// ignore error
	}
	return new BasicEvaluatedExpression().setRange(expression.range);
}
```
- example usage
```shell
...

				if(typeof parserOptions.browserify !== "undefined" && !parserOptions.browserify)
					return;

				parser.plugin("call require", (expr) => {
					// support for browserify style require delegator: "require(o, !0)"
					if(expr.arguments.length !== 2) return;
					const second = parser.evaluateExpression(expr.arguments[1]);
					if(!second.isBoolean()) return;
					if(second.asBool() !== true) return;
					const dep = new ConstDependency("require", expr.callee.range);
					dep.loc = expr.loc;
					if(parser.state.current.dependencies.length > 1) {
						const last = parser.state.current.dependencies[parser.state.current.dependencies.length - 1];
						if(last.critical && last.request === "." && last.userRequest === "." && last.recursive)
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.getRenameIdentifier"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>getRenameIdentifier (expr)](#apidoc.element.webpack.Parser.prototype.getRenameIdentifier)
- description and source-code
```javascript
function getRenameIdentifier(expr) {
	var result = this.evaluateExpression(expr);
	if(!result) return;
	if(result.isIdentifier()) return result.identifier;
	return;
}
```
- example usage
```shell
...
};

Parser.prototype.walkVariableDeclarators = function walkVariableDeclarators(declarators) {
	var _this = this;
	declarators.forEach(function(declarator) {
		switch(declarator.type) {
			case "VariableDeclarator":
				var renameIdentifier = declarator.init && _this.getRenameIdentifier(declarator.init);
				if(renameIdentifier && declarator.id.type === "Identifier" && _this.applyPluginsBailResult1("can-rename " + renameIdentifier
, declarator.init)) {
					// renaming with "var a = b;"
					if(!_this.applyPluginsBailResult1("rename " + renameIdentifier, declarator.init)) {
						_this.scope.renames["$" + declarator.id.name] = _this.scope.renames["$" + renameIdentifier] || renameIdentifier;
						var idx = _this.scope.definitions.indexOf(declarator.id.name);
						if(idx >= 0) _this.scope.definitions.splice(idx, 1);
					}
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.inScope"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>inScope (params, fn)](#apidoc.element.webpack.Parser.prototype.inScope)
- description and source-code
```javascript
function inScope(params, fn) {
	var oldScope = this.scope;
	var _this = this;
	this.scope = {
		inTry: false,
		inShorthand: false,
		definitions: oldScope.definitions.slice(),
		renames: Object.create(oldScope.renames)
	};

	for(var paramIndex = 0, len = params.length; paramIndex < len; paramIndex++) {
		var param = params[paramIndex];

		if(typeof param !== "string") {
			_this.enterPattern(param, function(param) {
				_this.scope.renames["$" + param] = undefined;
				_this.scope.definitions.push(param);
			});
		} else {
			_this.scope.renames["$" + param] = undefined;
			_this.scope.definitions.push(param);
		}
	}

	fn();
	_this.scope = oldScope;
}
```
- example usage
```shell
...
	this.walkStatement(statement.body);
};

// Declarations
Parser.prototype.walkFunctionDeclaration = function walkFunctionDeclaration(statement) {
	this.scope.renames["$" + statement.id.name] = undefined;
	this.scope.definitions.push(statement.id.name);
	this.inScope(statement.params, function() {
		if(statement.body.type === "BlockStatement")
			this.walkStatement(statement.body);
		else
			this.walkExpression(statement.body);
	}.bind(this));
};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.initializeEvaluating"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>initializeEvaluating ()](#apidoc.element.webpack.Parser.prototype.initializeEvaluating)
- description and source-code
```javascript
initializeEvaluating = function () {
	function joinRanges(startRange, endRange) {
		if(!endRange) return startRange;
		if(!startRange) return endRange;
		return [startRange[0], endRange[1]];
	}
	this.plugin("evaluate Literal", function(expr) {
		switch(typeof expr.value) {
			case "number":
				return new BasicEvaluatedExpression().setNumber(expr.value).setRange(expr.range);
			case "string":
				return new BasicEvaluatedExpression().setString(expr.value).setRange(expr.range);
			case "boolean":
				return new BasicEvaluatedExpression().setBoolean(expr.value).setRange(expr.range);
		}
		if(expr.value === null)
			return new BasicEvaluatedExpression().setNull().setRange(expr.range);
		if(expr.value instanceof RegExp)
			return new BasicEvaluatedExpression().setRegExp(expr.value).setRange(expr.range);
	});
	this.plugin("evaluate LogicalExpression", function(expr) {
		var left;
		var leftAsBool;
		var right;
		if(expr.operator === "&&") {
			left = this.evaluateExpression(expr.left);
			leftAsBool = left && left.asBool();
			if(leftAsBool === false) return left.setRange(expr.range);
			if(leftAsBool !== true) return;
			right = this.evaluateExpression(expr.right);
			return right.setRange(expr.range);
		} else if(expr.operator === "||") {
			left = this.evaluateExpression(expr.left);
			leftAsBool = left && left.asBool();
			if(leftAsBool === true) return left.setRange(expr.range);
			if(leftAsBool !== false) return;
			right = this.evaluateExpression(expr.right);
			return right.setRange(expr.range);
		}
	});
	this.plugin("evaluate BinaryExpression", function(expr) {
		var left;
		var right;
		var res;
		if(expr.operator === "+") {
			left = this.evaluateExpression(expr.left);
			right = this.evaluateExpression(expr.right);
			if(!left || !right) return;
			res = new BasicEvaluatedExpression();
			if(left.isString()) {
				if(right.isString()) {
					res.setString(left.string + right.string);
				} else if(right.isNumber()) {
					res.setString(left.string + right.number);
				} else if(right.isWrapped() && right.prefix && right.prefix.isString()) {
					res.setWrapped(
						new BasicEvaluatedExpression()
						.setString(left.string + right.prefix.string)
						.setRange(joinRanges(left.range, right.prefix.range)),
						right.postfix);
				} else {
					res.setWrapped(left, null);
				}
			} else if(left.isNumber()) {
				if(right.isString()) {
					res.setString(left.number + right.string);
				} else if(right.isNumber()) {
					res.setNumber(left.number + right.number);
				}
			} else if(left.isWrapped()) {
				if(left.postfix && left.postfix.isString() && right.isString()) {
					res.setWrapped(left.prefix,
						new BasicEvaluatedExpression()
						.setString(left.postfix.string + right.string)
						.setRange(joinRanges(left.postfix.range, right.range))
					);
				} else if(left.postfix && left.postfix.isString() && right.isNumber()) {
					res.setWrapped(left.prefix,
						new BasicEvaluatedExpression()
						.setString(left.postfix.string + right.number)
						.setRange(joinRanges(left.postfix.range, right.range))
					);
				} else if(right.isString()) {
					res.setWrapped(left.prefix, right);
				} else if(right.isNumber()) {
					res.setWrapped(left.prefix,
						new BasicEvaluatedExpression()
						.setString(right.number + "")
						.setRange(right.range));
				} else {
					res.setWrapped(left.prefix, new BasicEvaluatedExpression());
				}
			} else {
				if(right.isString()) {
					res.setWrapped(null, right);
				}
			}
			res.setRange(expr.range);
			return res;
		} else if(expr.operator === "-") {
			left = this.evaluateExpression(expr.left);
			right = this.evaluateExpression(expr.right);
			if(!left || !right) return;
			if(!left.isNumber() || !right.isNumber()) return;
			res = new BasicEvaluatedExpression();
			res.setNumber(left.number - right.number);
			res.setRange(expr.range);
			return res;
		} else if(expr.operator === "*") {
			left = this.evaluateExpression(expr.left);
			right = this.evaluateExpressio ...
```
- example usage
```shell
...
var acorn = require("acorn-dynamic-import").default;
var Tapable = require("tapable");
var BasicEvaluatedExpression = require("./BasicEvaluatedExpression");

function Parser(options) {
	Tapable.call(this);
	this.options = options;
	this.initializeEvaluating();
}
module.exports = Parser;

// Syntax: https://developer.mozilla.org/en/SpiderMonkey/Parser_API

Parser.prototype = Object.create(Tapable.prototype);
Parser.prototype.constructor = Parser;
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.isHoistedStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>isHoistedStatement (statement)](#apidoc.element.webpack.Parser.prototype.isHoistedStatement)
- description and source-code
```javascript
function isHoistedStatement(statement) {
	switch(statement.type) {
		case "ImportDeclaration":
		case "ExportAllDeclaration":
		case "ExportNamedDeclaration":
			return true;
	}
	return false;
}
```
- example usage
```shell
...
	if(methodDefinition.value)
		this.walkExpression(methodDefinition.value);
};

Parser.prototype.walkStatements = function walkStatements(statements) {
	for(var indexA = 0, lenA = statements.length; indexA < lenA; indexA++) {
		var statementA = statements[indexA];
		if(this.isHoistedStatement(statementA))
			this.walkStatement(statementA);
	}
	for(var indexB = 0, lenB = statements.length; indexB < lenB; indexB++) {
		var statementB = statements[indexB];
		if(!this.isHoistedStatement(statementB))
			this.walkStatement(statementB);
	}
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.parse"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parse (source, initialState)](#apidoc.element.webpack.Parser.prototype.parse)
- description and source-code
```javascript
function parse(source, initialState) {
	var ast, comments = [];
	for(var i = 0, len = POSSIBLE_AST_OPTIONS.length; i < len; i++) {
		if(!ast) {
			try {
				comments.length = 0;
				POSSIBLE_AST_OPTIONS[i].onComment = comments;
				ast = acorn.parse(source, POSSIBLE_AST_OPTIONS[i]);
			} catch(e) {
				// ignore the error
			}
		}
	}
	if(!ast) {
		// for the error
		ast = acorn.parse(source, {
			ranges: true,
			locations: true,
			ecmaVersion: 2017,
			sourceType: "module",
			plugins: {
				dynamicImport: true
			},
			onComment: comments
		});
	}
	if(!ast || typeof ast !== "object")
		throw new Error("Source couldn't be parsed");
	var oldScope = this.scope;
	var oldState = this.state;
	this.scope = {
		inTry: false,
		definitions: [],
		renames: {}
	};
	var state = this.state = initialState || {};
	if(this.applyPluginsBailResult("program", ast, comments) === undefined)
		this.walkStatements(ast.body);
	this.scope = oldScope;
	this.state = oldState;
	return state;
}
```
- example usage
```shell
...

		compiler.plugin("before-compile", (params, callback) => {
			const manifest = this.options.manifest;
			if(typeof manifest === "string") {
				params.compilationDependencies.push(manifest);
				compiler.inputFileSystem.readFile(manifest, function(err, result) {
					if(err) return callback(err);
					params["dll reference " + manifest] = JSON.parse(result.toString("utf-8"));
					return callback();
				});
			} else {
				return callback();
			}
		});
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.parseCalculatedString"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseCalculatedString (expression)](#apidoc.element.webpack.Parser.prototype.parseCalculatedString)
- description and source-code
```javascript
function parseCalculatedString(expression) {
	switch(expression.type) {
		case "BinaryExpression":
			if(expression.operator === "+") {
				var left = this.parseCalculatedString(expression.left);
				var right = this.parseCalculatedString(expression.right);
				if(left.code) {
					return {
						range: left.range,
						value: left.value,
						code: true
					};
				} else if(right.code) {
					return {
						range: [left.range[0], right.range ? right.range[1] : left.range[1]],
						value: left.value + right.value,
						code: true
					};
				} else {
					return {
						range: [left.range[0], right.range[1]],
						value: left.value + right.value
					};
				}
			}
			break;
		case "ConditionalExpression":
			var consequent = this.parseCalculatedString(expression.consequent);
			var alternate = this.parseCalculatedString(expression.alternate);
			var items = [];
			if(consequent.conditional)
				Array.prototype.push.apply(items, consequent.conditional);
			else if(!consequent.code)
				items.push(consequent);
			else break;
			if(alternate.conditional)
				Array.prototype.push.apply(items, alternate.conditional);
			else if(!alternate.code)
				items.push(alternate);
			else break;
			return {
				value: "",
				code: true,
				conditional: items
			};
		case "Literal":
			return {
				range: expression.range,
				value: expression.value + ""
			};
	}
	return {
		value: "",
		code: true
	};
}
```
- example usage
```shell
...
	throw new Error(expression.type + " is not supported as parameter for require");
};

Parser.prototype.parseCalculatedString = function parseCalculatedString(expression) {
	switch(expression.type) {
		case "BinaryExpression":
			if(expression.operator === "+") {
				var left = this.parseCalculatedString(expression.left);
				var right = this.parseCalculatedString(expression.right);
				if(left.code) {
					return {
						range: left.range,
						value: left.value,
						code: true
					};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.parseCalculatedStringArray"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseCalculatedStringArray (expression)](#apidoc.element.webpack.Parser.prototype.parseCalculatedStringArray)
- description and source-code
```javascript
function parseXXXArray(expression) {
		switch(expression.type) {
			case "ArrayExpression":
				var arr = [];
				if(expression.elements)
					expression.elements.forEach(function(expr) {
						arr.push(this[fn](expr));
					}, this);
				return arr;
		}
		return [this[fn](expression)];
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.parseString"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseString (expression)](#apidoc.element.webpack.Parser.prototype.parseString)
- description and source-code
```javascript
function parseString(expression) {
	switch(expression.type) {
		case "BinaryExpression":
			if(expression.operator === "+")
				return this.parseString(expression.left) + this.parseString(expression.right);
			break;
		case "Literal":
			return expression.value + "";
	}
	throw new Error(expression.type + " is not supported as parameter for require");
}
```
- example usage
```shell
...
	return new BasicEvaluatedExpression().setRange(expression.range);
};

Parser.prototype.parseString = function parseString(expression) {
	switch(expression.type) {
		case "BinaryExpression":
			if(expression.operator === "+")
				return this.parseString(expression.left) + this.parseString(expression.right);
			break;
		case "Literal":
			return expression.value + "";
	}
	throw new Error(expression.type + " is not supported as parameter for require");
};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.parseStringArray"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>parseStringArray (expression)](#apidoc.element.webpack.Parser.prototype.parseStringArray)
- description and source-code
```javascript
function parseXXXArray(expression) {
		switch(expression.type) {
			case "ArrayExpression":
				var arr = [];
				if(expression.elements)
					expression.elements.forEach(function(expr) {
						arr.push(this[fn](expr));
					}, this);
				return arr;
		}
		return [this[fn](expression)];
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkArrayExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkArrayExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkArrayExpression)
- description and source-code
```javascript
function walkArrayExpression(expression) {
	if(expression.elements)
		this.walkExpressions(expression.elements);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkArrayPattern"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkArrayPattern (pattern)](#apidoc.element.webpack.Parser.prototype.walkArrayPattern)
- description and source-code
```javascript
function walkArrayPattern(pattern) {
	for(var i = 0, len = pattern.elements.length; i < len; i++) {
		var element = pattern.elements[i];
		if(element)
			this.walkPattern(element);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkArrowFunctionExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkArrowFunctionExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkArrowFunctionExpression)
- description and source-code
```javascript
function walkArrowFunctionExpression(expression) {
	this.inScope(expression.params, function() {
		if(expression.body.type === "BlockStatement")
			this.walkStatement(expression.body);
		else
			this.walkExpression(expression.body);
	}.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkAssignmentExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkAssignmentExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkAssignmentExpression)
- description and source-code
```javascript
function walkAssignmentExpression(expression) {
	var renameIdentifier = this.getRenameIdentifier(expression.right);
	if(expression.left.type === "Identifier" && renameIdentifier && this.applyPluginsBailResult1("can-rename " + renameIdentifier,
expression.right)) {
		// renaming "a = b;"
		if(!this.applyPluginsBailResult1("rename " + renameIdentifier, expression.right)) {
			this.scope.renames["$" + expression.left.name] = renameIdentifier;
			var idx = this.scope.definitions.indexOf(expression.left.name);
			if(idx >= 0) this.scope.definitions.splice(idx, 1);
		}
	} else if(expression.left.type === "Identifier") {
		if(!this.applyPluginsBailResult1("assigned " + expression.left.name, expression)) {
			this.walkExpression(expression.right);
		}
		this.scope.renames["$" + expression.left.name] = undefined;
		if(!this.applyPluginsBailResult1("assign " + expression.left.name, expression)) {
			this.walkExpression(expression.left);
		}
	} else {
		this.walkExpression(expression.right);
		this.scope.renames["$" + expression.left.name] = undefined;
		this.walkExpression(expression.left);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkAwaitExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkAwaitExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkAwaitExpression)
- description and source-code
```javascript
function walkAwaitExpression(expression) {
	var argument = expression.argument;
	if(this["walk" + argument.type])
		return this["walk" + argument.type](argument);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkBinaryExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkBinaryExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkBinaryExpression)
- description and source-code
```javascript
function walkLeftRightExpression(expression) {
		this.walkExpression(expression.left);
		this.walkExpression(expression.right);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkBlockStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkBlockStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkBlockStatement)
- description and source-code
```javascript
function walkBlockStatement(statement) {
	this.walkStatements(statement.body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkCallExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkCallExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkCallExpression)
- description and source-code
```javascript
function walkCallExpression(expression) {
	var result;

	function walkIIFE(functionExpression, options) {
		var params = functionExpression.params;
		var args = options.map(function(arg) {
			var renameIdentifier = this.getRenameIdentifier(arg);
			if(renameIdentifier && this.applyPluginsBailResult1("can-rename " + renameIdentifier, arg)) {
				if(!this.applyPluginsBailResult1("rename " + renameIdentifier, arg))
					return renameIdentifier;
			}
			this.walkExpression(arg);
		}, this);
		this.inScope(params.filter(function(identifier, idx) {
			return !args[idx];
		}), function() {
			for(var i = 0; i < args.length; i++) {
				var param = args[i];
				if(!param) continue;
				if(!params[i] || params[i].type !== "Identifier") continue;
				this.scope.renames["$" + params[i].name] = param;
			}
			if(functionExpression.body.type === "BlockStatement")
				this.walkStatement(functionExpression.body);
			else
				this.walkExpression(functionExpression.body);
		}.bind(this));
	}
	if(expression.callee.type === "MemberExpression" &&
		expression.callee.object.type === "FunctionExpression" &&
		!expression.callee.computed &&
		(["call", "bind"]).indexOf(expression.callee.property.name) >= 0 &&
		expression.arguments &&
		expression.arguments.length > 1
	) {
		// (function(...) { }.call/bind(?, ...))
		walkIIFE.call(this, expression.callee.object, expression.arguments.slice(1));
		this.walkExpression(expression.arguments[0]);
	} else if(expression.callee.type === "FunctionExpression" && expression.arguments) {
		// (function(...) { }(...))
		walkIIFE.call(this, expression.callee, expression.arguments);
	} else if(expression.callee.type === "Import") {
		result = this.applyPluginsBailResult1("import-call", expression);
		if(result === true)
			return;

		if(expression.arguments)
			this.walkExpressions(expression.arguments);
	} else {

		var callee = this.evaluateExpression(expression.callee);
		if(callee.isIdentifier()) {
			result = this.applyPluginsBailResult1("call " + callee.identifier, expression);
			if(result === true)
				return;
		}

		if(expression.callee)
			this.walkExpression(expression.callee);
		if(expression.arguments)
			this.walkExpressions(expression.arguments);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkCatchClause"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkCatchClause (catchClause)](#apidoc.element.webpack.Parser.prototype.walkCatchClause)
- description and source-code
```javascript
function walkCatchClause(catchClause) {
	if(catchClause.guard)
		this.walkExpression(catchClause.guard);
	this.inScope([catchClause.param], function() {
		this.walkStatement(catchClause.body);
	}.bind(this));
}
```
- example usage
```shell
...
		this.walkStatement(statement.block);
	} else {
		this.scope.inTry = true;
		this.walkStatement(statement.block);
		this.scope.inTry = false;
	}
	if(statement.handler)
		this.walkCatchClause(statement.handler);
	if(statement.finalizer)
		this.walkStatement(statement.finalizer);
};

Parser.prototype.walkWhileStatement =
	Parser.prototype.walkDoWhileStatement = function walkLoopStatement(statement) {
		this.walkExpression(statement.test);
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkClass"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkClass (classy)](#apidoc.element.webpack.Parser.prototype.walkClass)
- description and source-code
```javascript
function walkClass(classy) {
	if(classy.superClass)
		this.walkExpression(classy.superClass);
	if(classy.body && classy.body.type === "ClassBody") {
		classy.body.body.forEach(function(methodDefinition) {
			if(methodDefinition.type === "MethodDefinition")
				this.walkMethodDefinition(methodDefinition);
		}, this);
	}
}
```
- example usage
```shell
...
	if(statement.declarations)
		this.walkVariableDeclarators(statement.declarations);
};

Parser.prototype.walkClassDeclaration = function walkClassDeclaration(statement) {
	this.scope.renames["$" + statement.id.name] = undefined;
	this.scope.definitions.push(statement.id.name);
	this.walkClass(statement);
};

Parser.prototype.walkSwitchCases = function walkSwitchCases(switchCases) {
	for(var index = 0, len = switchCases.length; index < len; index++) {
		var switchCase = switchCases[index];

		if(switchCase.test) {
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkClassDeclaration"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkClassDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkClassDeclaration)
- description and source-code
```javascript
function walkClassDeclaration(statement) {
	this.scope.renames["$" + statement.id.name] = undefined;
	this.scope.definitions.push(statement.id.name);
	this.walkClass(statement);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkClassExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkClassExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkClassExpression)
- description and source-code
```javascript
function walkClassExpression(expression) {
	this.walkClass(expression);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkConditionalExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkConditionalExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkConditionalExpression)
- description and source-code
```javascript
function walkConditionalExpression(expression) {
	var result = this.applyPluginsBailResult1("expression ?:", expression);
	if(result === undefined) {
		this.walkExpression(expression.test);
		this.walkExpression(expression.consequent);
		if(expression.alternate)
			this.walkExpression(expression.alternate);
	} else {
		if(result)
			this.walkExpression(expression.consequent);
		else if(expression.alternate)
			this.walkExpression(expression.alternate);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkDoWhileStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkDoWhileStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkDoWhileStatement)
- description and source-code
```javascript
function walkLoopStatement(statement) {
		this.walkExpression(statement.test);
		this.walkStatement(statement.body);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkExportAllDeclaration"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExportAllDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkExportAllDeclaration)
- description and source-code
```javascript
function walkExportAllDeclaration(statement) {
	var source = statement.source.value;
	this.applyPluginsBailResult("export import", statement, source);
	this.applyPluginsBailResult("export import specifier", statement, source, null, null, 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkExportDefaultDeclaration"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExportDefaultDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkExportDefaultDeclaration)
- description and source-code
```javascript
function walkExportDefaultDeclaration(statement) {
	this.applyPluginsBailResult1("export", statement);
	if(/Declaration$/.test(statement.declaration.type)) {
		if(!this.applyPluginsBailResult("export declaration", statement, statement.declaration)) {
			var pos = this.scope.definitions.length;
			this.walkStatement(statement.declaration);
			var newDefs = this.scope.definitions.slice(pos);
			for(var index = 0, len = newDefs.length; index < len; index++) {
				var def = newDefs[index];
				this.applyPluginsBailResult("export specifier", statement, def, "default");
			}
		}
	} else {
		this.walkExpression(statement.declaration);
		if(!this.applyPluginsBailResult("export expression", statement, statement.declaration)) {
			this.applyPluginsBailResult("export specifier", statement, statement.declaration, "default");
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkExportNamedDeclaration"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExportNamedDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkExportNamedDeclaration)
- description and source-code
```javascript
function walkExportNamedDeclaration(statement) {
	if(statement.source) {
		var source = statement.source.value;
		this.applyPluginsBailResult("export import", statement, source);
	} else {
		this.applyPluginsBailResult1("export", statement);
	}
	if(statement.declaration) {
		if(/Expression$/.test(statement.declaration.type)) {
			throw new Error("Doesn't occur?");
		} else {
			if(!this.applyPluginsBailResult("export declaration", statement, statement.declaration)) {
				var pos = this.scope.definitions.length;
				this.walkStatement(statement.declaration);
				var newDefs = this.scope.definitions.slice(pos);
				for(var index = newDefs.length - 1; index >= 0; index--) {
					var def = newDefs[index];
					this.applyPluginsBailResult("export specifier", statement, def, def, index);
				}
			}
		}
	}
	if(statement.specifiers) {
		for(var specifierIndex = 0; specifierIndex < statement.specifiers.length; specifierIndex++) {
			var specifier = statement.specifiers[specifierIndex];
			switch(specifier.type) {
				case "ExportSpecifier":
					var name = specifier.exported.name;
					if(source)
						this.applyPluginsBailResult("export import specifier", statement, source, specifier.local.name, name, specifierIndex);
					else
						this.applyPluginsBailResult("export specifier", statement, specifier.local.name, name, specifierIndex);
					break;
			}
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkExpression)
- description and source-code
```javascript
function walkExpression(expression) {
	if(this["walk" + expression.type])
		return this["walk" + expression.type](expression);
}
```
- example usage
```shell
...
	if(!result) return;
	if(result.isIdentifier()) return result.identifier;
	return;
};

Parser.prototype.walkClass = function walkClass(classy) {
	if(classy.superClass)
		this.walkExpression(classy.superClass);
	if(classy.body && classy.body.type === "ClassBody") {
		classy.body.body.forEach(function(methodDefinition) {
			if(methodDefinition.type === "MethodDefinition")
				this.walkMethodDefinition(methodDefinition);
		}, this);
	}
};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkExpressionStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExpressionStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkExpressionStatement)
- description and source-code
```javascript
function walkExpressionStatement(statement) {
	this.walkExpression(statement.expression);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkExpressions"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkExpressions (expressions)](#apidoc.element.webpack.Parser.prototype.walkExpressions)
- description and source-code
```javascript
function walkExpressions(expressions) {
	for(var expressionsIndex = 0, len = expressions.length; expressionsIndex < len; expressionsIndex++) {
		var expression = expressions[expressionsIndex];
		if(expression)
			this.walkExpression(expression);
	}
}
```
- example usage
```shell
...
	var argument = expression.argument;
	if(this["walk" + argument.type])
		return this["walk" + argument.type](argument);
};

Parser.prototype.walkArrayExpression = function walkArrayExpression(expression) {
	if(expression.elements)
		this.walkExpressions(expression.elements);
};

Parser.prototype.walkSpreadElement = function walkSpreadElement(expression) {
	if(expression.argument)
		this.walkExpression(expression.argument);
};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkForInStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkForInStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkForInStatement)
- description and source-code
```javascript
function walkForInStatement(statement) {
	if(statement.left.type === "VariableDeclaration")
		this.walkStatement(statement.left);
	else
		this.walkExpression(statement.left);
	this.walkExpression(statement.right);
	this.walkStatement(statement.body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkForOfStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkForOfStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkForOfStatement)
- description and source-code
```javascript
function walkForOfStatement(statement) {
	if(statement.left.type === "VariableDeclaration")
		this.walkStatement(statement.left);
	else
		this.walkExpression(statement.left);
	this.walkExpression(statement.right);
	this.walkStatement(statement.body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkForStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkForStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkForStatement)
- description and source-code
```javascript
function walkForStatement(statement) {
	if(statement.init) {
		if(statement.init.type === "VariableDeclaration")
			this.walkStatement(statement.init);
		else
			this.walkExpression(statement.init);
	}
	if(statement.test)
		this.walkExpression(statement.test);
	if(statement.update)
		this.walkExpression(statement.update);
	this.walkStatement(statement.body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkFunctionDeclaration"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkFunctionDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkFunctionDeclaration)
- description and source-code
```javascript
function walkFunctionDeclaration(statement) {
	this.scope.renames["$" + statement.id.name] = undefined;
	this.scope.definitions.push(statement.id.name);
	this.inScope(statement.params, function() {
		if(statement.body.type === "BlockStatement")
			this.walkStatement(statement.body);
		else
			this.walkExpression(statement.body);
	}.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkFunctionExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkFunctionExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkFunctionExpression)
- description and source-code
```javascript
function walkFunctionExpression(expression) {
	this.inScope(expression.params, function() {
		if(expression.body.type === "BlockStatement")
			this.walkStatement(expression.body);
		else
			this.walkExpression(expression.body);
	}.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkIdentifier"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkIdentifier (expression)](#apidoc.element.webpack.Parser.prototype.walkIdentifier)
- description and source-code
```javascript
function walkIdentifier(expression) {
	if(this.scope.definitions.indexOf(expression.name) === -1) {
		var result = this.applyPluginsBailResult1("expression " + (this.scope.renames["$" + expression.name] || expression.name), expression
);
		if(result === true)
			return;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkIfStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkIfStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkIfStatement)
- description and source-code
```javascript
function walkIfStatement(statement) {
	var result = this.applyPluginsBailResult1("statement if", statement);
	if(result === undefined) {
		this.walkExpression(statement.test);
		this.walkStatement(statement.consequent);
		if(statement.alternate)
			this.walkStatement(statement.alternate);
	} else {
		if(result)
			this.walkStatement(statement.consequent);
		else if(statement.alternate)
			this.walkStatement(statement.alternate);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkImportDeclaration"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkImportDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkImportDeclaration)
- description and source-code
```javascript
function walkImportDeclaration(statement) {
	var source = statement.source.value;
	this.applyPluginsBailResult("import", statement, source);
	statement.specifiers.forEach(function(specifier) {
		var name = specifier.local.name;
		this.scope.renames["$" + name] = undefined;
		this.scope.definitions.push(name);
		switch(specifier.type) {
			case "ImportDefaultSpecifier":
				this.applyPluginsBailResult("import specifier", statement, source, "default", name);
				break;
			case "ImportSpecifier":
				this.applyPluginsBailResult("import specifier", statement, source, specifier.imported.name, name);
				break;
			case "ImportNamespaceSpecifier":
				this.applyPluginsBailResult("import specifier", statement, source, null, name);
				break;
		}
	}, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkLabeledStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkLabeledStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkLabeledStatement)
- description and source-code
```javascript
function walkLabeledStatement(statement) {
	var result = this.applyPluginsBailResult1("label " + statement.label.name, statement);
	if(result !== true)
		this.walkStatement(statement.body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkLogicalExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkLogicalExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkLogicalExpression)
- description and source-code
```javascript
function walkLeftRightExpression(expression) {
		this.walkExpression(expression.left);
		this.walkExpression(expression.right);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkMemberExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkMemberExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkMemberExpression)
- description and source-code
```javascript
function walkMemberExpression(expression) {
	var expr = expression;
	var exprName = [];
	while(expr.type === "MemberExpression" &&
		expr.property.type === (expr.computed ? "Literal" : "Identifier")
	) {
		exprName.unshift(expr.property.name || expr.property.value);
		expr = expr.object;
	}
	if(expr.type === "Identifier" && this.scope.definitions.indexOf(expr.name) === -1) {
		exprName.unshift(this.scope.renames["$" + expr.name] || expr.name);
		var result = this.applyPluginsBailResult1("expression " + exprName.join("."), expression);
		if(result === true)
			return;
		exprName[exprName.length - 1] = "*";
		result = this.applyPluginsBailResult1("expression " + exprName.join("."), expression);
		if(result === true)
			return;
	}
	this.walkExpression(expression.object);
	if(expression.computed === true)
		this.walkExpression(expression.property);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkMethodDefinition"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkMethodDefinition (methodDefinition)](#apidoc.element.webpack.Parser.prototype.walkMethodDefinition)
- description and source-code
```javascript
function walkMethodDefinition(methodDefinition) {
	if(methodDefinition.computed && methodDefinition.key)
		this.walkExpression(methodDefinition.key);
	if(methodDefinition.value)
		this.walkExpression(methodDefinition.value);
}
```
- example usage
```shell
...

Parser.prototype.walkClass = function walkClass(classy) {
	if(classy.superClass)
		this.walkExpression(classy.superClass);
	if(classy.body && classy.body.type === "ClassBody") {
		classy.body.body.forEach(function(methodDefinition) {
			if(methodDefinition.type === "MethodDefinition")
				this.walkMethodDefinition(methodDefinition);
		}, this);
	}
};

Parser.prototype.walkMethodDefinition = function walkMethodDefinition(methodDefinition) {
	if(methodDefinition.computed && methodDefinition.key)
		this.walkExpression(methodDefinition.key);
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkNewExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkNewExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkNewExpression)
- description and source-code
```javascript
function walkNewExpression(expression) {
	this.walkExpression(expression.callee);
	if(expression.arguments)
		this.walkExpressions(expression.arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkObjectExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkObjectExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkObjectExpression)
- description and source-code
```javascript
function walkObjectExpression(expression) {
	for(var propIndex = 0, len = expression.properties.length; propIndex < len; propIndex++) {
		var prop = expression.properties[propIndex];
		if(prop.computed)
			this.walkExpression(prop.key);
		if(prop.shorthand)
			this.scope.inShorthand = true;
		this.walkExpression(prop.value);
		if(prop.shorthand)
			this.scope.inShorthand = false;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkObjectPattern"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkObjectPattern (pattern)](#apidoc.element.webpack.Parser.prototype.walkObjectPattern)
- description and source-code
```javascript
function walkObjectPattern(pattern) {
	for(var i = 0, len = pattern.properties.length; i < len; i++) {
		var prop = pattern.properties[i];
		if(prop) {
			if(prop.computed)
				this.walkExpression(prop.key);
			if(prop.value)
				this.walkPattern(prop.value);
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkPattern"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkPattern (pattern)](#apidoc.element.webpack.Parser.prototype.walkPattern)
- description and source-code
```javascript
function walkPattern(pattern) {
	if(pattern.type === "Identifier")
		return;
	if(this["walk" + pattern.type])
		this["walk" + pattern.type](pattern);
}
```
- example usage
```shell
...
					// renaming with "var a = b;"
					if(!_this.applyPluginsBailResult1("rename " + renameIdentifier, declarator.init)) {
						_this.scope.renames["$" + declarator.id.name] = _this.scope.renames["$" + renameIdentifier] || renameIdentifier;
						var idx = _this.scope.definitions.indexOf(declarator.id.name);
						if(idx >= 0) _this.scope.definitions.splice(idx, 1);
					}
				} else {
					_this.walkPattern(declarator.id);
					_this.enterPattern(declarator.id, function(name, decl) {
						if(!_this.applyPluginsBailResult1("var " + name, decl)) {
							_this.scope.renames["$" + name] = undefined;
							_this.scope.definitions.push(name);
						}
					});
					if(declarator.init)
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkRestElement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkRestElement (pattern)](#apidoc.element.webpack.Parser.prototype.walkRestElement)
- description and source-code
```javascript
function walkRestElement(pattern) {
	this.walkPattern(pattern.argument);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkReturnStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkReturnStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkReturnStatement)
- description and source-code
```javascript
function walkArgumentStatement(statement) {
		if(statement.argument)
			this.walkExpression(statement.argument);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkSequenceExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSequenceExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkSequenceExpression)
- description and source-code
```javascript
function walkSequenceExpression(expression) {
	if(expression.expressions)
		this.walkExpressions(expression.expressions);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkSpreadElement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSpreadElement (expression)](#apidoc.element.webpack.Parser.prototype.walkSpreadElement)
- description and source-code
```javascript
function walkSpreadElement(expression) {
	if(expression.argument)
		this.walkExpression(expression.argument);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkStatement)
- description and source-code
```javascript
function walkStatement(statement) {
	if(this.applyPluginsBailResult1("statement", statement) !== undefined) return;
	if(this["walk" + statement.type])
		this["walk" + statement.type](statement);
}
```
- example usage
```shell
...
		this.walkExpression(methodDefinition.value);
};

Parser.prototype.walkStatements = function walkStatements(statements) {
	for(var indexA = 0, lenA = statements.length; indexA < lenA; indexA++) {
		var statementA = statements[indexA];
		if(this.isHoistedStatement(statementA))
			this.walkStatement(statementA);
	}
	for(var indexB = 0, lenB = statements.length; indexB < lenB; indexB++) {
		var statementB = statements[indexB];
		if(!this.isHoistedStatement(statementB))
			this.walkStatement(statementB);
	}
};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkStatements"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkStatements (statements)](#apidoc.element.webpack.Parser.prototype.walkStatements)
- description and source-code
```javascript
function walkStatements(statements) {
	for(var indexA = 0, lenA = statements.length; indexA < lenA; indexA++) {
		var statementA = statements[indexA];
		if(this.isHoistedStatement(statementA))
			this.walkStatement(statementA);
	}
	for(var indexB = 0, lenB = statements.length; indexB < lenB; indexB++) {
		var statementB = statements[indexB];
		if(!this.isHoistedStatement(statementB))
			this.walkStatement(statementB);
	}
}
```
- example usage
```shell
...
	if(this.applyPluginsBailResult1("statement", statement) !== undefined) return;
	if(this["walk" + statement.type])
		this["walk" + statement.type](statement);
};

// Real Statements
Parser.prototype.walkBlockStatement = function walkBlockStatement(statement) {
	this.walkStatements(statement.body);
};

Parser.prototype.walkExpressionStatement = function walkExpressionStatement(statement) {
	this.walkExpression(statement.expression);
};

Parser.prototype.walkIfStatement = function walkIfStatement(statement) {
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkSwitchCases"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSwitchCases (switchCases)](#apidoc.element.webpack.Parser.prototype.walkSwitchCases)
- description and source-code
```javascript
function walkSwitchCases(switchCases) {
	for(var index = 0, len = switchCases.length; index < len; index++) {
		var switchCase = switchCases[index];

		if(switchCase.test) {
			this.walkExpression(switchCase.test);
		}
		this.walkStatements(switchCase.consequent);
	}
}
```
- example usage
```shell
...
Parser.prototype.walkWithStatement = function walkWithStatement(statement) {
	this.walkExpression(statement.object);
	this.walkStatement(statement.body);
};

Parser.prototype.walkSwitchStatement = function walkSwitchStatement(statement) {
	this.walkExpression(statement.discriminant);
	this.walkSwitchCases(statement.cases);
};

Parser.prototype.walkReturnStatement =
	Parser.prototype.walkThrowStatement = function walkArgumentStatement(statement) {
		if(statement.argument)
			this.walkExpression(statement.argument);
	};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkSwitchStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkSwitchStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkSwitchStatement)
- description and source-code
```javascript
function walkSwitchStatement(statement) {
	this.walkExpression(statement.discriminant);
	this.walkSwitchCases(statement.cases);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkTaggedTemplateExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkTaggedTemplateExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkTaggedTemplateExpression)
- description and source-code
```javascript
function walkTaggedTemplateExpression(expression) {
	if(expression.tag)
		this.walkExpression(expression.tag);
	if(expression.quasi && expression.quasi.expressions)
		this.walkExpressions(expression.quasi.expressions);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkTemplateLiteral"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkTemplateLiteral (expression)](#apidoc.element.webpack.Parser.prototype.walkTemplateLiteral)
- description and source-code
```javascript
function walkTemplateLiteral(expression) {
	if(expression.expressions)
		this.walkExpressions(expression.expressions);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkThrowStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkThrowStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkThrowStatement)
- description and source-code
```javascript
function walkArgumentStatement(statement) {
		if(statement.argument)
			this.walkExpression(statement.argument);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkTryStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkTryStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkTryStatement)
- description and source-code
```javascript
function walkTryStatement(statement) {
	if(this.scope.inTry) {
		this.walkStatement(statement.block);
	} else {
		this.scope.inTry = true;
		this.walkStatement(statement.block);
		this.scope.inTry = false;
	}
	if(statement.handler)
		this.walkCatchClause(statement.handler);
	if(statement.finalizer)
		this.walkStatement(statement.finalizer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkUnaryExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkUnaryExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkUnaryExpression)
- description and source-code
```javascript
function walkUnaryExpression(expression) {
	if(expression.operator === "typeof") {
		var expr = expression.argument;
		var exprName = [];
		while(expr.type === "MemberExpression" &&
			expr.property.type === (expr.computed ? "Literal" : "Identifier")
		) {
			exprName.unshift(expr.property.name || expr.property.value);
			expr = expr.object;
		}
		if(expr.type === "Identifier" && this.scope.definitions.indexOf(expr.name) === -1) {
			exprName.unshift(this.scope.renames["$" + expr.name] || expr.name);
			exprName = exprName.join(".");
			var result = this.applyPluginsBailResult1("typeof " + exprName, expression);
			if(result === true)
				return;
		}
	}
	this.walkExpression(expression.argument);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkUpdateExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkUpdateExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkUpdateExpression)
- description and source-code
```javascript
function walkUpdateExpression(expression) {
	this.walkExpression(expression.argument);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkVariableDeclaration"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkVariableDeclaration (statement)](#apidoc.element.webpack.Parser.prototype.walkVariableDeclaration)
- description and source-code
```javascript
function walkVariableDeclaration(statement) {
	if(statement.declarations)
		this.walkVariableDeclarators(statement.declarations);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkVariableDeclarators"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkVariableDeclarators (declarators)](#apidoc.element.webpack.Parser.prototype.walkVariableDeclarators)
- description and source-code
```javascript
function walkVariableDeclarators(declarators) {
	var _this = this;
	declarators.forEach(function(declarator) {
		switch(declarator.type) {
			case "VariableDeclarator":
				var renameIdentifier = declarator.init && _this.getRenameIdentifier(declarator.init);
				if(renameIdentifier && declarator.id.type === "Identifier" && _this.applyPluginsBailResult1("can-rename " + renameIdentifier
, declarator.init)) {
					// renaming with "var a = b;"
					if(!_this.applyPluginsBailResult1("rename " + renameIdentifier, declarator.init)) {
						_this.scope.renames["$" + declarator.id.name] = _this.scope.renames["$" + renameIdentifier] || renameIdentifier;
						var idx = _this.scope.definitions.indexOf(declarator.id.name);
						if(idx >= 0) _this.scope.definitions.splice(idx, 1);
					}
				} else {
					_this.walkPattern(declarator.id);
					_this.enterPattern(declarator.id, function(name, decl) {
						if(!_this.applyPluginsBailResult1("var " + name, decl)) {
							_this.scope.renames["$" + name] = undefined;
							_this.scope.definitions.push(name);
						}
					});
					if(declarator.init)
						_this.walkExpression(declarator.init);
				}
				break;
		}
	});
}
```
- example usage
```shell
...
	var source = statement.source.value;
	this.applyPluginsBailResult("export import", statement, source);
	this.applyPluginsBailResult("export import specifier", statement, source, null, null, 0);
};

Parser.prototype.walkVariableDeclaration = function walkVariableDeclaration(statement) {
	if(statement.declarations)
		this.walkVariableDeclarators(statement.declarations);
};

Parser.prototype.walkClassDeclaration = function walkClassDeclaration(statement) {
	this.scope.renames["$" + statement.id.name] = undefined;
	this.scope.definitions.push(statement.id.name);
	this.walkClass(statement);
};
...
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkWhileStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkWhileStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkWhileStatement)
- description and source-code
```javascript
function walkLoopStatement(statement) {
		this.walkExpression(statement.test);
		this.walkStatement(statement.body);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkWithStatement"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkWithStatement (statement)](#apidoc.element.webpack.Parser.prototype.walkWithStatement)
- description and source-code
```javascript
function walkWithStatement(statement) {
	this.walkExpression(statement.object);
	this.walkStatement(statement.body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.Parser.prototype.walkYieldExpression"></a>[function <span class="apidocSignatureSpan">webpack.Parser.prototype.</span>walkYieldExpression (expression)](#apidoc.element.webpack.Parser.prototype.walkYieldExpression)
- description and source-code
```javascript
function walkYieldExpression(expression) {
	if(expression.argument)
		this.walkExpression(expression.argument);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.ParserHelpers"></a>[module webpack.ParserHelpers](#apidoc.module.webpack.ParserHelpers)

#### <a name="apidoc.element.webpack.ParserHelpers.addParsedVariableToModule"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>addParsedVariableToModule (parser, name, expression)](#apidoc.element.webpack.ParserHelpers.addParsedVariableToModule)
- description and source-code
```javascript
addParsedVariableToModule = function (parser, name, expression) {
	if(!parser.state.current.addVariable) return false;
	var deps = [];
	parser.parse(expression, {
		current: {
			addDependency: function(dep) {
				dep.userRequest = name;
				deps.push(dep);
			}
		},
		module: parser.state.module
	});
	parser.state.current.addVariable(name, expression, deps);
	return true;
}
```
- example usage
```shell
...
						let expression = 'require(${JSON.stringify(request[0])})';
						if(scopedName) {
							nameIdentifier = '__webpack_provided_${name.replace(/\./g, "_dot_")}';
						}
						if(request.length > 1) {
							expression += request.slice(1).map(r => '[${JSON.stringify(r)}]').join("");
						}
						if(!ParserHelpers.addParsedVariableToModule(this, nameIdentifier, expression)) {
							return false;
						}
						if(scopedName) {
							ParserHelpers.toConstantDependency(nameIdentifier).bind(this)(expr);
						}
						return true;
					});
...
```

#### <a name="apidoc.element.webpack.ParserHelpers.approve"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>approve ()](#apidoc.element.webpack.ParserHelpers.approve)
- description and source-code
```javascript
function approve() {
	return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ParserHelpers.evaluateToBoolean"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>evaluateToBoolean (value)](#apidoc.element.webpack.ParserHelpers.evaluateToBoolean)
- description and source-code
```javascript
evaluateToBoolean = function (value) {
	return function booleanExpression(expr) {
		return new BasicEvaluatedExpression().setBoolean(value).setRange(expr.range);
	};
}
```
- example usage
```shell
...
			parser.plugin("expression module.id", ParserHelpers.toConstantDependency("module.i"));
			parser.plugin("expression module.exports", function() {
				var module = this.state.module;
				var isHarmony = module.meta && module.meta.harmonyModule;
				if(!isHarmony)
					return true;
			});
			parser.plugin("evaluate Identifier module.hot", ParserHelpers.evaluateToBoolean(false));
			parser.plugin("expression module", function() {
				var module = this.state.module;
				var isHarmony = module.meta && module.meta.harmonyModule;
				var moduleJsPath = path.join(__dirname, "..", "buildin", isHarmony ? "harmony-module.js" : "module.js");
				if(module.context) {
					moduleJsPath = path.relative(this.state.module.context, moduleJsPath);
					if(!/^[A-Z]:/i.test(moduleJsPath)) {
...
```

#### <a name="apidoc.element.webpack.ParserHelpers.evaluateToString"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>evaluateToString (value)](#apidoc.element.webpack.ParserHelpers.evaluateToString)
- description and source-code
```javascript
evaluateToString = function (value) {
	return function stringExpression(expr) {
		return new BasicEvaluatedExpression().setString(value).setRange(expr.range);
	};
}
```
- example usage
```shell
...
		compiler.plugin("compilation", (compilation, params) => {
			compilation.dependencyFactories.set(ConstDependency, new NullFactory());
			compilation.dependencyTemplates.set(ConstDependency, new ConstDependency.Template());

			params.normalModuleFactory.plugin("parser", parser => {
				Object.keys(REPLACEMENTS).forEach(key => {
					parser.plugin('expression ${key}', ParserHelpers.toConstantDependency(REPLACEMENTS[key]));
					parser.plugin('evaluate typeof ${key}', ParserHelpers.evaluateToString(REPLACEMENT_TYPES[key]));
				});
				IGNORES.forEach(key => {
					parser.plugin(key, ParserHelpers.skipTraversal);
				});
			});
		});
	}
...
```

#### <a name="apidoc.element.webpack.ParserHelpers.expressionIsUnsupported"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>expressionIsUnsupported (message)](#apidoc.element.webpack.ParserHelpers.expressionIsUnsupported)
- description and source-code
```javascript
expressionIsUnsupported = function (message) {
	return function unsupportedExpression(expr) {
		var dep = new ConstDependency("(void 0)", expr.range);
		dep.loc = expr.loc;
		this.state.current.addDependency(dep);
		if(!this.state.module) return;
		this.state.module.warnings.push(new UnsupportedFeatureWarning(this.state.module, message));
		return true;
	};
}
```
- example usage
```shell
...
			parser.plugin("evaluate Identifier __dirname", function(expr) {
				if(!this.state.module) return;
				return ParserHelpers.evaluateToString(this.state.module.context)(expr);
			});
			parser.plugin("expression require.main", ParserHelpers.toConstantDependency("__webpack_require__.c[__webpack_require__.s]"));
			parser.plugin(
				"expression require.extensions",
				ParserHelpers.expressionIsUnsupported("require.extensions is not supported by webpack. Use a loader instead.")
			);
			parser.plugin("expression module.loaded", ParserHelpers.toConstantDependency("module.l"));
			parser.plugin("expression module.id", ParserHelpers.toConstantDependency("module.i"));
			parser.plugin("expression module.exports", function() {
				var module = this.state.module;
				var isHarmony = module.meta && module.meta.harmonyModule;
				if(!isHarmony)
...
```

#### <a name="apidoc.element.webpack.ParserHelpers.requireFileAsExpression"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>requireFileAsExpression (context, pathToModule)](#apidoc.element.webpack.ParserHelpers.requireFileAsExpression)
- description and source-code
```javascript
requireFileAsExpression = function (context, pathToModule) {
	var moduleJsPath = path.relative(context, pathToModule);
	if(!/^[A-Z]:/i.test(moduleJsPath)) {
		moduleJsPath = "./" + moduleJsPath.replace(/\\/g, "/");
	}
	return "require(" + JSON.stringify(moduleJsPath) + ")";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ParserHelpers.skipTraversal"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>skipTraversal ()](#apidoc.element.webpack.ParserHelpers.skipTraversal)
- description and source-code
```javascript
function skipTraversal() {
	return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.ParserHelpers.toConstantDependency"></a>[function <span class="apidocSignatureSpan">webpack.ParserHelpers.</span>toConstantDependency (value)](#apidoc.element.webpack.ParserHelpers.toConstantDependency)
- description and source-code
```javascript
toConstantDependency = function (value) {
	return function constDependency(expr) {
		var dep = new ConstDependency(value, expr.range);
		dep.loc = expr.loc;
		this.state.current.addDependency(dep);
		return true;
	};
}
```
- example usage
```shell
...
	apply(compiler) {
		compiler.plugin("compilation", (compilation, params) => {
			compilation.dependencyFactories.set(ConstDependency, new NullFactory());
			compilation.dependencyTemplates.set(ConstDependency, new ConstDependency.Template());

			params.normalModuleFactory.plugin("parser", parser => {
				Object.keys(REPLACEMENTS).forEach(key => {
					parser.plugin('expression ${key}', ParserHelpers.toConstantDependency(REPLACEMENTS[key]));
					parser.plugin('evaluate typeof ${key}', ParserHelpers.evaluateToString(REPLACEMENT_TYPES[key]));
				});
				IGNORES.forEach(key => {
					parser.plugin(key, ParserHelpers.skipTraversal);
				});
			});
		});
...
```



# <a name="apidoc.module.webpack.SizeFormatHelpers"></a>[module webpack.SizeFormatHelpers](#apidoc.module.webpack.SizeFormatHelpers)

#### <a name="apidoc.element.webpack.SizeFormatHelpers.formatSize"></a>[function <span class="apidocSignatureSpan">webpack.SizeFormatHelpers.</span>formatSize (size <= 0)](#apidoc.element.webpack.SizeFormatHelpers.formatSize)
- description and source-code
```javascript
size => {
	if(size <= 0) {
		return "0 bytes";
	}

	const abbreviations = ["bytes", "kB", "MB", "GB"];
	const index = Math.floor(Math.log(size) / Math.log(1000));

	return '${+(size / Math.pow(1000, index)).toPrecision(3)} ${abbreviations[index]}';
}
```
- example usage
```shell
...
				}]
			];
			obj.assets.forEach(asset => {
				t.push([{
					value: asset.name,
					color: getAssetColor(asset, colors.green)
				}, {
					value: SizeFormatHelpers.formatSize(asset.size),
					color: getAssetColor(asset, colors.normal)
				}, {
					value: asset.chunks.join(", "),
					color: colors.bold
				}, {
					value: asset.emitted ? "[emitted]" : "",
					color: colors.green
...
```



# <a name="apidoc.module.webpack.SourceMapDevToolPlugin"></a>[module webpack.SourceMapDevToolPlugin](#apidoc.module.webpack.SourceMapDevToolPlugin)

#### <a name="apidoc.element.webpack.SourceMapDevToolPlugin.SourceMapDevToolPlugin"></a>[function <span class="apidocSignatureSpan">webpack.</span>SourceMapDevToolPlugin (options)](#apidoc.element.webpack.SourceMapDevToolPlugin.SourceMapDevToolPlugin)
- description and source-code
```javascript
function SourceMapDevToolPlugin(options) {
	if(arguments.length > 1)
		throw new Error("SourceMapDevToolPlugin only takes one argument (pass an options object)");
	if(typeof options === "string") {
		options = {
			sourceMapFilename: options
		};
	}
	if(!options) options = {};
	this.sourceMapFilename = options.filename;
	this.sourceMappingURLComment = options.append === false ? false : options.append || "\n//# sourceMappingURL=[url]";
	this.moduleFilenameTemplate = options.moduleFilenameTemplate || "webpack:///[resourcePath]";
	this.fallbackModuleFilenameTemplate = options.fallbackModuleFilenameTemplate || "webpack:///[resourcePath]?[hash]";
	this.options = options;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.SourceMapDevToolPlugin.prototype"></a>[module webpack.SourceMapDevToolPlugin.prototype](#apidoc.module.webpack.SourceMapDevToolPlugin.prototype)

#### <a name="apidoc.element.webpack.SourceMapDevToolPlugin.prototype.apply"></a>[function <span class="apidocSignatureSpan">webpack.SourceMapDevToolPlugin.prototype.</span>apply (compiler)](#apidoc.element.webpack.SourceMapDevToolPlugin.prototype.apply)
- description and source-code
```javascript
apply = function (compiler) {
	var sourceMapFilename = this.sourceMapFilename;
	var sourceMappingURLComment = this.sourceMappingURLComment;
	var moduleFilenameTemplate = this.moduleFilenameTemplate;
	var fallbackModuleFilenameTemplate = this.fallbackModuleFilenameTemplate;
	var requestShortener = new RequestShortener(compiler.context);
	var options = this.options;
	options.test = options.test || /\.(js|css)($|\?)/i;
	compiler.plugin("compilation", function(compilation) {
		new SourceMapDevToolModuleOptionsPlugin(options).apply(compilation);
		compilation.plugin("after-optimize-chunk-assets", function(chunks) {
			var allModules = [];
			var allModuleFilenames = [];
			var tasks = [];
			chunks.forEach(function(chunk) {
				chunk.files.filter(ModuleFilenameHelpers.matchObject.bind(undefined, options)).map(function(file) {
					var asset = this.assets[file];
					if(asset.__SourceMapDevToolData) {
						var data = asset.__SourceMapDevToolData;
						for(var cachedFile in data) {
							this.assets[cachedFile] = data[cachedFile];
							if(cachedFile !== file)
								chunk.files.push(cachedFile);
						}
						return;
					}
					var source;
					var sourceMap;
					if(asset.sourceAndMap) {
						var sourceAndMap = asset.sourceAndMap(options);
						sourceMap = sourceAndMap.map;
						source = sourceAndMap.source;
					} else {
						sourceMap = asset.map(options);
						source = asset.source();
					}
					if(sourceMap) {
						return {
							chunk: chunk,
							file: file,
							asset: asset,
							source: source,
							sourceMap: sourceMap
						};
					}
				}, this).filter(Boolean).map(function(task) {
					var modules = task.sourceMap.sources.map(function(source) {
						var module = compilation.findModule(source);
						return module || source;
					});
					var moduleFilenames = modules.map(function(module) {
						return ModuleFilenameHelpers.createFilename(module, moduleFilenameTemplate, requestShortener);
					});
					task.modules = modules;
					task.moduleFilenames = moduleFilenames;
					return task;
				}, this).forEach(function(task) {
					allModules = allModules.concat(task.modules);
					allModuleFilenames = allModuleFilenames.concat(task.moduleFilenames);
					tasks.push(task);
				}, this);
			}, this);
			allModuleFilenames = ModuleFilenameHelpers.replaceDuplicates(allModuleFilenames, function(filename, i) {
				return ModuleFilenameHelpers.createFilename(allModules[i], fallbackModuleFilenameTemplate, requestShortener);
			}, function(ai, bi) {
				var a = allModules[ai];
				var b = allModules[bi];
				a = !a ? "" : typeof a === "string" ? a : a.identifier();
				b = !b ? "" : typeof b === "string" ? b : b.identifier();
				return a.length - b.length;
			});
			allModuleFilenames = ModuleFilenameHelpers.replaceDuplicates(allModuleFilenames, function(filename, i, n) {
				for(var j = 0; j < n; j++)
					filename += "*";
				return filename;
			});
			tasks.forEach(function(task) {
				task.moduleFilenames = allModuleFilenames.slice(0, task.moduleFilenames.length);
				allModuleFilenames = allModuleFilenames.slice(task.moduleFilenames.length);
			}, this);
			tasks.forEach(function(task) {
				var chunk = task.chunk;
				var file = task.file;
				var asset = task.asset;
				var sourceMap = task.sourceMap;
				var source = task.source;
				var moduleFilenames = task.moduleFilenames;
				var modules = task.modules;
				sourceMap.sources = moduleFilenames;
				if(sourceMap.sourcesContent && !options.noSources) {
					sourceMap.sourcesContent = sourceMap.sourcesContent.map(function(content, i) {
						return content + "\n\n\n" + ModuleFilenameHelpers.createFooter(modules[i], requestShortener);
					});
				} else {
					sourceMap.sourcesContent = undefined;
				}
				sourceMap.sourceRoot = options.sourceRoot || "";
				sourceMap.file = file;
				asset.__SourceMapDevToolData = {};
				var currentSourceMappingURLComment = sourceMappingURLComment;
				if(currentSourceMappingURLComment !== false && /\.css($|\?)/i. ...
```
- example usage
```shell
...
		this.cache = cache || {};
		this.FS_ACCURENCY = 2000;
	}

	apply(compiler) {
		if(Array.isArray(compiler.compilers)) {
			compiler.compilers.forEach((c, idx) => {
				c.apply(new CachePlugin(this.cache[idx] = this.cache[idx] || {}));
			});
		} else {
			compiler.plugin("compilation", compilation => {
				if(!compilation.notCacheable) {
					compilation.cache = this.cache;
				} else if(this.watching) {
					compilation.warnings.push(
...
```



# <a name="apidoc.module.webpack.optimize"></a>[module webpack.optimize](#apidoc.module.webpack.optimize)

#### <a name="apidoc.element.webpack.optimize.AggressiveMergingPlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>AggressiveMergingPlugin (options)](#apidoc.element.webpack.optimize.AggressiveMergingPlugin)
- description and source-code
```javascript
class AggressiveMergingPlugin {
	constructor(options) {
		if(options !== undefined && typeof options !== "object" || Array.isArray(options)) {
			throw new Error("Argument should be an options object. To use defaults, pass in nothing.\nFor more info on options, see https
://webpack.js.org/plugins/");
		}
		this.options = options || {};
	}

	apply(compiler) {
		const options = this.options;
		const minSizeReduce = options.minSizeReduce || 1.5;

		function getParentsWeight(chunk) {
			return chunk.parents.map((p) => {
				return p.isInitial() ? options.entryChunkMultiplicator || 10 : 1;
			}).reduce((a, b) => {
				return a + b;
			}, 0);
		}
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("optimize-chunks-advanced", (chunks) => {
				let combinations = [];
				chunks.forEach((a, idx) => {
					if(a.isInitial()) return;
					for(let i = 0; i < idx; i++) {
						const b = chunks[i];
						if(b.isInitial()) continue;
						combinations.push([b, a]);
					}
				});

				combinations.forEach((pair) => {
					const a = pair[0].size({
						chunkOverhead: 0
					});
					const b = pair[1].size({
						chunkOverhead: 0
					});
					const ab = pair[0].integratedSize(pair[1], {
						chunkOverhead: 0
					});
					pair.push({
						a: a,
						b: b,
						ab: ab
					});
					let newSize;
					if(ab === false) {
						pair.unshift(false);
					} else if(options.moveToParents) {
						const aOnly = ab - b;
						const bOnly = ab - a;
						const common = a + b - ab;
						newSize = common + getParentsWeight(pair[0]) * aOnly + getParentsWeight(pair[1]) * bOnly;
						pair.push({
							aOnly: aOnly,
							bOnly: bOnly,
							common: common,
							newSize: newSize
						});
					} else {
						newSize = ab;
					}

					pair.unshift((a + b) / newSize);
				});
				combinations = combinations.filter((pair) => {
					return pair[0] !== false;
				});
				combinations.sort((a, b) => {
					return b[0] - a[0];
				});

				const pair = combinations[0];

				if(!pair) return;
				if(pair[0] < minSizeReduce) return;

				if(options.moveToParents) {
					const commonModules = pair[1].modules.filter((m) => {
						return pair[2].modules.indexOf(m) >= 0;
					});
					const aOnlyModules = pair[1].modules.filter((m) => {
						return commonModules.indexOf(m) < 0;
					});
					const bOnlyModules = pair[2].modules.filter((m) => {
						return commonModules.indexOf(m) < 0;
					});
					aOnlyModules.forEach((m) => {
						pair[1].removeModule(m);
						m.removeChunk(pair[1]);
						pair[1].parents.forEach((c) => {
							c.addModule(m);
							m.addChunk(c);
						});
					});
					bOnlyModules.forEach((m) => {
						pair[2].removeModule(m);
						m.removeChunk(pair[2]);
						pair[2].parents.forEach((c) => {
							c.addModule(m);
							m.addChunk(c);
						});
					});
				}
				if(pair[1].integrate(pair[2], "aggressive-merge")) {
					chunks.splice(chunks.indexOf(pair[2]), 1);
					return true;
				}
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.AggressiveSplittingPlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>AggressiveSplittingPlugin (options)](#apidoc.element.webpack.optimize.AggressiveSplittingPlugin)
- description and source-code
```javascript
class AggressiveSplittingPlugin {
	constructor(options) {
		this.options = options || {};
		if(typeof this.options.minSize !== "number") this.options.minSize = 30 * 1024;
		if(typeof this.options.maxSize !== "number") this.options.maxSize = 50 * 1024;
		if(typeof this.options.chunkOverhead !== "number") this.options.chunkOverhead = 0;
		if(typeof this.options.entryChunkMultiplicator !== "number") this.options.entryChunkMultiplicator = 1;
	}
	apply(compiler) {
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("optimize-chunks-advanced", (chunks) => {
				const savedSplits = compilation.records && compilation.records.aggressiveSplits || [];
				const usedSplits = compilation._aggressiveSplittingSplits ?
					savedSplits.concat(compilation._aggressiveSplittingSplits) : savedSplits;

				const minSize = this.options.minSize;
				const maxSize = this.options.maxSize;
				// 1. try to restore to recorded splitting
				for(let j = 0; j < usedSplits.length; j++) {
					const splitData = usedSplits[j];
					for(let i = 0; i < chunks.length; i++) {
						const chunk = chunks[i];
						const chunkModuleNames = chunk.modules.map(makeRelative(compiler.context));

						if(chunkModuleNames.length < splitData.modules.length)
							continue;
						const moduleIndicies = splitData.modules.map(toIndexOf(chunkModuleNames));
						const hasAllModules = moduleIndicies.every((idx) => {
							return idx >= 0;
						});
						if(hasAllModules) {
							if(chunkModuleNames.length > splitData.modules.length) {
								const selectedModules = moduleIndicies.map(toChunkModuleIndices(chunk.modules));
								const newChunk = compilation.addChunk();
								selectedModules.forEach(moveModuleBetween(chunk, newChunk));
								chunk.split(newChunk);
								chunk.name = null;
								newChunk._fromAggressiveSplitting = true;
								if(j < savedSplits.length)
									newChunk._fromAggressiveSplittingIndex = j;
								if(typeof splitData.id === "number") newChunk.id = splitData.id;
								newChunk.origins = chunk.origins.map(copyWithReason);
								chunk.origins = chunk.origins.map(copyWithReason);
								return true;
							} else {
								if(j < savedSplits.length)
									chunk._fromAggressiveSplittingIndex = j;
								chunk.name = null;
								if(typeof splitData.id === "number") chunk.id = splitData.id;
							}
						}
					}
				}
				// 2. for any other chunk which isn't splitted yet, split it
				for(let i = 0; i < chunks.length; i++) {
					const chunk = chunks[i];
					const size = chunk.size(this.options);
					if(size > maxSize && chunk.modules.length > 1) {
						const newChunk = compilation.addChunk();
						const modules = chunk.modules
							.filter(isNotAEntryModule(chunk.entryModule))
							.sort((a, b) => {
								a = a.identifier();
								b = b.identifier();
								if(a > b) return 1;
								if(a < b) return -1;
								return 0;
							});
						for(let k = 0; k < modules.length; k++) {
							chunk.moveModule(modules[k], newChunk);
							const newSize = newChunk.size(this.options);
							const chunkSize = chunk.size(this.options);
							// break early if it's fine
							if(chunkSize < maxSize && newSize < maxSize && newSize >= minSize && chunkSize >= minSize)
								break;
							if(newSize > maxSize && k === 0) {
								// break if there is a single module which is bigger than maxSize
								break;
							}
							if(newSize > maxSize || chunkSize < minSize) {
								// move it back
								newChunk.moveModule(modules[k], chunk);
								// check if it's fine now
								if(newSize < maxSize && newSize >= minSize && chunkSize >= minSize)
									break;
							}
						}
						if(newChunk.modules.length > 0) {
							chunk.split(newChunk);
							chunk.name = null;
							newChunk.origins = chunk.origins.map(copyWithReason);
							chunk.origins = chunk.origins.map(copyWithReason);
							compilation._aggressiveSplittingSplits = (compilation._aggressiveSplittingSplits || []).concat({ ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.ChunkModuleIdRangePlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>ChunkModuleIdRangePlugin (options)](#apidoc.element.webpack.optimize.ChunkModuleIdRangePlugin)
- description and source-code
```javascript
class ChunkModuleIdRangePlugin {
	constructor(options) {
		this.options = options;
	}
	apply(compiler) {
		const options = this.options;
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("module-ids", (modules) => {
				const chunk = this.chunks.filter((chunk) => {
					return chunk.name === options.name;
				})[0];
				if(!chunk) throw new Error("ChunkModuleIdRangePlugin: Chunk with name '" + options.name + "' was not found");
				let currentId = options.start;
				let chunkModules;
				if(options.order) {
					chunkModules = chunk.modules.slice();
					switch(options.order) {
						case "index":
							chunkModules.sort((a, b) => {
								return a.index - b.index;
							});
							break;
						case "index2":
							chunkModules.sort((a, b) => {
								return a.index2 - b.index2;
							});
							break;
						default:
							throw new Error("ChunkModuleIdRangePlugin: unexpected value of order");
					}

				} else {
					chunkModules = modules.filter((m) => {
						return m.chunks.indexOf(chunk) >= 0;
					});
				}

				for(let i = 0; i < chunkModules.length; i++) {
					const m = chunkModules[i];
					if(m.id === null) {
						m.id = currentId++;
					}
					if(options.end && currentId > options.end)
						break;
				}
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.CommonsChunkPlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>CommonsChunkPlugin (options)](#apidoc.element.webpack.optimize.CommonsChunkPlugin)
- description and source-code
```javascript
class CommonsChunkPlugin {
	constructor(options) {
		if(arguments.length > 1) {
			throw new Error('Deprecation notice: CommonsChunkPlugin now only takes a single argument. Either an options
object *or* the name of the chunk.
Example: if your old code looked like this:
	new webpack.optimize.CommonsChunkPlugin('vendor', 'vendor.bundle.js')
You would change it to:
	new webpack.optimize.CommonsChunkPlugin({ name: 'vendor', filename: 'vendor.bundle.js' })
The available options are:
	name: string
	names: string[]
	filename: string
	minChunks: number
	chunks: string[]
	children: boolean
	async: boolean
	minSize: number');
		}

		const normalizedOptions = this.normalizeOptions(options);

		this.chunkNames = normalizedOptions.chunkNames;
		this.filenameTemplate = normalizedOptions.filenameTemplate;
		this.minChunks = normalizedOptions.minChunks;
		this.selectedChunks = normalizedOptions.selectedChunks;
		this.children = normalizedOptions.children;
		this.async = normalizedOptions.async;
		this.minSize = normalizedOptions.minSize;
		this.ident = __filename + (nextIdent++);
	}

	normalizeOptions(options) {
		if(Array.isArray(options)) {
			return {
				chunkNames: options,
			};
		}

		if(typeof options === "string") {
			return {
				chunkNames: [options],
			};
		}

		// options.children and options.chunk may not be used together
		if(options.children && options.chunks) {
			throw new Error("You can't and it does not make any sense to use \"children\" and \"chunk\" options together.");
		}

		/**
		 * options.async and options.filename are also not possible together
		 * as filename specifies how the chunk is called but "async" implies
		 * that webpack will take care of loading this file.
		 */
		if(options.async && options.filename) {
			throw new Error('You can not specify a filename if you use the \"async\" option.
You can however specify the name of the async chunk by passing the desired string as the \"async\" option.');
		}

		/**
		 * Make sure this is either an array or undefined.
		 * "name" can be a string and
		 * "names" a string or an array
		 */
		const chunkNames = options.name || options.names ? [].concat(options.name || options.names) : undefined;
		return {
			chunkNames: chunkNames,
			filenameTemplate: options.filename,
			minChunks: options.minChunks,
			selectedChunks: options.chunks,
			children: options.children,
			async: options.async,
			minSize: options.minSize
		};
	}

	apply(compiler) {
		compiler.plugin("this-compilation", (compilation) => {
			compilation.plugin(["optimize-chunks", "optimize-extracted-chunks"], (chunks) => {
				// only optimize once
				if(compilation[this.ident]) return;
				compilation[this.ident] = true;

				/**
				 * Creates a list of "common"" chunks based on the options.
				 * The list is made up of preexisting or newly created chunks.
				 * - If chunk has the name as specified in the chunkNames it is put in the list
				 * - If no chunk with the name as given in chunkNames exists a new chunk is created and added to the list
				 *
				 * These chunks are the "targets" for extracted modules.
				 */
				const targetChunks = this.getTargetChunks(chunks, compilation, this.chunkNames, this.children, this.async);

				// iterate over all our new chunks
				targetChunks.forEach((targetChunk, idx) => {

					/**
					 * These chunks are subject to get "common" modules extracted and moved to the common chunk
					 */
					const affectedChunks = this.getAffectedChunks(compilation, chunks, targetChunk, targetChunks, idx, this.selectedChunks, this
.async, this.children);

					// bail if no chunk is affected
					if(!affectedChunks) {
						return;
					}

					// If we are async create an async chunk now
					// override the "commonChunk" with the newly created async one and use it as commonChunk from now on
					let asyncChunk;
					if(this.async) {
						asyncChunk = this.createAsyncChunk(compilation, this.async, targetChunk);
						targetChunk = asyncChunk;
					} ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.DedupePlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>DedupePlugin (compiler)](#apidoc.element.webpack.optimize.DedupePlugin)
- description and source-code
```javascript
class DedupePlugin {
	apply(compiler) {
		compiler.plugin("compilation", (compilation) => {
			compilation.warnings.push(new Error("DedupePlugin: This plugin was removed from webpack. Remove it from your configuration."));
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.LimitChunkCountPlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>LimitChunkCountPlugin (options)](#apidoc.element.webpack.optimize.LimitChunkCountPlugin)
- description and source-code
```javascript
class LimitChunkCountPlugin {
	constructor(options) {
		if(options !== undefined && typeof options !== "object" || Array.isArray(options)) {
			throw new Error("Argument should be an options object.\nFor more info on options, see https://webpack.js.org/plugins/");
		}
		this.options = options || {};
	}
	apply(compiler) {
		const options = this.options;
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("optimize-chunks-advanced", (chunks) => {
				const maxChunks = options.maxChunks;
				if(!maxChunks) return;
				if(maxChunks < 1) return;
				if(chunks.length <= maxChunks) return;

				if(chunks.length > maxChunks) {
					const sortedExtendedPairCombinations = chunks.reduce((combinations, a, idx) => {
						// create combination pairs
						for(let i = 0; i < idx; i++) {
							const b = chunks[i];
							combinations.push([b, a]);
						}
						return combinations;
					}, []).map((pair) => {
						// extend combination pairs with size and integrated size
						const a = pair[0].size(options);
						const b = pair[1].size(options);
						const ab = pair[0].integratedSize(pair[1], options);
						return [a + b - ab, ab, pair[0], pair[1], a, b];
					}).filter((extendedPair) => {
						// filter pairs that do not have an integratedSize
						// meaning they can NOT be integrated!
						return extendedPair[1] !== false;
					}).sort((a, b) => { // sadly javascript does an inplace sort here
						// sort them by size
						const diff = b[0] - a[0];
						if(diff !== 0) return diff;
						return a[1] - b[1];
					});

					const pair = sortedExtendedPairCombinations[0];

					if(pair && pair[2].integrate(pair[3], "limit")) {
						chunks.splice(chunks.indexOf(pair[3]), 1);
						return true;
					}
				}
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.MinChunkSizePlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>MinChunkSizePlugin (options)](#apidoc.element.webpack.optimize.MinChunkSizePlugin)
- description and source-code
```javascript
class MinChunkSizePlugin {
	constructor(options) {
		if(typeof options !== "object" || Array.isArray(options)) {
			throw new Error("Argument should be an options object.\nFor more info on options, see https://webpack.js.org/plugins/");
		}
		this.options = options;
	}

	apply(compiler) {
		const options = this.options;
		const minChunkSize = options.minChunkSize;
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("optimize-chunks-advanced", (chunks) => {
				const equalOptions = {
					chunkOverhead: 1,
					entryChunkMultiplicator: 1
				};

				const sortedSizeFilteredExtendedPairCombinations = chunks.reduce((combinations, a, idx) => {
					// create combination pairs
					for(let i = 0; i < idx; i++) {
						const b = chunks[i];
						combinations.push([b, a]);
					}
					return combinations;
				}, []).filter((pair) => {
					// check if one of the chunks sizes is smaller than the minChunkSize
					const p0SmallerThanMinChunkSize = pair[0].size(equalOptions) < minChunkSize;
					const p1SmallerThanMinChunkSize = pair[1].size(equalOptions) < minChunkSize;
					return p0SmallerThanMinChunkSize || p1SmallerThanMinChunkSize;
				}).map((pair) => {
					// extend combination pairs with size and integrated size
					const a = pair[0].size(options);
					const b = pair[1].size(options);
					const ab = pair[0].integratedSize(pair[1], options);
					return [a + b - ab, ab, pair[0], pair[1]];
				}).filter((pair) => {
					// filter pairs that do not have an integratedSize
					// meaning they can NOT be integrated!
					return pair[1] !== false;
				}).sort((a, b) => { // sadly javascript does an inplace sort here
					// sort by size
					const diff = b[0] - a[0];
					if(diff !== 0) return diff;
					return a[1] - b[1];
				});

				if(sortedSizeFilteredExtendedPairCombinations.length === 0) return;

				const pair = sortedSizeFilteredExtendedPairCombinations[0];

				pair[2].integrate(pair[3], "min-size");
				chunks.splice(chunks.indexOf(pair[3]), 1);
				return true;
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.OccurrenceOrderPlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>OccurrenceOrderPlugin (preferEntry)](#apidoc.element.webpack.optimize.OccurrenceOrderPlugin)
- description and source-code
```javascript
class OccurrenceOrderPlugin {
	constructor(preferEntry) {
		if(preferEntry !== undefined && typeof preferEntry !== "boolean") {
			throw new Error("Argument should be a boolean.\nFor more info on this plugin, see https://webpack.js.org/plugins/");
		}
		this.preferEntry = preferEntry;
	}
	apply(compiler) {
		const preferEntry = this.preferEntry;
		compiler.plugin("compilation", (compilation) => {
			compilation.plugin("optimize-module-order", (modules) => {
				function entryChunks(m) {
					return m.chunks.map((c) => {
						const sum = (c.isInitial() ? 1 : 0) + (c.entryModule === m ? 1 : 0);
						return sum;
					}).reduce((a, b) => {
						return a + b;
					}, 0);
				}

				function occursInEntry(m) {
					if(typeof m.__OccurenceOrderPlugin_occursInEntry === "number") return m.__OccurenceOrderPlugin_occursInEntry;
					const result = m.reasons.map((r) => {
						if(!r.module) return 0;
						return entryChunks(r.module);
					}).reduce((a, b) => {
						return a + b;
					}, 0) + entryChunks(m);
					return m.__OccurenceOrderPlugin_occursInEntry = result;
				}

				function occurs(m) {
					if(typeof m.__OccurenceOrderPlugin_occurs === "number") return m.__OccurenceOrderPlugin_occurs;
					const result = m.reasons.map((r) => {
						if(!r.module) return 0;
						return r.module.chunks.length;
					}).reduce((a, b) => {
						return a + b;
					}, 0) + m.chunks.length + m.chunks.filter((c) => {
						return c.entryModule === m;
					}).length;
					return m.__OccurenceOrderPlugin_occurs = result;
				}
				modules.sort((a, b) => {
					if(preferEntry) {
						const aEntryOccurs = occursInEntry(a);
						const bEntryOccurs = occursInEntry(b);
						if(aEntryOccurs > bEntryOccurs) return -1;
						if(aEntryOccurs < bEntryOccurs) return 1;
					}
					const aOccurs = occurs(a);
					const bOccurs = occurs(b);
					if(aOccurs > bOccurs) return -1;
					if(aOccurs < bOccurs) return 1;
					if(a.identifier() > b.identifier()) return 1;
					if(a.identifier() < b.identifier()) return -1;
					return 0;
				});
				// TODO refactor to Map
				modules.forEach((m) => {
					m.__OccurenceOrderPlugin_occursInEntry = undefined;
					m.__OccurenceOrderPlugin_occurs = undefined;
				});
			});
			compilation.plugin("optimize-chunk-order", (chunks) => {
				function occursInEntry(c) {
					if(typeof c.__OccurenceOrderPlugin_occursInEntry === "number") return c.__OccurenceOrderPlugin_occursInEntry;
					const result = c.parents.filter((p) => {
						return p.isInitial();
					}).length;
					return c.__OccurenceOrderPlugin_occursInEntry = result;
				}

				function occurs(c) {
					return c.blocks.length;
				}
				chunks.forEach((c) => {
					c.modules.sort((a, b) => {
						if(a.identifier() > b.identifier()) return 1;
						if(a.identifier() < b.identifier()) return -1;
						return 0;
					});
				});
				chunks.sort((a, b) => {
					const aEntryOccurs = occursInEntry(a);
					const bEntryOccurs = occursInEntry(b);
					if(aEntryOccurs > bEntryOccurs) return -1;
					if(aEntryOccurs < bEntryOccurs) return 1;
					const aOccurs = occurs(a);
					const bOccurs = occurs(b);
					if(aOccurs > bOccurs) return -1;
					if(aOccurs < bOccurs) return 1;
					if(a.modules.length > b.modules.length) return -1;
					if(a.modules.length < b.modules.length) return 1;
					for(let i = 0; i < a.modules.length; i++) {
						if(a.modules[i].identifier() > b.modules[i].identifier()) return -1;
						if(a.modules[i].identifier() < b.modules[i].identifier()) return 1;
					}
					return 0;
				});
				// TODO refactor to Map
				chunks.forEach((c) => {
					c.__OccurenceOrderPlugin_occursInEntry = undefined;
				});
			});
		});
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.optimize.UglifyJsPlugin"></a>[function <span class="apidocSignatureSpan">webpack.optimize.</span>UglifyJsPlugin (options)](#apidoc.element.webpack.optimize.UglifyJsPlugin)
- description and source-code
```javascript
class UglifyJsPlugin {
	constructor(options) {
		if(typeof options !== "object" || Array.isArray(options)) options = {};
		if(typeof options.compressor !== "undefined") options.compress = options.compressor;
		this.options = options;
	}

	apply(compiler) {
		const options = this.options;
		options.test = options.test || /\.js($|\?)/i;
		const warningsFilter = options.warningsFilter || (() => true);

		const requestShortener = new RequestShortener(compiler.context);
		compiler.plugin("compilation", (compilation) => {
			if(options.sourceMap) {
				compilation.plugin("build-module", (module) => {
					// to get detailed location info about errors
					module.useSourceMap = true;
				});
			}
			compilation.plugin("optimize-chunk-assets", (chunks, callback) => {
				const files = [];
				chunks.forEach((chunk) => files.push.apply(files, chunk.files));
				files.push.apply(files, compilation.additionalChunkAssets);
				const filterdFiles = files.filter(ModuleFilenameHelpers.matchObject.bind(undefined, options));
				filterdFiles.forEach((file) => {
					const oldWarnFunction = uglify.AST_Node.warn_function;
					const warnings = [];
					let sourceMap;
					try {
						const asset = compilation.assets[file];
						if(asset.__UglifyJsPlugin) {
							compilation.assets[file] = asset.__UglifyJsPlugin;
							return;
						}
						let input;
						let inputSourceMap;
						if(options.sourceMap) {
							if(asset.sourceAndMap) {
								const sourceAndMap = asset.sourceAndMap();
								inputSourceMap = sourceAndMap.map;
								input = sourceAndMap.source;
							} else {
								inputSourceMap = asset.map();
								input = asset.source();
							}
							sourceMap = new SourceMapConsumer(inputSourceMap);
							uglify.AST_Node.warn_function = (warning) => { // eslint-disable-line camelcase
								const match = /\[.+:([0-9]+),([0-9]+)\]/.exec(warning);
								const line = +match[1];
								const column = +match[2];
								const original = sourceMap.originalPositionFor({
									line: line,
									column: column
								});
								if(!original || !original.source || original.source === file) return;
								if(!warningsFilter(original.source)) return;
								warnings.push(warning.replace(/\[.+:([0-9]+),([0-9]+)\]/, "") +
									"[" + requestShortener.shorten(original.source) + ":" + original.line + "," + original.column + "]");
							};
						} else {
							input = asset.source();
							uglify.AST_Node.warn_function = (warning) => { // eslint-disable-line camelcase
								warnings.push(warning);
							};
						}
						uglify.base54.reset();
						let ast = uglify.parse(input, {
							filename: file
						});
						if(options.compress !== false) {
							ast.figure_out_scope();
							const compress = uglify.Compressor(options.compress || {
								warnings: false
							}); // eslint-disable-line new-cap
							ast = compress.compress(ast);
						}
						if(options.mangle !== false) {
							ast.figure_out_scope(options.mangle || {});
							ast.compute_char_frequency(options.mangle || {});
							ast.mangle_names(options.mangle || {});
							if(options.mangle && options.mangle.props) {
								uglify.mangle_properties(ast, options.mangle.props);
							}
						}
						const output = {};
						output.comments = Object.prototype.hasOwnProperty.call(options, "comments") ? options.comments : /^\**!|@preserve|@license
/;
						output.beautify = options.beautify;
						for(let k in options.output) {
							output[k] = options.output[k];
						}
						const extractedComments = [];
						if(options.extractComments) {
							const condition = {};
							if(typeof options.extractComments === "string" || options.extractComments instanceof RegExp) {
								// extractComments specifies the extract condition and output.comments specifies the preserve condition
								condition.preserve = output.comments;
								condition.extract = options.extractComments;
							} else if(Object.prototype.hasOwnProperty.call(options.extractC ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpack.webpack_web"></a>[module webpack.webpack_web](#apidoc.module.webpack.webpack_web)

#### <a name="apidoc.element.webpack.webpack_web.webpack_web"></a>[function <span class="apidocSignatureSpan">webpack.</span>webpack_web (options, callback)](#apidoc.element.webpack.webpack_web.webpack_web)
- description and source-code
```javascript
function webpack(options, callback) {
	new WebpackOptionsDefaulter().process(options);

	const compiler = new Compiler();
	compiler.options = options;
	compiler.options = new WebpackOptionsApply().process(options, compiler);
	new WebEnvironmentPlugin(options.inputFileSystem, options.outputFileSystem).apply(compiler);
	if(callback) {
		compiler.run(callback);
	}
	return compiler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.webpack_web.Compiler"></a>[function <span class="apidocSignatureSpan">webpack.webpack_web.</span>Compiler ()](#apidoc.element.webpack.webpack_web.Compiler)
- description and source-code
```javascript
function Compiler() {
	Tapable.call(this);

	this.outputPath = "";
	this.outputFileSystem = null;
	this.inputFileSystem = null;

	this.recordsInputPath = null;
	this.recordsOutputPath = null;
	this.records = {};

	this.fileTimestamps = {};
	this.contextTimestamps = {};

	this.resolvers = {
		normal: null,
		loader: null,
		context: null
	};
	var deprecationReported = false;
	this.parser = {
		plugin: function(hook, fn) {
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.plugin(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.plugin(hook, fn);
				});
			});
		}.bind(this),
		apply: function() {
			var args = arguments;
			if(!deprecationReported) {
				console.warn("webpack: Using compiler.parser is deprecated.\n" +
					"Use compiler.plugin(\"compilation\", function(compilation, data) {\n  data.normalModuleFactory.plugin(\"parser\", function
(parser, options) { parser.apply(/* ... */); });\n}); instead. " +
					"It was called " + new Error().stack.split("\n")[2].trim() + ".");
				deprecationReported = true;
			}
			this.plugin("compilation", function(compilation, data) {
				data.normalModuleFactory.plugin("parser", function(parser) {
					parser.apply.apply(parser, args);
				});
			});
		}.bind(this)
	};

	this.options = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.webpack_web.WebEnvironmentPlugin"></a>[function <span class="apidocSignatureSpan">webpack.webpack_web.</span>WebEnvironmentPlugin (inputFileSystem, outputFileSystem)](#apidoc.element.webpack.webpack_web.WebEnvironmentPlugin)
- description and source-code
```javascript
class WebEnvironmentPlugin {
	constructor(inputFileSystem, outputFileSystem) {
		this.inputFileSystem = inputFileSystem;
		this.outputFileSystem = outputFileSystem;
	}

	apply(compiler) {
		compiler.outputFileSystem = this.outputFileSystem;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.webpack_web.WebpackOptionsApply"></a>[function <span class="apidocSignatureSpan">webpack.webpack_web.</span>WebpackOptionsApply ()](#apidoc.element.webpack.webpack_web.WebpackOptionsApply)
- description and source-code
```javascript
class WebpackOptionsApply extends OptionsApply {
	constructor() {
		super();
	}

	process(options, compiler) {
		let ExternalsPlugin;
		compiler.outputPath = options.output.path;
		compiler.recordsInputPath = options.recordsInputPath || options.recordsPath;
		compiler.recordsOutputPath = options.recordsOutputPath || options.recordsPath;
		compiler.name = options.name;
		compiler.dependencies = options.dependencies;
		if(typeof options.target === "string") {
			let JsonpTemplatePlugin;
			let NodeSourcePlugin;
			let NodeTargetPlugin;
			let NodeTemplatePlugin;

			switch(options.target) {
				case "web":
					JsonpTemplatePlugin = require("./JsonpTemplatePlugin");
					NodeSourcePlugin = require("./node/NodeSourcePlugin");
					compiler.apply(
						new JsonpTemplatePlugin(options.output),
						new FunctionModulePlugin(options.output),
						new NodeSourcePlugin(options.node),
						new LoaderTargetPlugin("web")
					);
					break;
				case "webworker":
					{
						let WebWorkerTemplatePlugin = require("./webworker/WebWorkerTemplatePlugin");
						NodeSourcePlugin = require("./node/NodeSourcePlugin");
						compiler.apply(
							new WebWorkerTemplatePlugin(options.output),
							new FunctionModulePlugin(options.output),
							new NodeSourcePlugin(options.node),
							new LoaderTargetPlugin("webworker")
						);
						break;
					}
				case "node":
				case "async-node":
					NodeTemplatePlugin = require("./node/NodeTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					compiler.apply(
						new NodeTemplatePlugin({
							asyncChunkLoading: options.target === "async-node"
						}),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new LoaderTargetPlugin("node")
					);
					break;
				case "node-webkit":
					JsonpTemplatePlugin = require("./JsonpTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					ExternalsPlugin = require("./ExternalsPlugin");
					compiler.apply(
						new JsonpTemplatePlugin(options.output),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new ExternalsPlugin("commonjs", "nw.gui"),
						new LoaderTargetPlugin("node-webkit")
					);
					break;
				case "atom":
				case "electron":
				case "electron-main":
					NodeTemplatePlugin = require("./node/NodeTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					ExternalsPlugin = require("./ExternalsPlugin");
					compiler.apply(
						new NodeTemplatePlugin({
							asyncChunkLoading: true
						}),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new ExternalsPlugin("commonjs", [
							"app",
							"auto-updater",
							"browser-window",
							"content-tracing",
							"dialog",
							"electron",
							"global-shortcut",
							"ipc",
							"ipc-main",
							"menu",
							"menu-item",
							"power-monitor",
							"power-save-blocker",
							"protocol",
							"session",
							"web-contents",
							"tray",
							"clipboard",
							"crash-reporter",
							"native-image",
							"screen",
							"shell"
						]),
						new LoaderTargetPlugin(options.target)
					);
					break;
				case "electron-renderer":
					JsonpTemplatePlugin = require("./JsonpTemplatePlugin");
					NodeTargetPlugin = require("./node/NodeTargetPlugin");
					ExternalsPlugin = require("./ExternalsPlugin");
					compiler.apply(
						new JsonpTemplatePlugin(options.output),
						new FunctionModulePlugin(options.output),
						new NodeTargetPlugin(),
						new ExternalsPlugin("commonjs", [
							"desktop-capturer",
							"electron",
							"ipc",
							"ipc-renderer",
							"remote",
							"web-frame",
							"clipboard",
							"crash-reporter",
							"native-image",
							"screen",
							"shell"
						]),
						new LoaderTargetPlugin(options.target)
					);
					break;
				default:
					throw new Error("Unsupported target '" + options.target ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpack.webpack_web.WebpackOptionsDefaulter"></a>[function <span class="apidocSignatureSpan">webpack.webpack_web.</span>WebpackOptionsDefaulter ()](#apidoc.element.webpack.webpack_web.WebpackOptionsDefaulter)
- description and source-code
```javascript
class WebpackOptionsDefaulter extends OptionsDefaulter {
	constructor() {
		super();
		this.set("devtool", false);
		this.set("cache", true);

		this.set("context", process.cwd());
		this.set("target", "web");

		this.set("module.unknownContextRequest", ".");
		this.set("module.unknownContextRegExp", false);
		this.set("module.unknownContextRecursive", true);
		this.set("module.unknownContextCritical", true);
		this.set("module.exprContextRequest", ".");
		this.set("module.exprContextRegExp", false);
		this.set("module.exprContextRecursive", true);
		this.set("module.exprContextCritical", true);
		this.set("module.wrappedContextRegExp", /.*/);
		this.set("module.wrappedContextRecursive", true);
		this.set("module.wrappedContextCritical", false);
		this.set("module.strictExportPresence", false);

		this.set("module.unsafeCache", true);

		this.set("output", "call", (value, options) => {
			if(typeof value === "string") {
				return {
					filename: value
				};
			} else if(typeof value !== "object") {
				return {};
			} else {
				return value;
			}
		});
		this.set("output.filename", "[name].js");
		this.set("output.chunkFilename", "make", (options) => {
			const filename = options.output.filename;
			return filename.indexOf("[name]") >= 0 ? filename.replace("[name]", "[id]") : "[id]." + filename;
		});
		this.set("output.library", "");
		this.set("output.hotUpdateFunction", "make", (options) => {
			return Template.toIdentifier("webpackHotUpdate" + options.output.library);
		});
		this.set("output.jsonpFunction", "make", (options) => {
			return Template.toIdentifier("webpackJsonp" + options.output.library);
		});
		this.set("output.libraryTarget", "var");
		this.set("output.path", process.cwd());
		this.set("output.sourceMapFilename", "[file].map[query]");
		this.set("output.hotUpdateChunkFilename", "[id].[hash].hot-update.js");
		this.set("output.hotUpdateMainFilename", "[hash].hot-update.json");
		this.set("output.crossOriginLoading", false);
		this.set("output.hashFunction", "md5");
		this.set("output.hashDigest", "hex");
		this.set("output.hashDigestLength", 20);
		this.set("output.devtoolLineToLine", false);
		this.set("output.strictModuleExceptionHandling", false);

		this.set("node", {});
		this.set("node.console", false);
		this.set("node.process", true);
		this.set("node.global", true);
		this.set("node.Buffer", true);
		this.set("node.setImmediate", true);
		this.set("node.__filename", "mock");
		this.set("node.__dirname", "mock");

		this.set("performance.maxAssetSize", 250000);
		this.set("performance.maxEntrypointSize", 250000);
		this.set("performance.hints", false);

		this.set("resolve", {});
		this.set("resolve.unsafeCache", true);
		this.set("resolve.modules", ["node_modules"]);
		this.set("resolve.extensions", [".js", ".json"]);
		this.set("resolve.aliasFields", "make", (options) => {
			if(options.target === "web" || options.target === "webworker")
				return ["browser"];
			else
				return [];
		});
		this.set("resolve.mainFields", "make", (options) => {
			if(options.target === "web" || options.target === "webworker")
				return ["browser", "module", "main"];
			else
				return ["module", "main"];
		});
		this.set("resolveLoader", {});
		this.set("resolveLoader.unsafeCache", true);
		this.set("resolveLoader.mainFields", ["loader", "main"]);
		this.set("resolveLoader.extensions", [".js", ".json"]);
	}
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
