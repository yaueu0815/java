## ArrayList

### ArrayList とは

List インターフェースを実装したクラスの一つ。

- 要素の数が可変
- 各要素へ比較的高速にアクセス可能。逆に、要素の追加や削除に時間がかかる

#### インポート

ArrayList クラスは、java.util パッケージに含まれています。利用する場合、java.util.ArrayList をインポートする必要があります。

```java
import java.util.ArrayList;
```

#### インスタンスの生成

new 演算子を使う

```java
ArrayList<データ型> 変数名 = new ArrayList<>();

例 : ArrayList<String> strArray = new ArrayList<>();
```

#### 親クラスのインスタンスとして生成

ArrayList は、List インターフェースを実装したクラスなので、List オブジェクトとして生成することができます。List オブジェクトとして生成した場合、List インターフェースでのみ定義されているメソッドしか使用できません。同じ List インターフェースを実装したクラスへ変換する場合に便利です。

```java
List<データ型> 変数名 = new ArrayList<>();

例 : List<Integer> intList = new ArrayList<>();
```

#### ラッパークラスの使用

データ型には、基本データ型の int や double を指定することができません。これらの数値を格納したい場合には、それぞれの基本データ型に対応したラッパークラスを利用します。

| 基本データ型 | ラッパークラス |
| ------------ | -------------- |
| boolean      | Boolean        |
| char         | Character      |
| byte         | Byte           |
| short        | Short          |
| int          | Integer        |
| long         | Long           |
| float        | Float          |
| double       | Double         |

#### 要素の追加

```java
public boolean add(E e)
```

リストの最後に要素を追加するメソッドです。もしリストの領域が足りなくなった場合、自動的に領域が追加され格納されます。

```java
List<String> fruits = new ArrayList<>();

fruits.add("Apple");
fruits.add("Orange");
fruits.add("Lemon");
```

> **Note**  
> for 分で追加することもできます。
>
> ```java
> for (String fruit : new String[]{"Apple", "Orange", "Lemon"}) {
>     fruits.add(fruit);
> }
> ```
