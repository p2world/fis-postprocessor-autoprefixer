# fis-postprocessor-autoprefixer

a postprocessor for fis to autoprefixer css with [postcss/autoprefixer](https://github.com/postcss/autoprefixer)

1. install fis-postprocessor-autoprefixer
```bash
npm install -g https://github.com/p2world/fis-postprocessor-autoprefixer/archive/master.tar.gz
```
2. modify fis-conf.js
```javascript
fis.config.set('modules.postprocessor.css', 'autoprefixer');
```
3. set the browsers option of `postcss/autoprefixer`
```javascript
fis.config.merge({
    settings : {
        postprocessor : {
          autoprefixer : {
              // detail config (https://github.com/postcss/autoprefixer#browsers)
              "browsers": ['FireFox > 1','Chrome > 1',"ie >= 8"]
            }
        }
    }
});
```
4. fis release
`fis release`
