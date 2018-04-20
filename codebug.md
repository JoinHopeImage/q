# 淘宝npm镜像

临时使用

npm --registry https://registry.npm.taobao.org install express

持久

    npm config set registry https://registry.npm.taobao.org

    验证是否配置成功    npm config get registry

通过cnpm使用

    npm install -g cnpm --registry=https://registry.npm.taobao.org

    使用  cnpm install express

# flex存在兼容性，flex 有三个版本，分别是：
`
    display: box;
    display: flexbox;
    display: flex;
`
如果用了autoprefixer，则只需要写一个，display: flex

但是需要在package.json里面加上
`
"browserslist": [
   "iOS >= 8",
   "Android > 4"
]
`

# gulp-uglify压缩JS居然不支持ES6
但是可以先转为ES5再压缩，问题又来了，转ES5之后出现了require未定义，待解决。
pump([gulp.src('./src/sw.js'), babel({ presets: [es2015] }), uglify(), gulp.dest('./we/cx')])

# Uncaught (in promise) Error: Network Error
是因为Promise.reject返回了一个拒绝状态的promise对象，如果其后的then/catch都没有申明onRejected毁掉，就会抛出这样的错误。并且，外部的promise无法捕获这个错误，同时，由于promise是异步的，try/catch也无法捕获。所以，promise记得写上catch。
