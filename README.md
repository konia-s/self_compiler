# 自作コンパイラ
構文解析系、字句解析系、クロスリファレンス系のモジュールを作成した。

これらのモジュールは構文解析系が字句解析系を呼び出し字句解析を行い字句解析の結果を用いて構文解析をし、変数、関数宣言が行われていれば適宜クロスリファレンス系を呼び出し記号表への追加を行う。また、宣言が行われ記号表に追加されている変数及び関数が使用された場合についてもクロスリファレンス系を呼び出し使用された行数を記号表の呼びだされた変数及び関数について記録する。


今回は型の一致を字句解析系により行なっているため型の不一致が認められた場合は字句解析系がエラーを検出し適切なエラーメッセージを表示した後にプログラムを終了する
