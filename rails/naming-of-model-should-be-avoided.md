# Railsで避けるべきモデル・カラムのネーミング

ついうっかりつけてしまって積んだカラム名。

|名前|理由|代替え案|
|---|---|---|
|type|STIの予約語|context|
|transaction|ActiveRecordのクラスメソッド|bill|
|method|FactoryGirlで死ぬ||
