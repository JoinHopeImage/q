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
