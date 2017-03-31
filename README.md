# CINDERELLA-PROJECT


【バーテックスシェーダーの座標計算によって異なる解像度を吸収して高速に2D描画する】

通常必要最低限の解像度のビットマップやテクスチャのターゲットを決めて
ターゲットにゲームの背景やキャラクターを描画し
その後にターゲットをフルスクリーンで画面に描画する事で全ての機種に画面対応している。

ただしこの方法だと若干処理速度に無駄が生じるので効率の良い方法を考えた。

今回はOpenGL-ES2.0のシェーダープログラムを使用する事にする。
画面解像度は機種毎によって違っているが、
例えば「1280×720ピクセル以上のLANDSCAPE画面解像度に対応」と決めて
「1280×720ピクセルのレンダリングターゲットがある」と仮定して
レンダリングターゲットと画面解像度の比率を求めて頂点座標に乗算して
左上座標系にシェーダーで書き込む事によって全ての機種の液晶解像度に対応できる。

しかも流行りのフレームバッファを使った方法と違って
一画面ぶんのメモリーへのピクセルのバッファリングという時間の無駄が無いので
高速な2Dキャラのレンダリング(描画)が実現可能です。

　
by 神官メリイ
 
