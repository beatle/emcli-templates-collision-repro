#O Templates collision reproduction

## Steps to reproduce
```
npm i
bower i
npm run build
```
And you should see something like:
```
version: 1.13.13
Could not find watchman, falling back to NodeWatcher for file system events.
Visit http://www.ember-cli.com/user-guide/#watchman for more info.
Livereload server on http://localhost:49152
Serving on http://localhost:4200/
EEXIST, file already exists '/home/beatle/workspace/ember-cli-apps/c/tmp/template_compiler-output_path-beowNp4d.tmp/dummy/templates/test.js'
Error: EEXIST, file already exists '/home/beatle/workspace/ember-cli-apps/c/tmp/template_compiler-output_path-beowNp4d.tmp/dummy/templates/test.js'
    at Error (native)
      at Object.fs.symlinkSync (fs.js:848:18)
      at symlink (/home/beatle/workspace/ember-cli-apps/c/node_modules/symlink-or-copy/index.js:82:14)
      at symlinkOrCopySync (/home/beatle/workspace/ember-cli-apps/c/node_modules/symlink-or-copy/index.js:58:5)
      at TemplateCompiler.Filter._handleFile (/home/beatle/workspace/ember-cli-apps/c/node_modules/broccoli-persistent-filter/index.js:101:12)
      at TemplateCompiler.<anonymous> (/home/beatle/workspace/ember-cli-apps/c/node_modules/broccoli-persistent-filter/index.js:88:21)
      at /home/beatle/workspace/ember-cli-apps/c/node_modules/promise-map-series/index.js:11:14
          at lib$rsvp$$internal$$tryCatch (/home/beatle/workspace/ember-cli-apps/c/node_modules/rsvp/dist/rsvp.js:493:16)
      at lib$rsvp$$internal$$invokeCallback (/home/beatle/workspace/ember-cli-apps/c/node_modules/rsvp/dist/rsvp.js:505:17)
      at lib$rsvp$$internal$$publish (/home/beatle/workspace/ember-cli-apps/c/node_modules/rsvp/dist/rsvp.js:476:11)
```
