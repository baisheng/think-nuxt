# think-nuxt

> Nuxtjs for thinkjs middleware

#### 安装

```bash
npm install think-nuxt --save
```

#### 使用

在 middleware 中引入, 中间件文件在 `src/config/middleware.js`

```javascript
const nuxt = require('think-nuxt');
```

配置 `handle` 参数

```javascript
{
    handle: nuxt,
    options: {}
}
```

配置 `options` 

```javascript
  {
    handle: 'nuxt',
    options: {
      config: nuxtConfig, 	// nuxt.config.js 配置文件，默认识别为 think.ROOT_PATH/nuxt.config.js
      unless: [/^\/api?/],	// 非 nuxtjs 拦截的目录，如果 api controller 等
      isDev: isDev		// dev 模式下 nuxtjs 将主动编译
    }
  },
```

### 示例项目
[https://github.com/baisheng/nuxt-thinkjs3](https://github.com/baisheng/nuxt-thinkjs3)
