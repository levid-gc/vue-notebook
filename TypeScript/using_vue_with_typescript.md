# 使用 TypeScript 编写 Vue 应用

## 装饰器

Vue 中的所有装饰器类型都来自 `vue-property-decorator` 包。

示例：

```typescript
import { Vue, Component } from 'vue-property-decorator';
```

- `Vue`：Vue 组件基类，它间接从 `vue` 包导出。
- `Component`：用于标注一个类为 Vue 组件，它间接从 `vue-class-component` 包导出。

## Vue 组件对象

### `data`

JS 常见写法：

```javascript
import Vue from 'vue';

new Vue({
  // ...
  data: {
    counter: 0
  }
  // ...
})
```

TS 推荐写法：

```typescript
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {
  // ...
  public counter: number = 0;
  // ...
}
```

**提示**：将 `data` 对象中的各属性直接作为 Vue 组件类的公共字段。

### `computed`

JS 常见写法：

```javascript
import Vue from 'vue';

new Vue({
  // ...
  computed: {
    message() {
      return this.counter == 0 ? 'Button Not Pressed' : `Button Presses: ${this.counter}`;
    }
  }
  // ...
})
```

TS 推荐写法：

```typescript
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {
  // ...
  public get message(): string {
    return this.counter === 0 ? 'Button Not Pressed' : `Button Presses: ${this.counter}`;
  }
  // ...
}
```

**提示**：将 `computed` 对象中各方法直接作为 Vue 组件类的公共属性 `get` 方法。

### `methods`

JS 常见写法：

```javascript
import Vue from 'vue';

new Vue({
  // ...
  methods: {
    handleClick() {
      this.counter++;
    }
  }
  // ...
})
```

TS 推荐写法：

```typescript
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {
  // ...
  public handleClick(): void {
    this.counter++;
  }
  // ...
}
```

**提示**：将 `methods` 对象中各方法直接作为 Vue 组件类的公共方法。
