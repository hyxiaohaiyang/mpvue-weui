# Searchbar

搜索栏。

<imgPreview imgUrl="/assets/searchbar.png"/>

### 引入

``` js
import mpSearchbar from 'mpvue-weui/src/searchbar';
export default {
  components: {
    mpSearchbar,
  },
}
```

### 使用

``` html
<mp-searchbar :isFocus=true :inputValue="inputValue" :placeholder="placeholder" @input="input" @blur="blur" @focus="focus" @confirm="confirm"></mp-searchbar>
```

### API

| 参数 | 说明 | 类型 | 默认值 |
|-----------|-----------|-----------|-------------|
| value | 绑定的值，可使用 `v-model` 双向绑定 | `String, Number` | - |
| isFocus | 获取焦点 | `Boolean` | `false` |
| placeholder | 输入框为空时占位符 | `String` | -|
| confirmType | 设置键盘右下角按钮的文字,可选值 `send` `search` `next` `go` `done` | `String` | `right` |

::: tip  confirmType 值对应的文字说明
* send：右下角按钮为“发送”
* search：右下角按钮为“搜索”
* next：右下角按钮为“下一个”
* go：右下角按钮为“前往”
* done：右下角按钮为“完成”
:::

### Event
| 事件名 | 说明 | 参数 |
|-----------|-----------|-----------|
| @on-input | 键盘输入时触发 | `event` |
| @focus | 输入框聚焦时触发 | `event` |
| @blur | 输入框失去焦点时触发 | `event` |
| @confirm | 点击完成按钮时触发 | `event` |

::: warning
1.0.3 版本之前`searchbar` 输入框的值不支持数据双向绑定，输入时触发的事件为：`input`，详情见 [issues 19](https://github.com/MPComponent/mpvue-weui/issues/19)。
:::