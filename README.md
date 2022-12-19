# go-example-package

## パッケージ作成手順

- 1. `math/math.go`を作成する
    - ファイルの最初の行はパッケージ節で`package <パッケージ名>`を書きます。
    - パッケージ名とそのパッケージを含むディレクトリ名は同じにします。
    - `math`ディレクトリの中に`package math`を作ります。
- 2. `main.go`を作成する
    - mainパッケージは`package main`で始めます。
    - `package math`をインポートします。
        - インポートパスは`<モジュールまでのパス(example.co.jp/go-example-package)>/<モジュール内のパッケージまでのパス(math)>`とします。
        - この時点ではモジュールが作成されていないため、正しく`package math`を参照できていません。
- 3. モジュールを作成する
    - ` go mod init example.co.jp/go-example-package`でモジュールを作成します。モジュール名は https://go.dev/doc/modules/managing-dependencies#naming_module を参考にします。
    - モジュールを作成したことで正しく`package math`を参照できるようになります。
- 4. `go run main.go`する
    - 4が出力されればOKです。
- 5. `go build`
    - `go-example-package`が生成されます。
    - `./go-example-package`とすると実行できます。出来上がった`go-example-package`はどこに移動しても実行できます。
