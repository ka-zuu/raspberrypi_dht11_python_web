# raspberrypi_dht11_python_web
ラズパイに接続したdht11から温湿度を取得して、index.htmlを作成(main.py)
Pythonの簡易httpサーバで公開する(server.py)


## 下準備
### DHT11のPythonライブラリを取得
`git clone https://github.com/szazo/DHT11_Python.git`
* 参考URL：https://qiita.com/mininobu/items/1ba0223af84be153b850

### ライブラリをimportするために、リンクを貼る
`ln -s DHT11_Python/dht11`


## サーバ起動
`nohup python3 server.py &`


## OMAKE
### Macのxbarでメニューバーに値を表示する
`raspi-ondo.5m.sh`に実行権限を付与して、xbarに登録する
↑で起動したサーバに、5分に1回温度を問い合わせして、メニューバーに表示する
