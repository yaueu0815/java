## JSP の基本

### サンプルコード

hello.jsp

```jsp
<%@page contentType="text/html; charset=UTF-8" %>
<%! String msg = "Hello, World!!"; %>

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>JSPサンプルコード</title>
</head>
<body>
    <%
    for (int i = 0; i < 5; i++) {
        out.println(msg + "<br>");
    }
    %>
</body>
</html>
```

### JSP の構造

JSP は HTML をベースに、様々な出力ルールを埋め込むことが出来る **HTML 埋め込み型** の言語です。

> **JSP ページで使える主な要素**  
> | 名前 | 構文 | 概要 |
> | ---- | ---- | ---- |
> | ディレクティブ | <%@ ... %> | ページ単位の処理方法を指定 |
> | 宣言部 | <%! ... %> | 変数や定数、ユーザー定義メソッドを宣言 |
> | スクリプトレット | <% ... %> | ページの処理方法を記述 |
> | 式(Expression) | <%= ... %> | 指定された式を出力 |
> | アクションタグ | <jsp: ...> | 定型的な処理をタグの形式で記述 |
> | コメント | <%-- ... --%> | 処理に際しては無視される備考を記述 |
