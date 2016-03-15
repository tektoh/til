# Railsで避けるべきモデル・カラムのネーミング

ついうっかりつけてしまって積んだカラム名。

|名前|理由|代替え案|
|---|---|---|
|type|モデルでSTIするためのカラム名|context|
|transaction|ActiveRecordのクラスメソッド|bill|
|method|FactoryGirlで死ぬ||
