# 淘宝npm镜像

临时使用

npm --registry https://registry.npm.taobao.org install express

持久

    npm config set registry https://registry.npm.taobao.org

    验证是否配置成功    npm config get registry

通过cnpm使用

    npm install -g cnpm --registry=https://registry.npm.taobao.org

    使用  cnpm install express
