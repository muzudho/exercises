# 練習課題


## 課題： Hello

👇 次のようなプログラムを作ってください。  

以下の２０文字を打鍵してエンター・キーを押下すると……。（ここで、 `go-practice` の部分は、適宜、あなたのプログラム・ファイル名に置き換えてください。以降同じ）  

```shell
go-practice -p hello
```

👇 ２行目に、以下の５文字が出てください。  

```plaintext
world
```

👇 以降、以上の手続きを、以下のように表記することにします。

```shell
go-practice -p hello
        ## ## 応答
        ## world
```


## 課題： Interpreter

👇 次のようなプログラムを作ってください。  

以下の１１文字を打鍵してエンター・キーを押下すると……。（ここで、 `go-practice` の部分は、適宜、あなたのプログラム・ファイル名に置き換えてください。以降同じ）  

```shell
go-practice
```

👇 ２行目に、以下の４文字が出てください。（４文字目は半角空白です）  

```plaintext
>>> 
```

３行目に、以下の５文字を打鍵してエンター・キーを押下すると……。  

```shell
hello
```

👇 ４行目に、以下の５文字が出てください。  

```plaintext
world
```

👇 以降、以上の手続きを、以下のように表記することにします。

```shell
>>> hello
        ## ## 応答
        ## world
```

`[Ctrl] + [C]` を打鍵するなどして、プログラムを強制終了させてください。  


## 課題： Quit

さきほどの課題［Interpret］の続きです。  

以下のように、応答が返ってきたら、また入力に戻るようにしてください。  

```shell
go-practice
>>> hello
world
>>> hello
world
>>> hello
world
```

👆 繰り返しから抜けたいときは、[Ctrl] + [C] キーでプログラムを強制終了できるでしょう。  

次に、 `quit` と入力したら、繰り返しから抜けるようにしてください。  

```shell
go-practice
>>> hello
world
>>> quit
```


## 課題： Undefined Command

👇 次のようなプログラムを作ってください：  

👇 以下のコマンドを打鍵してください：  

```shell
go-practice
        ## ## 応答
        ## >>> 
```

👇 以下のように打鍵してください。  

```shell
>>> banana
        ## ## 応答
        ## Undefined `Banana` command.
```


## 課題： Engine Options

次のようなプログラムを作ってください：  

👇 以下のようにコマンドラインを入力すると：  

```shell
go-practice
        ## ## 応答
        ## >>> 
```

👇 以下のように打鍵：  

```shell
>>> get-option -n engine
        ## ## 応答
        ## Option not found.
        ## >>> 
```

👇 以下のように打鍵：  

```shell
>>> set-option -n engine -v banana
        ## ## 応答
        ## [banana] 
```

👇 以下のように打鍵：  

```shell
[banana] get-option -n engine
        ## ## 応答
        ## banana
        ## [banana] 
```

👇 以下のように打鍵：  

```shell
[banana] quit
```


## 課題： Echo Proxy

次のようなプログラムを作ってください：  

👇 以下のようにコマンドラインを入力すると：  

```shell
go-practice
        ## >>> 
```

このコマンドの実体は例えば 📄 `Z:/muzudho-github.com/muzudho/go-practice/go-practice.exe` といった実行ファイルだとします。  

👇 以下のように打鍵：  

```shell
>>> set-option -n engine -v banana
        ## [banana] 
```

👇 以下のように打鍵：  

```shell
[banana] echo-proxy -f Z:/muzudho-github.com/muzudho/go-practice/go-practice.exe
        ## >>> 
```

つまり、実行ファイル自身へのファイルパスを `-f` 引数に渡しています。  

👇 以下のように打鍵：  

```shell
>>> hello
        ## world
        ## >>> 
```

👇 以下のように打鍵：  

```shell
>>> quit
        ## 外部プロセスが終了しました。呼び出し元プロセスの標準入力がクリーンになるまで、改行を送ってきてください。
        ## [banana]
```

ここで、元のプロセスの標準入力に戻ったとき、（ＯＳ依存で）何回か入力が無効になっているケースがあります。  
仕方ないので、空行（エンター・キーを押すだけ）を２回ほど試してください。  

👇 以下のように再び打鍵：  

```shell
[banana] quit
```
