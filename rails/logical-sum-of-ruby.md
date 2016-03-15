# Rubyの論理和

- Rubyの `||` 演算子は、「左辺を評価し、結果が真であった場合にはその値を返します。 左辺の評価結果が偽であった場合には右辺を評価しその評価結果を返します。」
- なので、結果はBoolean(true, false)ではなく、「右辺もしくは左辺の評価結果」になる。
- 「右辺か左辺の少なくとも1つが真の場合に真」みたいな解説をちらほら見かけるが、正確ではない。

---

これを上手く利用すると、下のように処理をスッキリ書くことができる場合がある。

```ruby
# before
user_id = params[:id].present? ? params[:id] : params[:user_id]
```

```ruby
# after
user_id = params[:id] || params[:user_id]
```
