公式


Topcoder Public Calendar
https://www.topcoder.com/community/events/

active contests
https://community.topcoder.com/longcontest/

forum(marathon matches)
https://apps.topcoder.com/forums/?module=Category&categoryID=17

contests archive(過去コンテスト)
https://community.topcoder.com/longcontest/stats/?module=MatchList

Practice (過去コンテストの提出ができる)
http://community.topcoder.com/longcontest/?module=ViewPractice

statistics(レートの更新が早い)
https://community.topcoder.com/longcontest/stats/?module=CoderRank

公式チュートリアル(Simulated Annealing)
https://www.topcoder.com/blog/approaching-marathon-match-task-pt-1/

---

非公式


コンテスト後のツイートまとめ
https://togetter.com/li/1243876

TopCoderマラソンマッチのはじめかた
http://shindannin.hatenadiary.com/entry/2014/10/05/003714

マラソンマッチにおける頻出Q＆Aと小技
https://topcoder.g.hatena.ne.jp/CKomaki/20141202/1418158488

[MM][雑談]Marathon Matchでいつもやってること
https://topcoder.g.hatena.ne.jp/tomerun/20120502/1335972842

マラソンマッチにおける精神論
http://chokudai.hatenablog.com/entry/2014/12/04/000132

マラソンマッチにおける典型データ構造とアプローチ
http://topcoder.g.hatena.ne.jp/agw/20141205

焼きなまし法のコツ Ver. 1.2
http://shindannin.hatenadiary.com/entry/20121224/1356364040

---

tester

配布: teater.jar ローカル用テスター seed=1~3ぐらいは要素数などランダムな値になるところを固定していことが多い

配布: ProblemVis.java　テスターの実装コード 問題分から抜けた制約などがあるので確認すること
内部で使用する分布や確率をテスターから出力させるようにコードを改変すると便利になることが多い

tester.jar の再構成:
```
jar xvf tester.jar
javac *.java &&\
jar cvfm tester.jar META-INF/MANIFEST.MF *.class &&\
rm *.class
```
