/////////////////////////////////

JP1/Baseバックアップ手順

/////////////////////////////////


# バックアップ対象
-1.定義ファイル
-2.共通定義情報
-3.jp1hosts2情報
-4.イベントDB(不要)

## rootユーザにスイッチ
[cac]
 $ su -

## 定義ファイルのバックアップ
取得対象ファイルを記載したjp1base_backupfile_list.txtを用意しておく
上記ファイルをもとに、バックアップ対象のファイルをアーカイブする
```
[root]
 cd /
 tar czvf /tmp/etcoptjp1base_`hostname`_`date +%Y%m%d`.tar.gz -T /tmp/jp1base_backupfile_list.txt
```
## 共通定義情報のバックアップ
jbsgetcnfコマンドを実行して共通定義情報を出力する
```
[root]
 /opt/jp1base/bin/jbsgetcnf > /tmp/jbsgetcnf_`hostname`_`date +%Y%m%d`; ls -ltr /tmp/jbsgetcnf*
```
## jp1hosts2情報のバックアップ
```
[root]
 /opt/jp1base/bin/jbshosts2export > /tmp/jbshosts2export_`hostname`_`date +%Y%m%d`; ls -ltr /tmp/jbshosts*
```
## イベントDBのバックアップ
不要

