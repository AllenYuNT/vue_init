### Vue配置：

#### 目录结构：

> global

- filters.js

  > 公共方法

- router.js

  > 公共路由，views下配置的路由import引入

  ```vue
  import login from '../views/login/router'

  export default new Router({
    routes: [
      {
        path: '/',
        redirect:'/login',
        // component: App
      },
      ...login
    ],
  })
  ```



> lib

- ajax.js

  > 封装axios

- iview.js

  > 组件库：https://www.iviewui.com/

- svgIcon.js

  > svg矢量图标

  ```
  <sicon name="demo" scale="2.0"></sicon>
  ```



> svg

- svg图标目录，图标名与 `sicon` 的 `name` 对应



> views

- api.js

  > 封装 `ajax`

  - ```javascript
    this.$api.getData(url);
    ```

  - ```javascript
    this.$api.sendData(url, data);
    ```

- file (不同文件夹)

  > 不同页面放在不同文件夹，每个文件夹有自己单独的 `router`, `components` 等等
  >
  > 方便多人开发

