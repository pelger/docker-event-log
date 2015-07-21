# docker-events

Collect docker container events

## Install

```sh
npm install docker-events --save
```

## Usage

```
var de = require('docker-events');
var through = require('through2');

de({}).pipe(through.obj(function(chunk, enc, cb) {
  this.push(JSON.stringify(chunk));
  this.push('\n');
  cb();
})).pipe(process.stdout);
```

## Acknowledgements

Sponsored by [nearForm](http://nearform.com).

## License

MIT
