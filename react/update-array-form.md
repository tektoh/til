# 配列になったフォームの更新

```jsx
hundleClick: function(event, item) {
  item.value = event.target.value
  this.setState({items: this.state.items})
}

render: function() {
  return (
    <form>
      {this.state.items.map(function (item) {
        var _hundleClick = (function (event) {
          this.hundleClick(event, item)
        }).bind(this)
        
        return (
          <div key={item.key}>
            <input type="text" value={item.value} onClick={_hundleClick} />
          </div>
        )
      }, this)}
    </form>
  )
}
```

## 注意点など

- map の第2引数に `this` を入れておかないと `this` が行方不明になる。
