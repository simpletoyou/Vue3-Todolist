# Vue3-Todolist
Vue3+Vite 
## vue3.0
    * 变化
        - 组合式API + 函数式编程
        - 组件间逻辑共享
    * 性能提升 1.3~2x
        - 核心代码+Composition API
            - 静态node不再作更新处理（hoistStatic -> SSR优化）
            - 静态绑定的class，id不再作更新处理
            - 结合打包标记PathFlag，进行更新分析（动态绑定）
            - 事件监听器Cache缓存处理（cache Handles）
            - hoistStatic自动针对多静态节点进行优化，输出字符串
            - Complier原理
                https://vue-next-template-explorer.netlify.app/
            - 优点：复杂组件逻辑进行分离；组件间逻辑共享
    * TS支持（新增Fragment、Teleport、Suspense）
        - Fragment：不受根节点限制，渲染函数可接收Array
        - Teleport：类似Portal，随用随取，如弹窗、Actions
        - Suspense：嵌套的异步依赖，如async setup()
    * 按需加载（配合vite）& 组合API
## Vue2缺点
    * Vue2对于复杂逻辑组件，在后期变得无法维护
    * Vue2中代码复用方法，如Mixin，Filters都有缺陷
        - Mixin（命名空间冲突，逻辑不清晰，不易复用）
        - scoped slot作用域插槽（配置项多，代码分裂，性能差）
    * Vue2对TS支持不充分