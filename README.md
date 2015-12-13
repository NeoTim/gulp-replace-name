# gulp-replace-name
To change file name.

## Install

```bash
$ npm install gulp-replace-name --save-dev
```

## Usage

```javascript
var gulp = require('gulp');
var replaceName = require('gulp-replace-name');

var gulp = require('gulp');
var replaceName = require('./index');

// .js -> .min.js
gulp.task('replaceName', function() {
  return gulp.src('./**/*.js')
    .pipe(replaceName(/\.js/g, '.min.js'))
    .pipe(gulp.dest('./dist'));
});


// .js -> .json
gulp.task('replaceName', function() {
  return gulp.src('./**/*.js')
    .pipe(replaceName(/\.js/g, '.json'))
    .pipe(gulp.dest('./dist'));
});


// hello -> world
gulp.task('replaceName', function() {
  return gulp.src('./**/*.js')
    .pipe(replaceName(/hello/g, 'world'))
    .pipe(gulp.dest('./dist'));
});
```
