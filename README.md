DCGAN
①実施内容\
　猫の顔画像をDCGANおよびLSGANで生成し、その精度を検証する。\
　64x64データでの実施はインターネットでもよく見かけるので、128x128のデータ生成を試みる。\
　参考HP：https://ajolicoeur.wordpress.com/cats/

②追加実施内容\
　最適化アルゴリズムおよび活性化関数をそれぞれ、RAdam, Mishに変更した場合の、DCGANおよびLSGANにおける影響を検証する（注）。
 
  　RAdam :https://qiita.com/omiita/items/d24568a835da6911b01e　
  
 　　　　  (原論文)      https://arxiv.org/abs/1908.03265 
       
  　　　　 (論文筆者の公開しているRAdamコード)      https://github.com/LiyuanLucasLiu/RAdam 
       
  Mish  :https://atmarkit.itmedia.co.jp/ait/articles/2004/28/news017.html
  
  
  注：ざっと調べたが、どちらともGANの分野での有効性を調べているような資料はあまり見つからなかった。\
  　　はじめはMishと同様にReluの代替関数として考案されたTanhexp関数を実装して使おうと考えましたが\
　　なぜかいつも学習途中でCUDAのエラーが出て止まるので、Pytorchで公式実装済みのMish関数を使うことにしました…。
