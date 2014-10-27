# gulp-vm

> For whenever you need to run a script as part of your build process

Lets say you want to run a script, call a function which produces some output
and then save that output to a file:

    var streamify = require('streamify')
    var vm = require('gulp-vm')

    return gulp.src('./myScript.js')
      .pipe(streamify(vm(function (x) {
        return x.myMethodThatProducesOutput()
      })))
      .pipe(gulp.dest('./build/'))

`gulp-vm` takes a callback, but it's optional and if none is provided it just
runs the script and returns the original file input as output.

## License

MIT
