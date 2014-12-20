"A Gentle Introduction to Type Classes and Relations in Coq" の読み方
======

2014/12/20 @suharahiromichi


# 文書の在処

http://www.labri.fr/perso/casteran/CoqArt/TypeClassesTut/typeclassestut.pdf


# サンプルコードのインストール

http://www.labri.fr/perso/casteran/CoqArt/TypeClassesTut/src-V8.4.tar.gz

をダウンロードして展開すると、typeclassesTut というディレクトリができる。
Coq veversion 8.4 でコンパイルする手順は以下である。
（version 8.4pl2 で確認）

- ``cd typeclassesTut``

- 以下の修正をする。

(1) ``cp V8.3/Matrics.v Mat.v``
(1') Section名をMatに修正する。
(2) Makefileの ``_CoqProject`` のエントリをコメントアウトする。

- make



# 本文とサンプルコードの対応

| 章節    | 表題                              |  サンプルソース      |   | 補足  |
|:--------|:---------------------------------|:----------------------|:---------|:------|
| 2.1	  | A Monomorphic Introduction       | Power_mono.v	|               |       |
| 2.2	  | On Monoids	                     | Monoid_prog.v 	| Monoid.v	|       |
| 2.2.1   | Classes and Instances	     | Monoid_prog.v 	| Monoid.v	|       |
| 2.2.2   | A generic deﬁnition of power     | Monoid_prog.v 	| Monoid.v	|       |
| 2.2.3   | Instance Resolution	             | Monoid_prog.v 	| Monoid.v	|       |
| 2.2.4	  | More Monoids	             | Mat.v		| |             |
| 2.2.4.1 | Matrices over some ring	     | Mat.v		| |             |
| 2.3	  | Reasoning within a Type Class    | Monoid_prog.v 	| Monoid.v      |  1.   |
| 2.3.1   | The Equivalence Proof	     | Monoid_prog.v 	| Monoid.v	|       |
| 2.3.2   | Some Useful Lemmas About power   | Monoid_prog.v 	| Monoid.v	|       |
| 2.3.3   | Final Steps	                     | Monoid_prog.v 	| Monoid.v	|       |
| 2.3.4   | Discharging the Context	     | Monoid_prog.v 	| Monoid.v	|       |
| 2.3.5   | Subclasses	                     | Monoid_prog.v 	| Monoid.v	|       |
| 3.1	  | Introduction: Lost in Manhattan  | Lost_in_NY.v 		| |     |
| 3.2	  | Data Types and Deﬁnitions	     | Lost_in_NY.v 		| |     |
| 3.3	  | Route Semantics	             | Lost_in_NY.v 		| |     |
| 3.4	  | On Route Equivalence	     | Lost_in_NY.v 		| |     |
| 3.5	  | Proper Functions	             | Lost_in_NY.v 		| |     |
| 3.6	  | Some Other instances of Proper   | Lost_in_NY.v 		| |     |
| 3.7	  | Deciding Route Equivalence	     | Lost_in_NY.v 		| |     |
| 3.8	  | Monoids and Setoids	             | Lost_in_NY.v 		| |     |
| 	  | (Class EMonoid)	             | EMonoid.v	| Monoid_op_classes.v |2.|
| 	  | (Fixpoint Epower)	             | EMonoid.v	| Monoid_op_classes.v |2.|
| 	  | (Abelian_EMonoid)	             | EMonoid.v	| |	              |
| 3.9	  | Advanced Features of Type Classes           | | |			      |
| 3.9.1   | Alternate deﬁnitions of the class Monoid	| | |		              |
| 3.9.2	  | Operational Type Classes	     | Monoid_op_classes.v | |		      |
| 3.9.3   | Instance Resolution	             | Monoid_op_classes.v | |		      |

1. Monoid.vはFunction版である。この以外の節で内容は重複している。
2. 内容はほぼ重複している。

以上
