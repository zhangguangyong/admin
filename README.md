### antd 配置主题

```
yarn add antd

yarn add @craco/craco
/* package.json */
"scripts": {
-   "start": "react-scripts start",
-   "build": "react-scripts build",
-   "test": "react-scripts test",
+   "start": "craco start",
+   "build": "craco build",
+   "test": "craco test",
}


yarn add craco-less
/* craco.config.js */
const CracoLessPlugin = require('craco-less');
module.exports = {
  plugins: [
    {
      plugin: CracoLessPlugin,
      options: {
        lessLoaderOptions: {
          lessOptions: {
            modifyVars: { '@primary-color': '#1DA57A' },
            javascriptEnabled: true,
          },
        },
      },
    },
  ],
};

/* src/App.less */
- @import '~antd/dist/antd.css';
+ @import '~antd/dist/antd.less';

/* src/App.js */
- import './App.css';
+ import './App.less';

```
