###データベースの基礎
--------------------
####1.データベース操作の基礎
######表(テーブル)の作成

```sql
	CREATE TABLE 表名 (コラム1 データ型, コラム2 データ型 ...);
```

######SELECT文
(1)すべての表の内容を表示する(単純質問)
```SQL
	SELECT * FROM テーブル名;
```

(2)特定のコラムを指定して表示する(射影演算)
```SQL
	SELECT コラム名 FROM テーブル名;
```
重複を排除する場合
```SQL
	SELECT DISTINCT コラム名 FROM テーブル名;
```

(3)条件指定でレコードを表示する(選択演算)
```SQL
	SELECT コラム名 FROM テーブル名 WHERE 条件;
```

(4)条件のAND演算
```SQL
	SELECT コラム名 FROM テーブル名 WHERE 条件 AND 条件;
```

(5)SELECT文内での演算(拡張射影)
```SQL
	SELECT コラム名(演算を含む) FROM テーブル名
```

(6)範囲指定でレコードを表示する
```SQL
	SELECT * FROM テーブル名 WHERE コラム名 BETWEEN 条件 AND 条件;
```

(7)グループ化
```SQL
	SELECT コラム FROM テーブル名
	GROUP BY コラム
```

```SQL
	SELECT コラム名 
	FROM テーブル名
	HAVING COUNT(*) >= 3
	##HAVING節は条件を指定する。今回はCOUNT(*)が3以上の場合のみを表示。
```

(9)結合質問と入れ子型質問
```SQL
	SELECT X.コラム名, X.社員名
	FROM テーブル名 X, テーブル名 Y
	WHERE ~ 
```

######INSERT文
```SQL
	INSERT INTO テーブル名 VALUES(データ値);
```

######UPDATE文
```SQL
	UPDATE テーブル名 SET コラム名 = 入れるべきデータ WHERE 挿入するレコードを指定する条件
```

######DELETE文
```SQL
	DELETE FROM テーブル名 WHERE 削除するべきレコードを指定する条件
```

######テーブルの作成
