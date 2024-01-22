# entity_properties
predicateのentity_propertyに関するデータパックサンプルになります。

詳しくはブログ記事『[【マイクラ】entity_propertyでエンティティの状態を指示【predicate】](https://natsumake.com/entity_property/)』を参考にしてください。

<h3>使い方</h3>

導入後、自動的にredというチームに所属されます。<br>
もしされていない場合は、```/reload```を実行してください。

基本的には<br>
```/execute if predicate sample:effect run give @a diamond 1```<br>
といった形のコマンドを実行すればOKです。

※"sample:effect"の"effect"部分は各種jsonファイル名に変更してください。

***

一部、コマンドの実行者やコマンドの実行位置を指示しなければ分かりにくいものがあります。<br>
type_specific.jsonを指示する場合は``` /execute as @e[type=cat] if predicate sample:type_specific run give @a diamond 1```<br>
targeted_entity.jsonを指示する場合は```/execute as @e[type=zombie] if predicate sample:targeted_entity run give @a minecraft:diamond 1```<br>
distance.jsonを指示する場合は```/execute positioned 10 10 10 if predicate sample:distance run give @a diamond 1```<br>
といった風にasやpositionedを指示してください。

また、passenger.jsonはrideコマンドを駆使して、アイアンゴーレムを何かしらのmobに騎乗させてください。

***

以下、実装したjsonファイルの指示内容を簡潔に書いたものです。

|jsonファイル|記述内容|
-|-
| distance.json | コマンドの実行位置から空間的に見て0～10マス以内にいるかどうか |
| effect.json | 発光のエフェクトを受けているかどうか |
| entity_type.json | プレイヤーであるかどうか |
| equipment.json | メインハンドにダイヤモンドを持っているかどうか |
| flags.json | スニークをしているかどうか |
| location.json | 平野バイオームにいるかどうか |
| nbt.json | Airの値が300sかどうか |
| passenger.json | アイアンゴーレムが何かに騎乗しているかどうか |
| stepping_on.json | 草ブロックの上にいるかどうか |
| targeted_entity.json | プレイヤーを攻撃対象にしているかどうか |
| team.json | redというチームに所属しているかどうか |
| type_specific.json | （ネコの種類が）ブリティッシュショートヘアーかどうか |
| vehicle.json | ブタが騎乗されている状態にあるかどうか |

