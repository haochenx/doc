HP16Cのマニュアルからの抜粋

@suharahiromichi

2012/09/14


# 整数モード

1. 基数の切り替え、HEX、DEC、OCT、BIN

   DECのときだけ、「-」を表示する。
   表示だけであり、演算には影響しない。
   一時的に切り替えるなら、SHOW HEXなど。

2. 補数表現、1'S、2'S、UNSGN

   四則演算およびCHSに影響する。

3. ＋、-、×、÷、CHS、√、RMD（剰余）、ABS
   * 「C」「G」フラグがセットされる。
   * 「C」はキャリーまたはボロー、シフト、ローテート
   * UNSGNで負数になったときは、2の補数となり、「G」がセットされる。
   * 割り算と√で余りが≠0のとき、「C」がセットされる。
      割り算と√の結果は、絶対値の切り捨てである。
   * ABSでも「G」はセットされることがある。
      2'S、16、WSIZE、HEX、8000、ABS、の操作では、値は、8000のままとなる。
   * 「G」のとき、下位ビットだけになるが、1'Sまたは2'Sなら、符号ビットは保存される。

4. ワード長、WSIZE

   0〜64をXにおいてWSIZEを押す。
（通常はまずDEC、0、WSIZEを押してからでは
   ないと、所望のサイズが設定できない。）
   サイズの切り替えにおいては、零拡張のようだ。

4. 表示だけなら

   WINDOW n (前操作キー）、および、「<」 と 「>」

5. フラグ   SF、CF、F?、（前操作キー）
   * 1 ユーザ利用
   * 2 ユーザ利用
   * 3 ユーザ利用
   * 4 セットならBIN、OCT、HEXでゼロサプレスしない。
   * 5 キャリー「C」
   * 6 out-of-range「G」

6. 論理演算 AND、OR、XOR

7. シフト SL、SR（論理シフト）、ASL
 * LJ、右揃えした結果がY、シフト量をXにいれる。
 * RLn、RRn、ローテート量がX、対象がY。

8. ローテート
 * RL、RR、「C」を含まないが、「C」は変化する。
 * RLC、RRC、「C」を含む。RLCn、RRCn、ローテート量がX、対象がY。

9. マスク MASKL、MASKR

   マスク用のデータを作る（まだANDはとらない）

10. ビットの合計 #B

11. 2倍長演算 DBLX、DBL÷、DBLR
    * Y * X → X..Y
    * Y..Z / X → X

    X, Y, Z は、同じワード長のデータが入る。

# 実数モード

1. 実数と整数の切り替え
  * FLOAT n （前操作キー）
  * FLOAT . で指数部付きの表示となる。

　切り替えにともなうXとYの値の変化

  * 実数になるとき、Y * 2^X → X
  * 整数になるとき、X → Y * 2^X

    この計算は、そのときの補数表現でおこなわれる。


2. 実数モードで使用できる演算

    ＋、-、×、÷、CHS、√、ABS

    1/X は実数モードだけである。RMD（剰余）は使用できない。


3. CHS

   整数モードでは演算だが、実数モードでは「.」やEEXとおなじ、数値入力の一部である。
    

# 補足

* 日英ともマニュアルの表記は HP-16C と「ハイフン」が入っている。
HP-10シリーズはすべてそうだが、復刻版はそうなっていない。

* 小数部桁数の数字はスタックに積まれないものを、前操作キーという。
* 付録に、IEEE754の単精度をHP-16Cの実数に、その逆のプログラム例が掲載されている。

以上

