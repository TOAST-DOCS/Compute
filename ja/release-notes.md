<!-- pre-align:aligned sig=f73105f85d1d -->

<a id="compute-release-notes"></a>
## Compute > リリースノート { #compute-release-notes }

<a id="august-20-2026"></a>
## 2026. 08. 20.
### Image

* GPU関連(Linux)
    * NVIDIAドライバーのアップデート: 580.105.08 → 580.173.02
    * NVIDIAサーバードライバーパッケージの適用
    * CUDAツールキットの追加: 12.6
    * DCGM: 4.5.0 → 4.6.0
    * DCGM-Exporter: 4.6.0 → 4.8.3
        * PROF指標の収集のため、non-rootではなくrootで実行
        * GPUによって負のカウンターが発生する問題により、LOW_UTIL_VIOLATION指標の収集を除外処理
        * Exporterデータを外部から収集できるように、リッスンアドレス及びポートを0.0.0.0:9400に修正
    * MIG Manager: 0.13.1 → 0.14.4

* 新規イメージの追加
    * Ubuntu Server 22.04.5 LTS with NVIDIA (2026.08.20.)
    * Ubuntu Server 24.04.4 LTS with NVIDIA (2026.08.20.)
    * PentaSecurity WAPPLES SA 7.0.104.2-hatfix3 (2026.08.20.)

* イメージのサポート終了
    * Ubuntu Server 22.04.5 LTS with Redis 7.2.4 (2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA (2026.03.10.)
    * PentaSecurity WAPPLES SA 6.0.6 (2024.04.15.)

<a id="may-27-2026"></a>
## 2026. 05. 27. { #may-27-2026 }
<a id="instance"></a>
### Instance { #instance }
* インスタンス一覧照会 API の limit パラメータのデフォルト値 (default) を 100 件、最大値 (max) を 1,000 件に調整
* インスタンスの累積停止期間が 90 日を超えているかどうかの情報を提供

<a id="image"></a>
### Image { #image }
* イメージ一覧照会 API の limit パラメータのデフォルト値 (default) を 100 件、最大値 (max) を 1,000 件に調整

<a id="april-28-2026"></a>
## 2026. 04. 28. { #april-28-2026 }
<a id="april-28-2026-image"></a>
### Image

* 新規イメージ追加
    * Ubuntu Server 22.04.5 LTS for Deep Learning v8.0.0(2026.04.28.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v7.0.1(2026.04.28.)
    * Rocky Linux 8.10 with Tibero 7 Enterprise 294582(2026.04.28.)
    * Rocky Linux 8.10 with Tibero 7 Standard 294582(2026.04.28.)
    * Rocky Linux 9.7 with Tibero 7 Enterprise 294582(2026.04.28.)
    * Rocky Linux 9.7 with Tibero 7 Standard 294582(2026.04.28.)
    * Ubuntu Server 24.04.5 LTS with MySQL 8.0.45(2026.04.28.)
    * Ubuntu Server 24.04.5 LTS with CUBRID 11.4.4(2026.04.28.)
    * Ubuntu Server 24.04.5 LTS with CUBRID 10.2.17(2026.04.28.)
    * Ubuntu Server 24.04.5 LTS with Valkey 8.1.6(2026.04.28.)
    * Ubuntu Server 24.04.5 LTS with PostgreSQL 17(2026.04.28.)
    * Ubuntu Server 24.04.3 LTS with Apache Kafka 3.9.2(2026.04.28.)
    * Ubuntu Server 24.04.3 LTS with MariaDB 10.11.7(2026.04.28.)

* イメージサポート終了
    * Ubuntu Server 22.04.5 LTS for Deep Learning v6.0.1(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v7.0.0(2025.10.28.)
    * Rocky Linux 8.10 with Tibero 7 Enterprise 294582(2025.07.15.)
    * Rocky Linux 8.10 with Tibero 7 Standard 294582(2025.07.15.)
    * Rocky Linux 9.5 with Tibero 7 Enterprise 294582(2025.07.15.)
    * Rocky Linux 9.5 with Tibero 7 Standard 294582(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with Apache Kafka 3.6.1(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with CUBRID 10.2.14(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with CUBRID 11.0.13(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with MariaDB 10.11.7(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with MySQL 8.0.36(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with PostgreSQL 15(2025.07.15.)


<a id="march-31-2026"></a>
## 2026. 03. 31. { #march-31-2026 }
* アメリカ (カリフォルニア) リージョンのサービス終了

<a id="march-10-2026"></a>
## 2026. 03. 10. { #march-10-2026 }
<a id="march-10-2026-image"></a>
### Image { #march-10-2026-image }
* Rocky 9.7 イメージ GRUB BLS 設定の無効化
* Debian 11.11 bullseye-backports リポジトリのサポート終了に伴い、sources.list から削除

* GPU およびコンテナ関連 (Linux)
    * containerd: 1.6.32 → 2.2.1
    * NVIDIA ドライバーアップデート: 535.230.02 → 580.105.08
    * CUDA アップデート: 12.2 → 13.0
    * DCGM: 3.3.5 → 4.5.0
    * DCGM-Exporter: 3.3.5 → 4.5.0
    * MIG Manager: 0.7.0 → 0.13.1

* GPU (Windows)
    * NVIDIA ドライバーアップデート: 539.19 → 581.80
    * CUDA アップデート: 12.2 → 13.0

* セキュリティアップデート
    * Windows 2016: KB5071543
        * https://support.microsoft.com/en-us/topic/december-9-2025-kb5071543-os-build-14393-8688-ec93aa63-f343-4a7e-ab3c-faa096e17395
    * Windows 2019: KB5071544
        * https://support.microsoft.com/en-us/topic/december-9-2025-kb5071544-os-build-17763-8146-630aa62e-f399-4e42-9f7a-2a4d38dd1210
    * Windows 2022: KB5071547
        * https://support.microsoft.com/en-us/topic/december-9-2025-kb5071547-os-build-20348-4529-7935ca9f-cac3-4d17-93bb-fe8e57c6db32

* 新規イメージ追加
    * Debian 11.11 Bullseye(2026.03.10.)
    * Debian 12.13 Bookworm(2026.03.10.)
    * Rocky Linux 8.10(2026.03.10.)
    * Rocky Linux 8.10 - Container(2026.03.10.)
    * Rocky Linux 8.10 for NAT(2026.03.10.)
    * Rocky Linux 9.7(2026.03.10.)
    * Rocky Linux 9.7 - Container(2026.03.10.)
    * Ubuntu Server 22.04.5 LTS(2026.03.10.)
    * Ubuntu Server 22.04.5 LTS - Container(2026.03.10.)
    * Ubuntu Server 22.04.5 LTS for NAT(2026.03.10.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA(2026.03.10.)
    * Ubuntu Server 24.04.3 LTS(2026.03.10.)
    * Ubuntu Server 24.04.4 LTS - Container(2026.03.10.)
    * Windows 2016 STD(2026.03.10.) EN
    * Windows 2016 STD(2026.03.10.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard(2026.03.10.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard(2026.03.10.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard(2026.03.10.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard(2026.03.10.) KO
    * Windows 2016 STD with MS-SQL 2019 Express(2026.03.10.) EN
    * Windows 2016 STD with MS-SQL 2019 Express(2026.03.10.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard(2026.03.10.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard(2026.03.10.) KO
    * Windows 2019 STD(2026.03.10.) EN
    * Windows 2019 STD(2026.03.10.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard(2026.03.10.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard(2026.03.10.) KO
    * Windows 2022 STD(2026.03.10.) EN
    * Windows 2022 STD(2026.03.10.) KO
    * Windows 2022 STD with MS-SQL 2022 Standard(2026.03.10.) EN
    * Windows 2022 STD with MS-SQL 2022 Standard(2026.03.10.) KO
* イメージサポート終了
    * Debian 11.11 Bullseye(2025.07.15.)
    * Debian 12.10 Bookworm(2025.07.15.)
    * Rocky Linux 8.10(2025.07.15.)
    * Rocky Linux 8.10 for NAT(2025.07.15.)
    * Rocky Linux 8.10 - Container(2025.07.15.)
    * Rocky Linux 9.5(2025.07.15.)
    * Rocky Linux 9.5 - Container(2025.11.18.)
    * Ubuntu Server 22.04.5 LTS(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS - Container(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS for NAT(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA(2025.07.15.)
    * Ubuntu Server 24.04.2 LTS(2025.07.15.)
    * Ubuntu Server 24.04.3 LTS - Container(2025.11.18.)
    * Windows 2016 STD(2025.07.15.) EN
    * Windows 2016 STD(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2019 Express(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2019 Express(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.07.15.) KO
    * Windows 2019 STD(2025.07.15.) EN
    * Windows 2019 STD(2025.07.15.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.07.15.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.07.15.) KO
    * Windows 2022 STD(2025.07.15.) EN
    * Windows 2022 STD(2025.07.15.) KO
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.07.15.) EN
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.07.15.) KO

<a id="january-27-2026"></a>
## 2026. 01. 27. { #january-27-2026 }
<a id="january-27-2026-instance"></a>
### Instance { #january-27-2026-instance }
* シリアルコンソール機能の追加

<a id="november-25-2025"></a>
## 2025. 11. 25. { #november-25-2025 }
<a id="november-25-2025-image"></a>
### Image { #november-25-2025-image }
* イメージ修正機能の改善
    * イメージダウンロード機能の使用可否設定を追加

* 新規イメージ追加
    * Rocky Linux 9.5 - Container(2025.11.18.)
    * Ubuntu Server 24.04.3 LTS - Container(2025.11.18.)

<a id="instance-template"></a>
### Instance Template { #instance-template }
* スナップショットからのインスタンス作成機能の追加

<a id="auto-scale"></a>
### Auto Scale { #auto-scale }
* スナップショットからのインスタンス作成機能の追加

<a id="october-28-2025"></a>
## 2025. 10. 28. { #october-28-2025 }
<a id="october-28-2025-image"></a>
### Image { #october-28-2025-image }
* 新規イメージ追加
    * Ubuntu Server 22.04.5 LTS for Deep Learning v7.0.0(2025.10.28.)
* イメージサポート終了
    * Ubuntu Server 22.04.5 LTS for Deep Learning v5.0.2(2025.07.15.)

<a id="september-23-2025"></a>
## 2025. 09. 23. { #september-23-2025 }
<a id="september-23-2025-image"></a>
### Image { #september-23-2025-image }
* 新規イメージ追加
    * PIOLINK WEBFRONT-KS 4.0.6.62.20(2025.09.23.)
    * PIOLINK WEBFRONT-KS 4.0.6.61.33(2025.09.23.)
* イメージサポート終了
    * PIOLINK WEBFRONT-KS 4.0.6.61.32(2025.07.15.)

<a id="july-15-2025"></a>
## 2025. 07. 15. { #july-15-2025 }
<a id="july-15-2025-image"></a>
### Image { #july-15-2025-image }
* 新規イメージ追加
    * Debian 11.11 Bullseye(2025.07.15.)
    * Debian 12.10 Bookworm(2025.07.15.)
    * PIOLINK WEBFRONT-KS 4.0.6.61.32(2025.07.15.)
    * Rocky Linux 8.10(2025.07.15.)
    * Rocky Linux 8.10 - Container(2025.07.15.)
    * Rocky Linux 8.10 for NAT(2025.07.15.)
    * Rocky Linux 8.10 with Tibero 7 Enterprise 294582(2025.07.15.)
    * Rocky Linux 8.10 with Tibero 7 Standard 294582(2025.07.15.)
    * Rocky Linux 9.5(2025.07.15.)
    * Rocky Linux 9.5 with Tibero 7 Enterprise 294582(2025.07.15.)
    * Rocky Linux 9.5 with Tibero 7 Standard 294582(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS - Container(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v5.0.2(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v6.0.1(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS for NAT(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with Apache Kafka 3.6.1(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with CUBRID 10.2.14(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with CUBRID 11.0.13(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with MariaDB 10.11.7(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with MySQL 8.0.36(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with PostgreSQL 15(2025.07.15.)
    * Ubuntu Server 22.04.5 LTS with Redis 7.2.4(2025.07.15.)
    * Ubuntu Server 24.04.2 LTS(2025.07.15.)
    * Windows 2016 STD(2025.07.15.) EN
    * Windows 2016 STD(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2019 Express(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2019 Express(2025.07.15.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.07.15.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.07.15.) KO
    * Windows 2019 STD(2025.07.15.) EN
    * Windows 2019 STD(2025.07.15.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.07.15.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.07.15.) KO
    * Windows 2019 STD with NVIDIA(2025.07.15.) KO
    * Windows 2022 STD(2025.07.15.) EN
    * Windows 2022 STD(2025.07.15.) KO
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.07.15.) EN
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.07.15.) KO

* イメージサポート終了
    * Debian 11.11 Bullseye(2025.02.25.)
    * Debian 12.9 Bookworm(2025.02.25.)
    * PIOLINK WEBFRONT-KS 4.0.6.61.28(2023.04.25.)
    * Rocky Linux 8.10(2025.02.25.)
    * Rocky Linux 8.10 - Container(2025.02.25.)
    * Rocky Linux 8.10 for NAT(2025.02.25.)
    * Rocky Linux 8.10 with Tibero 7 Enterprise 277758(2025.03.25.)
    * Rocky Linux 8.10 with Tibero 7 Standard 277758(2025.03.25.)
    * Rocky Linux 9.5(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS - Container(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS for NAT(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.14(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2025.04.29.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with NVIDIA(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4(2025.03.25.)
    * Ubuntu Server 22.04.5 LTS(2025.02.25.)
    * Ubuntu Server 22.04.5 LTS - Container(2025.02.25.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v3.1.2(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v4.0.2(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v5.0.1(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v6.0.0(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA(2025.02.25.)
    * Ubuntu Server 24.04.1 LTS(2025.02.25.)
    * Windows 2016 STD(2025.02.25.) EN
    * Windows 2016 STD(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2019 Express(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2019 Express(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.02.25.) KO
    * Windows 2019 STD(2025.02.25.) EN
    * Windows 2019 STD(2025.02.25.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.02.25.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.02.25.) KO
    * Windows 2019 STD with NVIDIA(2025.02.25.) KO
    * Windows 2022 STD(2025.02.25.) EN
    * Windows 2022 STD(2025.02.25.) KO
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.02.25.) EN
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.02.25.) KO

<a id="may-27-2025"></a>
## 2025. 05. 27. { #may-27-2025 }
<a id="may-27-2025-instance"></a>
### Instance { #may-27-2025-instance }
* 配置ポリシー機能の追加
* ネットワークインターフェイス切断時の削除設定機能追加
* インスタンス作成またはブロックストレージ接続時のブロックストレージ削除ポリシー設定機能追加
* コンソールからインスタンス削除時の接続リソース削除ポリシーの改定
    * ブロックストレージ削除時に存在するスナップショットも合わせて削除

<a id="april-29-2025"></a>
## 2025. 04. 29. { #april-29-2025 }
<a id="april-29-2025-image"></a>
### Image { #april-29-2025-image }
* 新規イメージ追加
    * Ubuntu Server 22.04.5 LTS for Deep Learning v6.0.0(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v5.0.1(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v4.0.2(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v3.1.2(2025.04.29.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2025.04.29.)

* イメージサポート終了
    * Ubuntu Server 22.04.4 LTS for Deep Learning v5.0.0(2024.10.29)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v4.0.1(2024.10.29)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v3.1.1(2024.10.29)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2025.03.25)

<a id="march-25-2025"></a>
## 2025. 03. 25. { #march-25-2025 }
<a id="march-25-2025-image"></a>
### Image { #march-25-2025-image }
* 新規イメージ追加
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1(2024.03.25)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with Cubrid 10.2.14(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13(2025.03.25.)
    * Rocky Linux 8.10 with Tibero 7 Enterprise 277758(2025.03.25.)
    * Rocky Linux 8.10 with Tibero 7 Standard 277758(2025.03.25.)

* イメージサポート終了
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.14(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15.8(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4(2024.10.29.)
    * Rocky Linux 8.10 with Tibero 7 Enterprise 277758(2024.11.19.)
    * Rocky Linux 8.10 with Tibero 7 Standard 277758(2024.11.19.)

<a id="march-4-2025"></a>
## 2025. 03. 04. { #march-4-2025 }
<a id="march-4-2025-instance"></a>
### Instance { #march-4-2025-instance }
* インスタンスの説明変更機能を追加
* APIパスワード変更時、既存のパスワードと同じパスワードへの変更を制限
* ブロックストレージおよびスナップショットからのインスタンス作成機能を追加

<a id="march-4-2025-image"></a>
### Image { #march-4-2025-image }
* Rocky 8.10 のデフォルト Python が platform python に変更(python 3.11 → 3.6)

* GPU およびコンテナ関連(Linux)
    * containerd: 1.6.32 → 変更なし
    * NVIDIA ドライバーアップデート: 535.216.01 → 535.230.02
    * CUDA アップデート: 12.2 → 変更なし
    * DCGM: 3.3.5 → 変更なし
    * DCGM-Exporter: 3.3.5 → 変更なし
    * MIG Manager: 0.7.0 → 変更なし

* GPU(Windows)
    * NVIDIA ドライバーアップデート: 538.95 → 539.19
    * CUDA アップデート: 12.2 → 変更なし

* セキュリティアップデート
    * Windows 2016: KB5049993
        * https://support.microsoft.com/en-us/topic/january-14-2025-kb5049993-os-build-14393-7699-b148c0ad-29fd-460e-b4a2-db38e88ae937
    * Windows 2019: KB5050008
        * https://support.microsoft.com/en-us/topic/january-14-2025-kb5050008-os-build-17763-6775-9a174725-a7ea-4e37-a6f8-e86f7c4d3f31
    * Windows 2022: KB5049983
        * https://support.microsoft.com/en-us/topic/january-14-2025-kb5049983-os-build-20348-3091-789bf923-7777-419d-9c3a-23f7c814930f

* 新規イメージ追加
    * Debian 11.11 Bullseye(2025.02.25.)
    * Debian 12.9 Bookworm(2025.02.25.)
    * Rocky Linux 8.10(2025.02.25.)
    * Rocky Linux 8.10 - Container(2025.02.25.)
    * Rocky Linux 8.10 for NAT(2025.02.25.)
    * Rocky Linux 9.5(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS - Container(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS for NAT(2025.02.25.)
    * Ubuntu Server 20.04.6 LTS with NVIDIA(2025.02.25.)
    * Ubuntu Server 22.04.5 LTS(2025.02.25.)
    * Ubuntu Server 22.04.5 LTS - Container(2025.02.25.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA(2025.02.25.)
    * Ubuntu Server 24.04.1 LTS(2025.02.25.)
    * Windows 2016 STD(2025.02.25.) EN
    * Windows 2016 STD(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2019 Express(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2019 Express(2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard(2025.02.25.) KO
    * Windows 2019 STD(2025.02.25.) EN
    * Windows 2019 STD(2025.02.25.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.02.25.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard(2025.02.25.) KO
    * Windows 2019 STD with NVIDIA(2025.02.25.) KO
    * Windows 2022 STD(2025.02.25.) EN
    * Windows 2022 STD(2025.02.25.) KO
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.02.25.) EN
    * Windows 2022 STD with MS-SQL 2022 Standard(2025.02.25.) KO

* イメージサポート終了
    * Debian 11.11 Bullseye(2024.11.19.)
    * Debian 12.7 Bookworm(2024.11.19.)
    * Rocky Linux 8.10(2024.11.19.)
    * Rocky Linux 8.10 - Container(2024.11.19.)
    * Rocky Linux 8.10 for NAT(2024.11.19.)
    * Rocky Linux 9.4(2024.11.19.)
    * Ubuntu Server 20.04.6 LTS(2024.11.19.)
    * Ubuntu Server 20.04.6 LTS - Container(2024.11.19.)
    * Ubuntu Server 20.04.6 LTS for NAT(2024.11.19.)
    * Ubuntu Server 20.04.6 LTS with NVIDIA(2024.11.19.)
    * Ubuntu Server 22.04.5 LTS(2024.11.19.)
    * Ubuntu Server 22.04.5 LTS - Container(2024.11.19.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA(2024.11.19.)
    * Windows 2016 STD(2024.11.19.) EN
    * Windows 2016 STD(2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard(2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard(2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard(2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard(2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2019 Express(2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2019 Express(2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard(2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard(2024.11.19.) KO
    * Windows 2019 STD(2024.11.19.) EN
    * Windows 2019 STD(2024.11.19.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard(2024.11.19.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard(2024.11.19.) KO
    * Windows 2022 STD(2024.11.19.) EN
    * Windows 2022 STD(2024.11.19.) KO


<a id="december-24-2024"></a>
## 2024. 12. 24. { #december-24-2024 }
<a id="december-24-2024-image"></a>
### Image { #december-24-2024-image }
* Tibero イメージ名変更
  * Rocky Linux 8.10 with Tibero 7 Enterprise(2024.11.19.) → Rocky Linux 8.10 with Tibero 7 Enterprise 277758(2024.11.19.)
  * Rocky Linux 8.10 with Tibero 7 Standard(2024.11.19.) → Rocky Linux 8.10 with Tibero 7 Standard 277758(2024.11.19.)

<a id="november-26-2024"></a>
## 2024. 11. 26. { #november-26-2024 }
<a id="november-26-2024-instance"></a>
### Instance { #november-26-2024-instance }
* インスタンス OS 情報変更機能を追加

<a id="november-26-2024-image"></a>
### Image { #november-26-2024-image }
* イメージ修正機能の改善
  * 修正可能な項目を追加
    * OS バージョン値の設定
    * 最大 CPU 値の設定
    * 最小 CPU 値の設定
    * 最小メモリ値の設定
    * 最小ブロックストレージ値の設定
    * イメージ作成機能の使用有無の設定
    * ユーザースクリプト機能の使用有無の設定
    * 使用対象サービスの設定

* GPU およびコンテナ関連 (Linux)
    * containerd: 1.6.32 → 変更なし
    * NVIDIA ドライバーアップデート: 535.183.06 → 535.216.01
    * CUDA アップデート: 12.2 → 変更なし
    * DCGM: 3.3.5 → 変更なし
    * DCGM-Exporter: 3.4.1 → 変更なし
    * MIG Manager: 0.7.0 → 変更なし
    * 最小ディスクサイズ (GB): 20 → 30
    * DCGM-Exporter 未インストールの問題をパッチ (NVIDIA、Deep Learning イメージ)

* GPU (Windows)
    * NVIDIA ドライバーアップデート: 538.78 → 538.95
    * CUDA バージョン: 12.2

* セキュリティアップデート
    * Windows 2016: KB5044293
        * https://support.microsoft.com/en-us/topic/october-8-2024-kb5044293-os-build-14393-7428-3f172048-e2d1-4eb2-b6b9-41abd891e52f
    * Windows 2019: KB5044277
        * https://support.microsoft.com/en-us/topic/october-8-2024-kb5044277-os-build-17763-6414-edccc872-2f4e-4ac6-b224-50ca8f1acd4f
    * Windows 2022: KB5044281
        * https://support.microsoft.com/en-us/topic/october-8-2024-kb5044281-os-build-20348-2762-e063059c-9122-4324-86e8-4f6f3383a20a

* 新規イメージ追加
     * Rocky Linux 8.10 for NAT(2024.11.19.)
     * Rocky Linux 8.10 with Tibero 7 Enterprise(2024.11.19.)
     * Rocky Linux 8.10 with Tibero 7 Standard(2024.11.19.)
     * Rocky Linux 9.4(2024.11.19.)

* イメージサポート終了
     * CentOS 7.9(2024.08.20.)
     * CentOS 7.9 - Container(2024.08.20.)
     * CentOS 7.9 for NAT(2024.08.20.)
     * CentOS 7.9 with Apache Kafka 3.6.1(2024.04.23.)
     * CentOS 7.9 with CUBRID 10.2.14(2024.04.23.)
     * CentOS 7.9 with CUBRID 11.0.13(2024.04.23.)
     * CentOS 7.9 with MariaDB 10.11.7(2024.04.23.)
     * CentOS 7.9 with MySQL 8.0.36(2024.04.23.)
     * CentOS 7.9 with PostgreSQL 15.6(2024.04.23.)
     * CentOS 7.9 with Redis 7.2.4(2024.04.23.)
     * CentOS 7.9 with Tibero 7 CEE(2024.04.23.)
     * CentOS 7.9 with Tibero 7 CSE(2024.04.23.)


* イメージアップデート (Linux)
     * Debian 11.11 Bullseye(2024.11.19.)
     * Debian 12.7 Bookworm(2024.11.19.)
     * Rocky Linux 8.10(2024.11.19.)
     * Rocky Linux 8.10 - Container(2024.11.19.)
     * Ubuntu Server 20.04.6 LTS(2024.11.19.)
     * Ubuntu Server 20.04.6 LTS - Container(2024.11.19.)
     * Ubuntu Server 20.04.6 LTS for NAT(2024.11.19.)
     * Ubuntu Server 22.04.4 LTS for Deep Learning v3.1.1(2024.10.29.)
     * Ubuntu Server 22.04.4 LTS for Deep Learning v4.0.1(2024.10.29.)
     * Ubuntu Server 22.04.4 LTS for Deep Learning v5.0.0(2024.10.29.)
     * Ubuntu Server 20.04.6 LTS with NVIDIA(2024.11.19.)
     * Ubuntu Server 22.04.5 LTS(2024.11.19.)
     * Ubuntu Server 22.04.5 LTS - Container(2024.11.19.)
     * Ubuntu Server 22.04.5 LTS with NVIDIA(2024.11.19.)

* イメージアップデート (Windows)
     * Windows 2016 STD(2024.11.19.) EN
     * Windows 2016 STD(2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2016 Standard(2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2016 Standard(2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2017 Standard(2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2017 Standard(2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2019 Express(2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2019 Express(2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2019 Standard(2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2019 Standard(2024.11.19.) KO
     * Windows 2019 STD(2024.11.19.) EN
     * Windows 2019 STD(2024.11.19.) KO
     * Windows 2019 STD with MS-SQL 2019 Standard(2024.11.19.) EN
     * Windows 2019 STD with MS-SQL 2019 Standard(2024.11.19.) KO
     * Windows 2019 STD with NVIDIA(2024.11.19.) KO
     * Windows 2022 STD(2024.11.19.) EN
     * Windows 2022 STD(2024.11.19.) KO

<a id="image-builder"></a>
### Image Builder { #image-builder }
* アプリケーションバージョンのサポート終了
    * NHN Kubernetes Service(NKS) Worker Node 1.0
    * NHN Kubernetes Service(NKS) Worker Node(GPU) 1.0
    * MySQL 5.7
    * MariaDB 10.3
* ベースイメージのサポート終了
    * CentOS 7.9

<a id="october-29-2024"></a>
## 2024. 10. 29. { #october-29-2024 }
<a id="october-29-2024-image-builder"></a>
### Image Builder { #october-29-2024-image-builder }
* アプリケーションバージョンの追加
    * Deep Learning Framework 5.0

<a id="october-29-2024-image"></a>
### Image { #october-29-2024-image }
* 新規イメージ追加
    * Ubuntu Server 22.04.4 LTS for Deep Learning v3.1.1(2024.10.29.)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v4.0.1(2024.10.29.)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v5.0.0(2024.10.29.)

* イメージサポート終了
    * Ubuntu Server 22.04.3 LTS for Deep Learning v3.1.0(2023.11.21.)
    * Ubuntu Server 22.04.3 LTS for Deep Learning v4.0.0(2024.04.23.)

* イメージアップデート (Linux)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.14(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15.8(2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4(2024.10.29.)

<a id="august-27-2024"></a>
## 2024. 08. 27. { #august-27-2024 }
<a id="august-27-2024-image"></a>
### Image { #august-27-2024-image }
* GPU およびコンテナ関連 (Linux)
    * containerd: 1.6.31 → 1.6.32
    * NVIDIA ドライバーアップデート: 535.161.08 → 535.183.06
    * CUDA アップデート: 12.2 → 変更なし
    * MIG Manager: 0.7.0 → 変更なし
    * NVIDIA DCGM: 3.3.5 → 変更なし
    * NVIDIA DCGM Exporter: 3.4.1 → 変更なし

* GPU (Windows)
    * NVIDIA ドライバーアップデート: 538.46 → 538.78

* セキュリティアップデート (Windows)
    * Windows 2016: KB5040434
        * https://support.microsoft.com/en-us/topic/july-9-2024-kb5040434-os-build-14393-7159-40d1baef-65b4-467f-9bd9-729d369fcc4c
    * Windows 2019: KB5040430
        * https://support.microsoft.com/en-us/topic/july-9-2024-kb5040430-os-build-17763-6054-0bb10c24-db8c-47eb-8fa9-9ebc06afa4e7
    * Windows 2022: KB5040437
        * https://support.microsoft.com/en-us/topic/july-9-2024-kb5040437-os-build-20348-2582-5b28d9b8-fcba-43bb-91e6-062f43c7ec7c

* 新規イメージ追加
    * Debian 12.6 Bookworm (2024.08.20.)
    * Rocky Linux 8.10 (2024.08.20.)

* イメージサポート終了
    * Debian 10.13 Buster (2024.05.21.)
    * Rocky Linux 8.9 (2024.05.21.)

* イメージアップデート (Linux)
    * CentOS 7.9 (2024.08.20.)
    * CentOS 7.9 for NAT (2024.08.20.)
    * Debian 11.10 Bullseye (2024.08.20.)
    * Ubuntu Server 20.04.6 LTS (2024.08.20.)
    * Ubuntu Server 20.04.6 LTS for NAT (2024.08.20.)
    * Ubuntu Server 20.04.6 LTS with NVIDIA (2024.08.20.)
    * Ubuntu Server 22.04.4 LTS (2024.08.20.)
    * Ubuntu Server 22.04.4 LTS with NVIDIA (2024.08.20.)

* イメージアップデート (Windows)
    * Windows 2016 STD (2024.08.20.) EN
    * Windows 2016 STD (2024.08.20.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.08.20.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.08.20.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.08.20.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.08.20.) KO
    * Windows 2016 STD with MS-SQL 2019 Express (2024.08.20.) EN
    * Windows 2016 STD with MS-SQL 2019 Express (2024.08.20.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.08.20.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.08.20.) KO
    * Windows 2019 STD (2024.08.20.) EN
    * Windows 2019 STD (2024.08.20.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.08.20.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.08.20.) KO
    * Windows 2022 STD (2024.08.20.) EN
    * Windows 2022 STD (2024.08.20.) KO

<a id="public-api"></a>
### Public API { #public-api }
* 米国 (カリフォルニア) リージョンの追加

<a id="august-27-2024-instance"></a>
### Instance { #august-27-2024-instance }
* インスタンスキーペア変更機能の追加

<a id="august-27-2024-image-builder"></a>
### Image Builder { #august-27-2024-image-builder }
* アプリケーションサポートバージョンの追加
    * PostgreSQL 15
    * NHN Kubernetes Service (NKS) Worker Node 1.6
    * NHN Kubernetes Service (NKS) Worker Node (GPU) 1.6
* アプリケーションバージョンのサポート終了
    * PostgreSQL 10
    * PostgreSQL 11
    * PostgreSQL 12
    * PostgreSQL 13
    * PostgreSQL 14
    * Slurm 21.08
    * WebtoB 5.0
    * JEUS (Domain Administrator Server) 8
    * JEUS (Managed Server) 8
* 新規ベースイメージ追加
    * Rocky Linux 8.10
    * Debian 12 Bookworm
* ベースイメージのサポート終了
    * Rocky Linux 8.9
    * Debian 10 Buster
    * Debian 11 Bullseye
        * NHN Kubernetes Service (NKS) Worker Node / NHN Kubernetes Service (NKS) Worker Node (GPU) 該当

<a id="may-28-2024"></a>
## 2024. 05. 28. { #may-28-2024 }
<a id="may-28-2024-instance"></a>
### Instance { #may-28-2024-instance }
* インスタンス一覧内の検索/フィルター条件の拡張および UI 改善
    * 検索条件の追加
        * インスタンス名
        * インスタンスタイプ
        * イメージ ID
    * フィルター条件の追加
        * イメージタイプ
        * インスタンスの状態

<a id="may-28-2024-image"></a>
### Image { #may-28-2024-image }
* GPU およびコンテナ関連 (Linux)
    * containerd: 1.6.27 → 1.6.31
    * NVIDIA ドライバーアップデート: 535.154.05 → 535.161.08
    * CUDA アップデート: 12.2 → 変更なし
    * MIG Manager: 0.5.5 → 0.7.0
    * NVIDIA DCGM: 3.1.8 → 3.3.5
    * NVIDIA DCGM Exporter: 3.1.5 → 3.4.1

* GPU (Windows)
    * NVIDIA ドライバーアップデート: 538.46 → 538.15

* セキュリティアップデート (Windows)
    * Windows 2016: KB5036899
        * https://support.microsoft.com/en-us/topic/april-9-2024-kb5036899-os-build-14393-6897-6a0b7cdd-dd67-4ef8-8c38-8a936b2f952c
    * Windows 2019: KB5036896
        * https://support.microsoft.com/en-us/topic/april-9-2024-kb5036896-os-build-17763-5696-efb580f1-2ce4-4695-b76c-d2068a00fb92
    * Windows 2022: KB5036909
        * https://support.microsoft.com/en-us/topic/april-9-2024-kb5036909-os-build-20348-2402-36062ce9-f426-40c6-9fb9-ee5ab428da8c

* イメージ更新 (Linux)
    * CentOS 7.9 (2024.05.21.)
    * CentOS 7.9 - Container (2024.05.21.)
    * CentOS 7.9 for NAT (2024.05.21.)
    * Debian 10.13 Buster (2024.05.21.)
    * Debian 11.9 Bullseye (2024.05.21.)
    * Rocky Linux 8.9 (2024.05.21.)
    * Ubuntu Server 20.04.6 LTS (2024.05.21.)
    * Ubuntu Server 20.04.6 LTS for NAT (2024.05.21.)
    * Ubuntu Server 22.04.4 LTS (2024.05.21.)

* イメージ更新 (Windows)
    * Windows 2016 STD (2024.05.21.) EN
    * Windows 2016 STD (2024.05.21.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.05.21.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.05.21.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.05.21.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.05.21.) KO
    * Windows 2016 STD with MS-SQL 2019 Express (2024.05.21.) EN
    * Windows 2016 STD with MS-SQL 2019 Express (2024.05.21.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.05.21.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.05.21.) KO
    * Windows 2019 STD (2024.05.21.) EN
    * Windows 2019 STD (2024.05.21.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.05.21.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.05.21.) KO
    * Windows 2022 STD (2024.05.21.) EN
    * Windows 2022 STD (2024.05.21.) KO


<a id="april-23-2024"></a>
## 2024. 04. 23. { #april-23-2024 }
<a id="april-23-2024-instance"></a>
### Instance { #april-23-2024-instance }
* インスタンスタイプの利用終了 - 韓国(板橋)リージョン該当
    * u2(Ephemeral Storage Instance)

<a id="april-23-2024-image"></a>
### Image { #april-23-2024-image }
* 新規イメージ追加
    * CentOS 7.9 with Apache Kafka 3.6.1(2024.04.23.)
    * CentOS 7.9 with CUBRID 10.2.14(2024.04.23.)
    * CentOS 7.9 with CUBRID 11.0.13(2024.04.23.)
    * CentOS 7.9 with MariaDB 10.11.7(2024.04.23.)
    * CentOS 7.9 with MySQL 8.0.36(2024.04.23.)
    * CentOS 7.9 with PostgreSQL 15.6(2024.04.23.)
    * CentOS 7.9 with Redis 7.2.4(2024.04.23.)
    * CentOS 7.9 with Tibero 7 CEE(2024.04.23.)
    * CentOS 7.9 with Tibero 7 CSE(2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1(2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.14(2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13(2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36(2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15.6(2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4(2024.04.23.)
    * Ubuntu Server 22.04.3 LTS for Deep Learning v4.0.0(2024.04.23.)

* イメージサポート終了
    * CentOS 7.9 with Apache Kafka 3.3.1(2022.12.20.)
    * CentOS 7.9 with CUBRID 10.2.10(2023.03.21.)
    * CentOS 7.9 with CUBRID 11.0.10(2023.03.21.)
    * CentOS 7.9 with MariaDB 10.3.31(2022.12.20.)
    * CentOS 7.9 with MariaDB 10.6.11(2023.03.21.)
    * CentOS 7.9 with MySQL 5.7.35(2022.12.20.)
    * CentOS 7.9 with MySQL 8.0.27(2022.12.20.)
    * CentOS 7.9 with PostgreSQL 10.20(2022.12.20.)
    * CentOS 7.9 with PostgreSQL 11.15(2022.12.20.)
    * CentOS 7.9 with PostgreSQL 12.10(2022.12.20.)
    * CentOS 7.9 with PostgreSQL 13.6(2022.12.20.)
    * CentOS 7.9 with PostgreSQL 14.2(2022.12.20.)
    * CentOS 7.9 with Redis 7.0.5(2022.12.20.)
    * CentOS 7.9 with Tibero 7 CEE(2023.10.31.)
    * CentOS 7.9 with Tibero 7 CSE(2023.10.31.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.3.1(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.10(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.10(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.6.11(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.27(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.0.5(2023.03.21.)

<a id="april-15-2024"></a>
## 2024. 04. 15. { #april-15-2024 }
<a id="april-15-2024-image"></a>
### Image { #april-15-2024-image }
* イメージアップデート
    * PentaSecurity WAPPLES SA 6.0.6(2024.04.15.)

<a id="march-26-2024"></a>
## 2024. 03. 26. { #march-26-2024 }
<a id="march-26-2024-image-builder"></a>
### Image Builder { #march-26-2024-image-builder }
* アプリケーションバージョン追加
    * Deep Learning Framework 4.0

<a id="february-27-2024"></a>
## 2024. 02. 27. { #february-27-2024 }
<a id="february-27-2024-image"></a>
### Image { #february-27-2024-image }
* 新規イメージ追加
    * Rocky Linux 8.9(2024.02.20.)

* イメージサポート終了
    * Rocky Linux 8.8(2023.11.21.)

* GPU およびコンテナ関連 (Linux)
    * containerd: 1.6.22 → 1.6.27
    * NVIDIA ドライバーアップデート: 535.104.12 → 535.154.05
    * CUDA アップデート: 12.2 → 変更なし
    * MIG Manager: 0.5.5 → 変更なし

* GPU (Windows)
    * NVIDIA ドライバーアップデート: 537.13 → 538.15

* セキュリティアップデート (Windows)
    * Windows 2016: KB5034119
        * https://support.microsoft.com/en-us/topic/january-9-2024-kb5034119-os-build-14393-6614-7e7dae78-5944-4041-bf3d-4660e5ef7bb4
    * Windows 2019: KB5034127
        * https://support.microsoft.com/en-gb/topic/january-9-2024-kb5034127-os-build-17763-5329-4de58ce5-eb0d-4b9a-95d1-aa15fe30b082
    * Windows 2022: KB5034129
        * https://support.microsoft.com/en-us/topic/january-9-2024-kb5034129-os-build-20348-2227-6958a36f-efaf-4ef5-a576-c5931072a89a

* イメージアップデート (Linux)
    * CentOS 7.9(2024.02.20.)
    * CentOS 7.9 for NAT(2024.02.20.)
    * Debian 10.13 Buster(2024.02.20.)
    * Debian 11.8 Bullseye(2024.02.20.)
    * Rocky Linux 8.9(2024.02.20.)
    * Ubuntu Server 20.04.6 LTS(2024.02.20.)
    * Ubuntu Server 20.04.6 LTS for NAT(2024.02.20.)
    * Ubuntu Server 22.04.3 LTS(2024.02.20.)

* イメージアップデート (Windows)
    * Windows 2016 STD(2024.02.20.) EN
    * Windows 2016 STD(2024.02.20.) KO
    * Windows 2019 STD(2024.02.20.) EN
    * Windows 2019 STD(2024.02.20.) KO
    * Windows 2022 STD(2024.02.20.) EN
    * Windows 2022 STD(2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard(2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard(2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard(2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard(2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2019 Express(2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2019 Express(2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard(2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard(2024.02.20.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard(2024.02.20.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard(2024.02.20.) KO

<a id="february-27-2024-instance"></a>
### Instance { #february-27-2024-instance }
* 暗号化されたルートブロックストレージのインスタンスからのイメージ作成機能を追加
* GPU Instance でのインスタンス終了機能を無効化


<a id="november-28-2023"></a>
## 2023. 11. 28. { #november-28-2023 }
<a id="november-28-2023-instance"></a>
### Instance { #november-28-2023-instance }
* インスタンス終了機能の追加

<a id="november-28-2023-public-api"></a>
### Public API { #november-28-2023-public-api }
* インスタンスの終了、終了済みインスタンスの起動 API の追加

<a id="november-28-2023-image"></a>
### Image { #november-28-2023-image }
* イメージ共有メンバー数の制限解除

* 新規イメージ追加
	* Ubuntu Server 22.04.3 LTS with NVIDIA(2023.11.21.)
	* Ubuntu Server 22.04.3 LTS - Container(2023.11.21.)
	* Ubuntu Server 22.04.3 LTS for Deep Learning v3.1.0(2023.11.21.)

* イメージサポート終了
	* Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.1(2023.09.26.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.1(2023.09.26.)

* GPU およびコンテナ関連 (Linux)
    * debian 11 container - gpu driver 追加/gpu flavor 選択後にクラスターを作成可能
    * NVIDIA ドライバーの更新: 470.199.02 → 535.104.12
    * CUDA の更新: 11.4 → 12.2
    * MIG Manager: 0.5.4 → 0.5.5

* GPU (Windows)
	* NVIDIA ドライバーの更新: 474.44 → 537.13

* セキュリティアップデート (Linux)
	* CentOS 7.9: /usr/bin/newgrp、/sbin/unix_chkpwd SetUID の削除

* セキュリティアップデート (Windows)
	* Windows 2016: KB5031362
		* https://support.microsoft.com/en-au/topic/october-10-2023-kb5031362-os-build-14393-6351-0c6e713e-3d6a-4593-8a75-af0a605f249c
	* Windows 2019: KB5031361
		* https://support.microsoft.com/en-gb/topic/october-10-2023-kb5031361-os-build-17763-4974-766593db-b47a-4b18-a698-906426860313
	* Windows 2022: KB5031364
		* https://support.microsoft.com/en-us/topic/october-10-2023-kb5031364-os-build-20348-2031-7f1d69e7-c468-4566-887a-1902af791bbc

* イメージの更新 (Linux)
	* CentOS 7.9(2023.11.21.)
	* Debian 10.13 Buster(2023.11.21.)
	* Debian 11.8 Bullseye(2023.11.21.)
	* Rocky Linux 8.8(2023.11.21.)
	* Ubuntu Server 20.04.6 LTS(2023.11.21.)
	* Ubuntu Server 22.04.3 LTS(2023.11.21.)
	* CentOS 7.9 for NAT(2023.11.21.)
	* Ubuntu Server 20.04.6 LTS for NAT(2023.11.21.)
	* CentOS 7.9 - Container(2023.11.21.)
	* Debian 11.8 Bullseye - Container(2023.11.21.)
	* Rocky Linux 8.8 - Container(2023.11.21.)
	* Ubuntu Server 20.04.6 LTS - Container(2023.11.21.)
	* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.11.21.)

* イメージの更新 (Windows)
	* Windows 2016 STD(2023.11.21.) EN
	* Windows 2016 STD(2023.11.21.) KO
	* Windows 2019 STD(2023.11.21.) EN
	* Windows 2019 STD(2023.11.21.) KO
	* Windows 2022 STD(2023.11.21.) EN
	* Windows 2022 STD(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2016 Standard(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2016 Standard(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2017 Standard(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2017 Standard(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2019 Express(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2019 Express(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2019 Standard(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2019 Standard(2023.11.21.) KO
	* Windows 2019 STD with MS-SQL 2019 Standard(2023.11.21.) EN
	* Windows 2019 STD with MS-SQL 2019 Standard(2023.11.21.) KO


<a id="bare-metal-instance"></a>
### Bare Metal Instance { #bare-metal-instance }
* Bare Metal Instance サービスのリリース

<a id="october-31-2023"></a>
## 2023. 10. 31. { #october-31-2023 }

<a id="system-monitoring"></a>
### System Monitoring { #system-monitoring }
* バグ修正
  * プロジェクトから除外したユーザーに引き続きアラームが送信されていた問題を修正

<a id="october-31-2023-image"></a>
### Image { #october-31-2023-image }
* 新規イメージ追加
    * CentOS 7.9 with Tibero 7 CSE(2023.10.31.)
    * CentOS 7.9 with Tibero 7 CEE(2023.10.31.)

* イメージサポート終了
    * CentOS 7.9 with Tibero 6(2022.12.20.)


<a id="september-26-2023"></a>
## 2023. 09. 26. { #september-26-2023 }
<a id="september-26-2023-image"></a>
### Image { #september-26-2023-image }
* 新規イメージ追加
    * Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.1(2023.09.26.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.1(2023.09.26.)
    * PentaSecurity WAPPLES SA 6.0.6(2023.09.26.)

* イメージサポート終了
    * Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.0(2023.06.27.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.0(2023.08.22.)
    * Windows 2012 R2 STD(2023.08.22.) EN
    * Windows 2012 R2 STD(2023.08.22.) KO
    * Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) KO

* PIOLINK WEBFRONT-KS 4.0.6.61.28(2023.04.25.)
    * イメージ名の変更 PLOS-WAF-KS-v4.0.6.61.28(2023.04.25.) → PIOLINK WEBFRONT-KS 4.0.6.61.28(2023.04.25.)

<a id="august-29-2023"></a>
## 2023. 08. 29. { #august-29-2023 }
<a id="august-29-2023-public-api"></a>
### Public API { #august-29-2023-public-api }
* イメージアップロード/ダウンロード API 追加

<a id="august-29-2023-image"></a>
### Image { #august-29-2023-image }
* 新規イメージ追加
    * Rocky Linux 8.8(2023.08.22.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.0(2023.08.22.)
    * CentOS 7.9 for NAT(2023.08.22.)

* イメージサポート終了
    * Rocky Linux 8.7(2023.05.25.)

* GPU
    * NVIDIA ドライバーアップデート(Linux): 470.182.03 → 470.199.02
    * dcgm アップデート(Linux): 3.1.7 → 3.1.8
    * NVIDIA ドライバーアップデート(Windows): 474.30 → 474.44

* イメージ名変更
    * Ubuntu Server 20.04.6 LTS for Deep Learning(2023.06.27.) → Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.0(2023.06.27.)

* CentOS 7.9(2023.08.22.)
    * イメージアップデート
* Debian 10.13 Buster(2023.08.22.)
    * イメージアップデート
* Debian 11.7 Bullseye(2023.08.22.)
    * イメージアップデート
* Ubuntu Server 20.04.6 LTS(2023.08.22.)
    * イメージアップデート
* Ubuntu Server 20.04.6 LTS for NAT(2023.08.22.)
    * イメージアップデート
* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.08.22.)
    * イメージアップデート
* Ubuntu Server 22.04.2 LTS(2023.08.22.)
    * イメージアップデート
* Windows 2012 R2 STD(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2016 STD(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2016 Standard(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2017 Standard(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2017 Standard(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Express(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Express(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Standard(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Standard(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2019 STD(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with MS-SQL 2019 Standard(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with MS-SQL 2019 Standard(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with NVIDIA(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2022 STD(2023.08.22.) EN
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/july-11-2023-security-update-kb5028171-34557119-e00c-4678-bb87-048a36ed8585
* Windows 2022 STD(2023.08.22.) KO
    * イメージアップデート
    * 2023年7月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/july-11-2023-security-update-kb5028171-34557119-e00c-4678-bb87-048a36ed8585

<a id="august-29-2023-instance"></a>
### Instance { #august-29-2023-instance }
* インスタンス削除時に、インスタンスに関連付けられているフローティング IP および追加ブロックストレージを同時に削除する機能を追加

<a id="august-29-2023-instance-template"></a>
### Instance Template { #august-29-2023-instance-template }
* 暗号化ブロックストレージタイプのサポート

<a id="scaling-group"></a>
### Scaling Group { #scaling-group }
* 暗号化ブロックストレージタイプのサポート


<a id="july-25-2023"></a>
## 2023. 07. 25. { #july-25-2023 }
<a id="july-25-2023-image-builder"></a>
### Image Builder { #july-25-2023-image-builder }
* アプリケーションバージョン追加
    * Deep Learning Framework 3.0.0


<a id="june-27-2023"></a>
## 2023. 06. 27. { #june-27-2023 }
<a id="june-27-2023-system-monitoring"></a>
### System Monitoring { #june-27-2023-system-monitoring }
* **[月間指標レポート]** 機能使用時に、間欠的にExcelの生成が完了しない問題を修正
* Windows agent
    * 高可用性機能の改善
    * ログ追加

<a id="june-27-2023-image-builder"></a>
### Image Builder { #june-27-2023-image-builder }
* アプリケーションバージョン追加
    * Deep Learning Framework 2.1.0
* アプリケーションバージョンサポート終了
    * Deep Learning Framework 2.0.1

<a id="june-27-2023-image"></a>
### Image { #june-27-2023-image }
* GPU
    * NVIDIA ドライバーアップデート(Linux): 470.182.03

* Ubuntu Server 20.04.6 LTS for Deep Learning(2023.06.27.)
    * イメージアップデート

<a id="may-30-2023"></a>
## 2023. 05. 30. { #may-30-2023 }

<a id="may-30-2023-instance"></a>
### Instance { #may-30-2023-instance }
* **CloudTrail** のインスタンス作成およびインスタンス削除ログの改善
* インスタンス作成時に既存のネットワークインターフェイスを複数指定できるよう UI を改善

<a id="may-30-2023-image-builder"></a>
### Image Builder { #may-30-2023-image-builder }
* アプリケーションの追加
    * NHN Kubernetes Service(NKS) Worker Node
    * NHN Kubernetes Service(NKS) Worker Node(GPU)

<a id="may-30-2023-image"></a>
### Image { #may-30-2023-image }
* 新規イメージ追加
    * Rocky Linux 8.7(2023.05.25.)
    * Ubuntu Server 20.04.6 LTS for NAT(2023.05.25.)

* イメージサポート終了
    * Rocky Linux 8.6(2023.03.21.)
    * Ubuntu Server 18.04.6 LTS(2023.02.21.)
    * Ubuntu Server 18.04.6 LTS for NAT(2023.02.21.)
    * Ubuntu Server 18.04.5 LTS for AI(2021.06.22.)
    * Ubuntu Server 18.04.6 LTS with NVIDIA(2023.03.21.)

* GPU
    * NVIDIA ドライバーアップデート (Linux): 450.216.04 → 470.182.03
    * NVIDIA ドライバーアップデート: 453.94 → 474.30

* CentOS 7.9(2023.05.25.)
    * イメージ更新
* Debian 10.13 Buster(2023.05.25.)
    * イメージ更新
    * Multi NIC 設定時にアクセスできない問題の対処
* Debian 11.6 Bullseye(2023.05.25.)
    * イメージ更新
    * cgroup v2 無効化の設定
* Ubuntu Server 20.04.6 LTS(2023.05.25.)
    * イメージ更新
* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.05.25.)
    * イメージ更新
* Ubuntu Server 20.04.6 LTS for Deep Learning(2023.05.25.)
    * イメージ更新
* Ubuntu Server 22.04.2 LTS(2023.05.25.)
    * イメージ更新
* Windows 2012 R2 STD(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2012 R2 STD(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2016 STD(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2019 STD(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2019 STD(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2022 STD(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-gb/topic/april-11-2023-kb5025230-os-build-20348-1668-28a5446e-6389-4a5b-ae3f-e942a604f2d3
* Windows 2022 STD(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-gb/topic/april-11-2023-kb5025230-os-build-20348-1668-28a5446e-6389-4a5b-ae3f-e942a604f2d3
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2016 STD with MS-SQL 2016 Standard(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2016 Standard(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2017 Standard(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2017 Standard(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Express(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Express(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Standard(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Standard(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2019 STD with MS-SQL 2019 Standard(2023.05.25.) EN
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2019 STD with MS-SQL 2019 Standard(2023.05.25.) KO
    * イメージ更新
    * 23年11月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f

<a id="april-25-2023"></a>
## 2023. 04. 25. { #april-25-2023 }
<a id="april-25-2023-image"></a>
### Image { #april-25-2023-image }
* 新規イメージ追加
    * Ubuntu Server 20.04.6 LTS for Deep Learning(2023.04.25.)
    * PLOS-WFK-KS-v4.0.6.61.28(2023.04.25.)

* イメージサポート終了
    * Ubuntu Server 18.04.6 LTS for Deep Learning(2022.01.25.)
    * PLOS-WFK-KS-v4.0.6.61.25(2022.09.20.)

<a id="april-25-2023-system-monitoring"></a>
### System Monitoring { #april-25-2023-system-monitoring }
* バグ修正
    * ダウンロードした月次メトリクスレポートが断続的に正常に実行されない問題の修正

<a id="march-28-2023"></a>
## 2023. 03. 28. { #march-28-2023 }
<a id="march-28-2023-image"></a>
### Image { #march-28-2023-image }
* 新規イメージ追加
    * CentOS 7.9 with CUBRID 10.2.10(2023.03.21.)
    * CentOS 7.9 with CUBRID 11.0.10(2023.03.21.)
    * CentOS 7.9 with MariaDB 10.6.11(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.27(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.0.5(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.3.1(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.10(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.10(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.6.11(2023.03.21.)

* イメージサポート終了
    * CentOS 7.9 with CUBRID 10.2.4(2022.12.20.)
    * CentOS 7.9 with CUBRID 11.0.2(2022.12.20.)

* Debian 10.13 Buster(2023.03.21.)
    * イメージ更新
* Debian 11.6 Bullseye(2023.03.21.)
    * イメージ更新
* Rocky Linux 8.6(2023.03.21.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS(2023.03.21.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS for NAT(2023.03.21.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS with NVIDIA(2023.03.21.)
    * イメージ更新
* Ubuntu Server 20.04.6 LTS(2023.03.21.)
    * イメージ更新
* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.03.21.)
    * イメージ更新
* Ubuntu Server 22.04.2 LTS(2023.03.21.)
    * イメージ更新

<a id="march-28-2023-image-builder"></a>
### Image Builder { #march-28-2023-image-builder }
* 新機能追加
    * イメージビルド時に個人イメージをベースイメージとして選択可能

<a id="march-28-2023-public-api"></a>
### Public API { #march-28-2023-public-api }
* API エンドポイントの変更

<a id="march-28-2023-system-monitoring"></a>
### System Monitoring { #march-28-2023-system-monitoring }
* 月次メトリクスレポートの期間選択条件から `1分` オプションを除外

<a id="february-28-2023"></a>
## 2023. 02. 28. { #february-28-2023 }

<a id="february-28-2023-image"></a>
### Image { #february-28-2023-image }
* 新規イメージ追加
    * Ubuntu Server 22.04.1 LTS(2023.02.21.)
    * Ubuntu Server 20.04.5 LTS with NVIDIA(2023.02.21.)

* カーネルアップデート

* GPU
    * NVIDIA ドライバーアップデート(Windows): 453.51 → 453.94
    * NVIDIA ドライバーアップデート(Linux): 450.191.01 → 450.216.04

* Rocky Linux 8.6(2023.02.21.)
    * イメージアップデート
* Debian 10.13 Buster(2023.02.21.)
    * イメージアップデート
* Debian 11.6 Bullseye(2023.02.21.)
    * イメージアップデート
* Ubuntu Server 18.04.6 LTS(2023.02.21.)
    * イメージアップデート
* Ubuntu Server 18.04.6 LTS for NAT(2023.02.21.)
    * イメージアップデート
* Ubuntu Server 20.04.5 LTS(2023.02.21.)
    * イメージアップデート
* Ubuntu Server 18.04.6 LTS with NVIDIA(2023.02.21.)
    * イメージアップデート
* Windows 2012 R2 STD(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022352-monthly-rollup-cf299bf2-707b-47db-89a5-4e22c5ce4e26
* Windows 2016 STD(2023.02.14.)
    * イメージアップデート: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
    * 23年1月セキュリティアップデート適用
* Windows 2019 STD(2023.02.14.)
    * イメージアップデート: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022286-os-build-17763-3887-48683103-7b22-4f36-aa98-0049c7a6e579
    * 23年1月セキュリティアップデート適用
* Windows 2022 STD(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022291-os-build-20348-1487-38772acf-103f-463e-9d60-486174e806b2
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022352-monthly-rollup-cf299bf2-707b-47db-89a5-4e22c5ce4e26
* Windows 2016 STD with MS-SQL 2016 Standard(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2017 Standard(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2019 Express(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2019 Standard(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2019 STD with MS-SQL 2019 Standard(2023.02.14.)
    * イメージアップデート
    * 23年1月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022286-os-build-17763-3887-48683103-7b22-4f36-aa98-0049c7a6e579

<a id="february-28-2023-image-builder"></a>
### Image Builder { #february-28-2023-image-builder }
* 新規ベースイメージ追加
    * Ubuntu 20.04
* アプリケーションバージョン追加
    * CUBRID 10.2.10
    * CUBRID 11.0.10
    * MariaDB 10.6.11
* アプリケーションバージョンのサポート終了
    * CUBRID 10.2.4
    * CUBRID 11.0.2

<a id="january-31-2023"></a>
## 2023. 01. 31. { #january-31-2023 }

<a id="january-31-2023-instance"></a>
### Instance { #january-31-2023-instance }
* **[インスタンステンプレート]** からインスタンスを作成する際に設定値を変更できるよう UI を改善
* インスタンス情報 UI を改善

<a id="january-31-2023-instance-template"></a>
### Instance Template { #january-31-2023-instance-template }
* **[インスタンステンプレートのオーナー変更]** 機能を追加

<a id="january-31-2023-auto-scale"></a>
### Auto Scale { #january-31-2023-auto-scale }
* **[スケーリンググループのオーナー変更]** 機能を追加
* **[インスタンステンプレート]** からスケーリンググループを作成する際に設定値を変更できるよう UI を改善

<a id="december-27-2022"></a>
## 2022. 12. 27. { #december-27-2022 }

<a id="december-27-2022-image"></a>
### Image { #december-27-2022-image }
* 新規イメージ追加
    * CentOS 7.9 with Apache Kafka 3.3.1(2022. 12. 20.)
    * CentOS 7.9 with CUBRID 10.2.4(2022. 12. 20.)
    * CentOS 7.9 with CUBRID 11.0.2(2022. 12. 20.)
    * CentOS 7.9 with JEUS8Fix1(Domain Administrator Server 2022. 12. 20.)
    * CentOS 7.9 with JEUS8Fix1(Managed Server 2022. 12. 20.)
    * CentOS 7.9 with MariaDB 10.3.31(2022. 12. 20.)
    * CentOS 7.9 with MySQL 5.7.35(2022. 12. 20.)
    * CentOS 7.9 with MySQL 8.0.27(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 10.20(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 11.15(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 12.10(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 13.6(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 14.2(2022. 12. 20.)
    * CentOS 7.9 with Redis 7.0.5(2022. 12. 20.)
    * CentOS 7.9 with Tibero 6(2022. 12. 20.)
    * CentOS 7.9 with WebtoB5Fix4(2022. 12. 20.)
* イメージサポート終了
    * CentOS 7.8(2021. 12. 21.)
    * CentOS 7.8 with CUBRID 10.2.4(2021. 12. 21.)
    * CentOS 7.8 with CUBRID 11.0.2(2021. 12. 21.)
    * CentOS 7.8 with JEUS8Fix1(Domain Administrator Server 2022. 03. 22.)
    * CentOS 7.8 with JEUS8Fix1(Managed Server 2022. 03. 22.)
    * CentOS 7.8 with MariaDB 10.3.31(2022.11.4)
    * CentOS 7.8 with MySQL 5.7.20(2021. 12. 21.)
    * CentOS 7.8 with MySQL 5.7.32(2021. 12. 21.)
    * CentOS 7.8 with MySQL 8.0.22(2021. 12. 21.)
    * CentOS 7.8 with PostgreSQL 10.20(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 11.15(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 12.10(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 13.6(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 14.2(2022. 05. 17.)
    * CentOS 7.8 with Tibero 6(2022. 01. 25.)
    * CentOS 7.8 with WebtoB5Fix4(2022. 03. 22.)

<a id="december-27-2022-image-builder"></a>
### Image Builder { #december-27-2022-image-builder }
* 新規ベースイメージ追加
    * CentOS 7.9
* ベースイメージのサポート終了
    * CentOS 7.8

<a id="november-29-2022"></a>
## 2022. 11. 29. { #november-29-2022 }
<a id="november-29-2022-instance"></a>
### Instance { #november-29-2022-instance }
* インスタンス管理の**フィルター条件**に削除保護（全体/設定/未設定）を追加
* ネットワークインターフェイス別に設定されたセキュリティグループの変更機能を改善
* インスタンス情報 UI を改善
* 削除保護トグルボタンを追加
* 削除保護の一括設定機能を改善

<a id="november-29-2022-image"></a>
### Image { #november-29-2022-image }
* 新規イメージ追加
    * CentOS 7.9(2022. 11. 22.)
    * CentOS 7.9 for NAT(2022. 11. 22.)
    * Rocky Linux 8.6(2022. 11. 22.)
* イメージサポート終了
    * Rocky Linux 8.5(2022. 05. 17.)
* Debian 10.13 Buster(2022. 11. 22.)
    * イメージ更新
* Debian 11.5 Bullseye(2022. 11. 22.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS(2022. 11. 22.)
    * イメージ更新
* Ubuntu Server 20.04.5 LTS(2022. 11. 22.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS for NAT(2022. 11. 22.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS with NVIDIA(2022. 11. 22.)
    * イメージ更新
* Windows 2012 R2 STD(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018474-monthly-rollup-21182931-4a5f-4085-a37b-2e63ac3c8c0a
* Windows 2016 STD(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2019 STD(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018419-os-build-17763-3532-ca62cca7-b599-44c4-a2a6-347996662623
* Windows 2022 STD(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018421-os-build-20348-1129-115b1147-9568-4924-83b8-d27ab5b495be
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD with MS-SQL 2016 Standard(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018474-monthly-rollup-21182931-4a5f-4085-a37b-2e63ac3c8c0a
* Windows 2016 STD with MS-SQL 2019 Express(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2016 STD with MS-SQL 2017 Standard(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2016 STD with MS-SQL 2019 Standard(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2019 STD with MS-SQL 2019 Standard(2022. 11. 22.)
    * 日本語イメージのサポート終了
    * 22年10月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018419-os-build-17763-3532-ca62cca7-b599-44c4-a2a6-347996662623

<a id="november-29-2022-image-builder"></a>
### Image Builder { #november-29-2022-image-builder }
* アプリケーション追加
    * Redis
    * Apache Kafka

<a id="november-4-2022"></a>
## 2022. 11. 04. { #november-4-2022 }
<a id="november-4-2022-image"></a>
### Image { #november-4-2022-image }
* CentOS 7.8 with MariaDB 10.3.31(2022. 11. 04.)
    * イメージ更新

<a id="november-4-2022-image-builder"></a>
### Image Builder { #november-4-2022-image-builder }
* スクリプト修正
    * MariaDB

<a id="october-25-2022"></a>
## 2022. 10. 25. { #october-25-2022 }
<a id="october-25-2022-image"></a>
### Image { #october-25-2022-image }
* イメージサポート終了
    * CentOS 7.8 with MySQL 5.6.38(2021. 12. 21.)
    * CentOS 7.8 with MySQL 5.6.50(2021. 12. 21.)

<a id="september-27-2022"></a>
## 2022. 09. 27. { #september-27-2022 }
<a id="september-27-2022-image"></a>
### Image { #september-27-2022-image }
* 新規イメージ追加
    * Windows 2022 STD(2022. 09. 20.)

* PLOS-WFK-KS-v4.0.6.61.25
    * イメージ更新

<a id="july-26-2022"></a>
## 2022. 07. 26. { #july-26-2022 }
<a id="july-26-2022-instance"></a>
### Instance { #july-26-2022-instance }
* インスタンス作成でインスタンスタイプ（Instance、Ephemeral Storage Instance）の選択機能を追加しました。
* インスタンス管理でイメージタイプ（OS、Application、DBMS など）の検索機能を追加しました。

<a id="july-26-2022-image"></a>
### Image { #july-26-2022-image }
* Windows イメージの Administrator アカウント名を変更しても、パスワードの初期化が可能になるよう変更しました。

* Windows 2012 R2 STD（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows 2019 STD（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-us/topic/april-12-2022-kb5012647-os-build-17763-2803-9a10c5c9-e65f-4ae1-a9c4-2db9a8eca4fc
* Windows 2012 R2 STD with MS-SQL 2016 Standard（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD with MS-SQL 2016 Standard（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows 2016 STD with MS-SQL 2019 Express（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
    * SQL Server 累積アップデート 16 を反映: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896
* Windows 2016 STD with MS-SQL 2017 Standard（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows 2016 STD with MS-SQL 2019 Standard（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
    * SQL Server 累積アップデート 16 を反映: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896
* Windows 2019 STD with MS-SQL 2019 Standard（2022. 07. 19.）
    * 22年5月のセキュリティアップデートを反映: https://support.microsoft.com/en-us/topic/april-12-2022-kb5012647-os-build-17763-2803-9a10c5c9-e65f-4ae1-a9c4-2db9a8eca4fc
    * SQL Server 累積アップデート 16 を反映: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896

<a id="july-26-2022-system-monitoring"></a>
### System Monitoring { #july-26-2022-system-monitoring }
* 新機能追加: 月間メトリクスレポート
  * 月間メトリクスレポートを生成およびダウンロードできます。
  * 月単位で最大 6 か月分のメトリクスに関するレポートを生成できます。
  * メトリクス選択項目の `GENERAL` は `サーバーダッシュボード`で、`PROMQL` は `OpenMetrics ダッシュボード`で確認できるメトリクスです。
  * `月間メトリクスレポート`で各リクエストを確認でき、レポート生成後 1 か月間ダウンロードが可能です。

<a id="may-24-2022"></a>
## 2022. 05. 24. { #may-24-2022 }
<a id="may-24-2022-instance"></a>
### Instance { #may-24-2022-instance }
* インスタンスのスクリーンショット機能を追加しました。
* インスタンスの削除保護機能を追加しました。
* API でインスタンスを照会する際に、インスタンスの削除保護属性（NHN-EXT-ATTR:protect）が表示されるよう変更しました。
* 一括作成された複数のインスタンス名からハイフン（`-`）を削除しました。
    * 変更前: instance-1、instance-2、...
    * 変更後: instance1、instance2、...
* インスタンス作成時の OS イメージ選択 UI を改善しました。

<a id="may-24-2022-image"></a>
### Image { #may-24-2022-image }
* 新規イメージ追加
    * Rocky Linux 8.5（2022. 05. 17.）

<a id="march-29-2022"></a>
## 2022. 03. 29. { #march-29-2022 }
<a id="march-29-2022-image"></a>
### Image { #march-29-2022-image }
* 新規イメージ追加
    * Debian 11.2 Bullseye（2022. 03. 22.）

* イメージサポート終了
    * Debian 9.13 Stretch（2021. 12. 21.）

<a id="january-25-2022"></a>
## 2022. 01. 25. { #january-25-2022 }
<a id="january-25-2022-public-api"></a>
### Public API { #january-25-2022-public-api }
* イメージ照会 API で GPU Instance サービスのイメージも照会できるよう変更しました。
* イメージ照会 API にインフラサービス種別のフィルタリング用クエリパラメータを追加しました。

<a id="january-25-2022-image"></a>
### Image { #january-25-2022-image }
* 他のリージョンへのイメージ複製機能を追加しました。

<a id="january-25-2022-image-builder"></a>
### Image Builder { #january-25-2022-image-builder }
* アプリケーション追加
    * Slurm

<a id="december-28-2021"></a>
## 2021. 12. 28. { #december-28-2021 }

<a id="december-28-2021-image"></a>
### Image { #december-28-2021-image }
* インスタンス作成時に Prometheus 互換 exporter が自動的にインストールされないように変更しました。

* CentOS 7.8(2021. 12. 21.)
    * イメージ更新
* CentOS 7.8 for NAT(2021. 12. 21.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.6.38(2021. 12. 21.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.6.50(2021. 12. 21.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.7.20(2021. 12. 21.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.7.32(2021. 12. 21.)
    * イメージ更新
* CentOS 7.8 with MySQL 8.0.22(2021. 12. 21.)
    * イメージ更新
* Debian 9.13 Stretch(2021. 12. 21.)
    * イメージ更新
* Debian 10.11 Buster(2021. 12. 21.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS(2021. 12. 21.)
    * イメージ更新
* Ubuntu Server 20.04.3 LTS(2021. 12. 21.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS for NAT(2021. 12. 21.)
    * イメージ更新
* Ubuntu Server 18.04.6 LTS with NVIDIA(2021. 12. 21.)
    * イメージ更新
* Windows 2012 R2 STD(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007247-monthly-rollup-2c3b6017-82f4-4102-b1e2-36f366bf3520
* Windows 2016 STD(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows 2019 STD(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007206-os-build-17763-2300-c63b76fa-a9b4-4685-b17c-7d866bb50e48
* Windows Server 2012 R2 with SQL Server 2016 Standard(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007247-monthly-rollup-2c3b6017-82f4-4102-b1e2-36f366bf3520
* Windows Server 2016 with SQL Server 2016 Standard(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2019 Express(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2017 Standard(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2019 Standard(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2019 with SQL Server 2019 Standard(2021. 12. 21.)
    * 21年11月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007206-os-build-17763-2300-c63b76fa-a9b4-4685-b17c-7d866bb50e48

<a id="december-28-2021-image-builder"></a>
### Image Builder { #december-28-2021-image-builder }
* アプリケーション追加
    * Deep Learning Framework

<a id="december-28-2021-system-monitoring"></a>
### System Monitoring { #december-28-2021-system-monitoring }
* @Linux、@Windows デフォルトワークスペース追加機能の削除および作成済みワークスペースの削除
    * インスタンス作成時に自動的に追加されていた @Linux、@Windows ワークスペースは、自動追加されなくなりました。
    * 既存のインスタンスに自動作成されていた @Linux、@Windows ワークスペースはすべて削除されます。

<a id="november-23-2021"></a>
## 2021. 11. 23. { #november-23-2021 }
<a id="november-23-2021-image"></a>
### Image { #november-23-2021-image }
* GPU インスタンスを作成できる個人イメージの作成をサポートしました。

<a id="november-23-2021-image-builder"></a>
### Image Builder { #november-23-2021-image-builder }
* アプリケーション追加
    * JEUS
    * WebtoB
    * Apache Tomcat
    * Node.js
    * MySQL

<a id="october-26-2021"></a>
## 2021. 10. 26. { #october-26-2021 }
<a id="october-26-2021-image-builder"></a>
### Image Builder { #october-26-2021-image-builder }
* Image Builder サービス追加
    * OS イメージとアプリケーションインストールコンポーネント、ユーザースクリプトを組み合わせて個人イメージを作成
* アプリケーション追加
    * PostgreSQL
    * MariaDB
    * CUBRID

<a id="october-26-2021-system-monitoring"></a>
### System Monitoring { #october-26-2021-system-monitoring }

* OpenMetrics ダッシュボード → 照会
    * 照会期間を選択する際、最大1年前の日付までのみ選択できるように変更しました。
    * データなしまたはエラーに関する案内メッセージがチャートに表示されるように変更しました。
* OpenMetrics ダッシュボード → チャートの追加/編集
    * 指標を選択せずに **[追加]** ボタンを押すと案内メッセージが表示され、該当箇所が強調表示されるように変更しました。

<a id="september-14-2021"></a>
## 2021. 09. 14. { #september-14-2021 }
<a id="september-14-2021-system-monitoring"></a>
### System Monitoring { #september-14-2021-system-monitoring }
- 新規 API 追加: ワークスペース、収集対象の照会/追加/削除 API を追加しました。
- @Linux、@Windows デフォルトワークスペース追加
    - @Linux: インスタンスにインストールされた node exporter の指標を収集します。Linux OS 系インスタンス作成時に自動的に @Linux の収集対象として登録されます。
    - @Windows: インスタンスにインストールされた windows exporter の指標を収集します。Windows OS 系インスタンス作成時に自動的に @Windows の収集対象として登録されます。

<a id="july-27-2021"></a>
## 2021. 07. 27. { #july-27-2021 }

<a id="july-27-2021-instance"></a>
### Instance { #july-27-2021-instance }
* インスタンステンプレートを使用したインスタンス作成をサポートしました。

<a id="july-27-2021-instance-template"></a>
### Instance Template { #july-27-2021-instance-template }
* Instance Template サービス追加
    * 頻繁に使用するインスタンスの構成要素情報をテンプレート形式であらかじめ定義して保管
    * ユーザーが定義したテンプレートを Instance または Scaling Group の作成に使用

<a id="july-27-2021-auto-scale"></a>
### Auto Scale { #july-27-2021-auto-scale }
* Instance Template タブの削除
    * Instance Template サービスで作成したテンプレートを使用して Scaling Group を作成
* 自動復旧ポリシーのオプション選択肢を追加しました。

<a id="july-27-2021-system-monitoring"></a>
### System Monitoring { #july-27-2021-system-monitoring }

* バグ修正: アラームグループのサーバー、ユーザーグループを追加する際に「There are no entires.」を選択できた問題を修正しました。
* バグ修正: Advanced Monitoring レイアウトを素早く作成すると5個を超えて作成できた問題を修正しました。
* バグ修正: **Advanced Monitoring → ワークスペース → 収集対象**で、同一ポートで同じ名称の異なるインスタンスを収集対象として追加できなかった問題を修正しました。

<a id="june-29-2021"></a>
## 2021. 06. 29. { #june-29-2021 }

<a id="june-29-2021-image"></a>
### Image { #june-29-2021-image }

* Prometheus互換Exporter
    * Advanced Monitoring サポートのため、インスタンス作成時に該当ツールが自動的にインストールされます。

* CentOS 7.8(2021. 06. 22.)
    * イメージ更新
* CentOS 7.8 for NAT(2021. 06. 22.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.6.38(2021. 06. 22.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.6.50(2021. 06. 22.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.7.20(2021. 06. 22.)
    * イメージ更新
* CentOS 7.8 with MySQL 5.7.32(2021. 06. 22.)
    * イメージ更新
* CentOS 7.8 with MySQL 8.0.22(2021. 06. 22.)
    * イメージ更新
* Debian 9.13 Stretch(2021. 06. 22.)
    * イメージ更新
* Debian 10.9 Buster(2021. 06. 22.)
    * イメージ更新
* Ubuntu Server 18.04.5 LTS(2021. 06. 22.)
    * イメージ更新
* Ubuntu Server 18.04.5 LTS for NAT(2021. 06. 22.)
    * イメージ更新
* Ubuntu Server 18.04.5 LTS with NVIDIA(2021. 06. 22.)
    * イメージ更新
* Ubuntu Server 20.04.2 LTS(2021. 06. 22.)
    * イメージ更新
* Windows 2012 R2 STD(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD with MS-SQL 2016 Standard(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Express(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2017 Standard(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Standard(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD with MS-SQL 2019 Standard(2021. 06. 22.)
    * 2021 年 05 月セキュリティアップデート適用: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27

<a id="june-29-2021-system-monitoring"></a>
### System Monitoring { #june-29-2021-system-monitoring }

* OpenMetrics アラートグループ入力ガイド文言の改善
* サーバーダッシュボードのサーバー/エージェント状態ツールチップサイズの改善
* イベント状況画面で一部ドロップダウンメニューボタンが正常に表示されない現象を修正
* **Compute → Instance** で変更したインスタンス名がサーバーダッシュボードのサーバー一覧に反映されるよう修正
* ローディングバーを変更
* Prometheus 互換 API を追加 (ベータ)

<a id="april-27-2021"></a>
## 2021. 04. 27. { #april-27-2021 }

<a id="april-27-2021-image"></a>
### Image { #april-27-2021-image }

* 新規イメージ追加 (平村リージョン)
    * CentOS 7.8 for NAT(2021. 04. 22.)
    * Ubuntu Server 18.04.5 LTS for NAT(2021. 04. 22.)

* イメージサポート終了
    * Ubuntu Server 16.04.7 LTS(2020. 12. 22.)

<a id="february-23-2021"></a>
## 2021. 02. 23. { #february-23-2021 }

<a id="february-23-2021-image"></a>
### Image { #february-23-2021-image }

* 新規イメージ追加
    * CentOS 7.8 with MySQL 5.6.38(2021. 02. 23.)
    * CentOS 7.8 with MySQL 5.6.50(2021. 02. 23.)
    * CentOS 7.8 with MySQL 5.7.20(2021. 02. 23.)
    * CentOS 7.8 with MySQL 5.7.32(2021. 02. 23.)
    * CentOS 7.8 with MySQL 8.0.22(2021. 02. 23.)

* イメージサポート終了
    * CentOS 6.10(2020. 12. 22.)
    * CentOS 7.5(2020. 12. 22.)
    * CentOS Linux 6.10 with MySQL 5.6.38(2020. 12. 22.)
    * CentOS Linux 6.10 with MySQL 5.7.20(2020. 12. 22.)

* CentOS 7.8(2021. 02. 23.)
    * イメージ更新

* Linux セキュリティ脆弱性パッチ適用
    * Heap-based buffer overflow in Sudo(CVE-2021-3156)
    * 新規インスタンス作成時に適用

<a id="january-26-2021"></a>
## 2021. 01. 26. { #january-26-2021 }

<a id="january-26-2021-system-monitoring"></a>
### System Monitoring { #january-26-2021-system-monitoring }
* 新規機能追加: Advanced Monitoring (OpenMetrics)
    * OpenMetrics (Prometheus exposition format) メトリクスの収集、照会、アラート機能を提供

<a id="december-29-2020"></a>
## 2020. 12. 29. { #december-29-2020 }

<a id="december-29-2020-image"></a>
### Image { #december-29-2020-image }
* CentOS 6.10(2020. 12. 22.)
    * イメージを更新しました
* CentOS 7.5(2020. 12. 22.)
    * イメージを更新しました
* CentOS 7.8(2020. 12. 22.)
    * イメージを更新しました
* CentOS Linux 6.10 with MySQL 5.6.38(2020. 12. 22.)
    * イメージを更新しました
* CentOS Linux 6.10 with MySQL 5.7.20(2020. 12. 22.)
    * イメージを更新しました
* Debian 9.13 Stretch(2020. 12. 22.)
    * イメージを更新しました
* Debian 10.7 Buster(2020. 12. 22.)
    * イメージを更新しました
* Ubuntu Server 16.04.7 LTS(2020. 12. 22.)
    * イメージを更新しました
* Ubuntu Server 18.04.5 LTS(2020. 12. 22.)
    * イメージを更新しました
* Ubuntu Server 20.04.1 LTS(2020. 12. 22.)
    * イメージを更新しました
* Ubuntu Server 18.04.5 LTS with NVIDIA(2020. 12. 22.)
    * イメージを更新しました
* Windows 2012 R2 STD(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD with MS-SQL 2016 Standard(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Express(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2017 Standard(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Standard(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD with MS-SQL 2019 Standard(2020. 12. 22.)
    * 2020年11月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839

<a id="november-24-2020"></a>
## 2020. 11. 24. { #november-24-2020 }

<a id="november-24-2020-auto-scale"></a>
### Auto Scale { #november-24-2020-auto-scale }
* Deploy サービス連携機能を追加しました

<a id="august-25-2020"></a>
## 2020. 08. 25. { #august-25-2020 }

<a id="august-25-2020-instance"></a>
### Instance { #august-25-2020-instance }
* **[Windows インスタンス接続情報]** タブに **[パスワード初期化]** ボタンを追加しました
* Windows イメージ作成時に元のインスタンスのパスワードを初期化する機能を追加しました

<a id="august-25-2020-image"></a>
### Image { #august-25-2020-image }
* 新規イメージ追加
    * Cent OS 7.8(2020. 08. 18.)
    * Ubuntu 20.04 LTS(2020. 08. 18.)
    * Windows 2016 STD with MS-SQL 2019 Express(2020. 08. 18.)
    * Windows 2016 STD with MS-SQL 2017 Standard(2020. 08. 18.)
    * Windows 2016 STD with MS-SQL 2019 Standard(2020. 08. 18.)
    * Windows 2019 STD with MS-SQL 2019 Standard(2020. 08. 18.)

* CentOS 6.10(2020. 08. 18.)
    * イメージを更新しました
* CentOS 7.5(2020. 08. 18.)
    * イメージを更新しました
* CentOS Linux 6.10 with MySQL 5.6.38(2020. 08. 18.)
    * イメージを更新しました
* CentOS Linux 6.10 with MySQL 5.7.20(2020. 08. 18.)
    * イメージを更新しました
* Debian 9.9 Stretch(2020. 08. 18.)
    * イメージを更新しました
* Debian 10.5 Buster(2020. 08. 18.)
    * イメージを更新しました
* Ubuntu Server 16.04.6 LTS(2020. 08. 18.)
    * イメージを更新しました
* Ubuntu Server 18.04.4 LTS(2020. 08. 18.)
    * イメージを更新しました
* Ubuntu Server 18.04.4 LTS with NVIDIA(2020. 08. 18.)
    * イメージを更新しました
* Windows 2012 R2 STD(2020. 08. 18.)
    * イメージを更新しました
* Windows 2016 STD(2020. 08. 18.)
    * イメージを更新しました
* Windows 2019 STD(2020. 08. 18.)
    * イメージを更新しました
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020. 08. 18.)
    * イメージを更新しました
* Windows 2016 STD with MS-SQL 2016 Standard(2020. 08. 18.)
    * イメージを更新しました

* イメージサポート終了
    * Windows 2012 R2 STD with MS-SQL 2012 Standard(2020. 02. 18.)
    * Windows 2012 R2 STD with MS-SQL 2014 Standard(2020. 02. 18.)
    * Windows 2012 R2 STD with MS-SQL 2016 Express(2020. 02. 18.)

<a id="june-23-2020"></a>
## 2020. 06. 23. { #june-23-2020 }

<a id="june-23-2020-system-monitoring"></a>
### System Monitoring { #june-23-2020-system-monitoring }

* 意味がより明確に伝わるよう、チャートおよび凡例の名称を変更しました
* サブ項目のある収集項目に詳細チャートを表示する機能を追加しました

<a id="june-23-2020-instance"></a>
### Instance { #june-23-2020-instance }
* キーペアに登録された公開鍵を照会する機能を追加しました
* GPU インスタンスをコンソールから直接作成できるようサービスを公開しました
* **[インスタンス停止]** ダイアログボックスから **[削除]** ボタンを削除しました

<a id="may-26-2020"></a>
## 2020. 05. 26. { #may-26-2020 }

<a id="may-26-2020-instance"></a>
### Instance { #may-26-2020-instance }

* Public API v2 をリリースしました
    * Openstack 互換 API 仕様に変更しました
    * Terraform をサポートしました

<a id="may-26-2020-image"></a>
### Image { #may-26-2020-image }

* Public API v2 をリリースしました
    * Openstack 互換 API 仕様に変更しました

<a id="february-25-2020"></a>
## 2020. 02. 25. { #february-25-2020 }
<a id="february-25-2020-image"></a>
### Image { #february-25-2020-image }
* 個人イメージと共有されたイメージがイメージ一覧に一緒に表示されるよう変更しました
* 新規イメージ追加
    * Debian 10.2 Buster(2020. 02. 18.)

* CentOS 6.10(2020. 02. 18.)
    * イメージを更新しました
* CentOS 7.5(2020. 02. 18.)
    * イメージを更新しました
* CentOS Linux 6.10 with MySQL 5.6.38(2020. 02. 18.)
    * イメージを更新しました
* CentOS Linux 6.10 with MySQL 5.7.20(2020. 02. 18.)
    * イメージを更新しました
* Debian 9.9 Stretch(2020. 02. 18.)
    * イメージを更新しました
* Ubuntu Server 16.04.2 LTS(2020. 02. 18.)
    * イメージを更新しました
* Ubuntu Server 18.04.2 LTS(2020. 02. 18.)
    * イメージを更新しました
* Windows 2012 R2 STD(2020. 02.18)
    * 2019年12月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2012 Standard(2020. 02. 18.)
    * 2019年12月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2014 Standard(2020. 02. 18.)
    * 2019年12月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Express(2020. 02. 18.)
    * 2019年12月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020. 02. 18.)
    * 2019年12月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2016 STD(2020. 02. 18.)
    * 2019年12月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689
* Windows 2016 R2 STD with MS-SQL 2016 Standard(2020. 02. 18.)
    * 2019年12月のセキュリティアップデートを反映: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689
* Windows 2019 STD(2020. 02. 18.)
    * イメージを更新しました

* イメージサポート終了
    * Debian 8.11 Jessie(2019. 07. 23.)

<a id="february-25-2020-system-monitoring"></a>
### System Monitoring { #february-25-2020-system-monitoring }
* イベント状況ページを改善しました
    * リージョンごとにイベントを照会できるよう改善しました
    * イベント検索フィルターのステータス項目に「All」オプションを追加しました
    * ユーザーが直接イベントを終了できる **[強制終了]** ボタンを追加しました
* Agent を改善しました
    * System Monitoring サーバーとの通信経路を最適化しました
        * インターネットゲートウェイ、セキュリティグループの設定に関わらず指標の収集が可能になりました
    * CPU・メモリ使用量の収集精度を改善しました

<a id="january-31-2020"></a>
## 2020. 01. 31. { #january-31-2020 }
<a id="january-31-2020-image"></a>
### Image { #january-31-2020-image }
* 新規イメージ追加
    * Windows 2019 STD(2020. 01. 31.)

<a id="january-21-2020"></a>
## 2020. 01. 21. { #january-21-2020 }
<a id="january-21-2020-system-monitoring"></a>
### System Monitoring { #january-21-2020-system-monitoring }
* イベント照会ページを追加しました
    * 設定した **[監視設定]** によって発生したイベントを照会する機能を提供します
* サーバーダッシュボードの **[サーバー一覧]** 機能を改善しました
    * **Compute → Instance** のすべてのインスタンスを照会できるよう改善しました
    * インスタンスの状態が正確に表示されるよう改善しました
* 通知グループの **[サーバーおよびユーザーグループ連携]** 機能を改善しました
    * サーバーおよびユーザーグループを選択して **[保存]** ボタンを押すことで変更内容が保存されるよう変更しました

<a id="december-17-2019"></a>
## 2019. 12. 17. { #december-17-2019 }
<a id="december-17-2019-auto-scale"></a>
### Auto Scale { #december-17-2019-auto-scale }
* インスタンステンプレートの一覧および詳細情報で、作成時に入力したすべての情報を確認できるよう修正しました
    * 一覧テーブル: Availability Zone
    * 詳細情報: 設定したすべてのネットワーク情報、ユーザースクリプトの内容

<a id="november-26-2019"></a>
## 2019. 11. 26. { #november-26-2019 }
<a id="november-26-2019-auto-scale"></a>
### Auto Scale { #november-26-2019-auto-scale }
* Auto Scaling 自動復旧
    * Scaling Group に属する個々のインスタンスにネットワーク切断などの障害が発生した場合、自動的に新しいインスタンスを作成して障害が発生したインスタンスを置き換える機能を追加しました

<a id="november-26-2019-instance"></a>
### Instance { #november-26-2019-instance }
* インスタンス一覧で IP を使用してインスタンスを検索する際、一部の特殊文字を入力するとエラーが発生する問題を修正しました

<a id="november-26-2019-system-monitoring"></a>
### System Monitoring { #november-26-2019-system-monitoring }
* サーバーダッシュボードのインスタンス検索機能を改善しました: 大文字と小文字を区別しないよう修正しました


<a id="october-29-2019"></a>
## 2019. 10. 29. { #october-29-2019 }
<a id="october-29-2019-image"></a>
### Image { #october-29-2019-image }
* PLOS-WFK-KS-v2.0.60.0.14(2019. 10. 22.)
    * WF-KS ページの Storage サイズ表示の不具合を修正しました

* Windows 2012 R2 STD(2019. 10. 22.)
    * 言語別イメージを提供(KO、EN、JP)
* Windows 2016 STD(2019. 10. 22.)
    * 言語別イメージを提供(KO、EN、JP)
* Windows 2012 R2 STD with MS-SQL 2012 Standard(2019. 10. 22.)
    * 言語別イメージを提供(KO、EN、JP)
* Windows 2012 R2 STD with MS-SQL 2014 Standard(2019. 10. 22.)
    * 言語別イメージを提供(KO、EN、JP)
* Windows 2012 R2 STD with MS-SQL 2016 Express(2019. 10. 22.)
    * 言語別イメージを提供(KO、EN、JP)
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2019. 10. 22.)
    * 言語別イメージを提供(KO、EN、JP)
* Windows 2016 R2 STD with MS-SQL 2016 Standard(2019. 10. 22.)
    * 言語別イメージを提供(KO、EN、JP)

<a id="october-29-2019-system-monitoring"></a>
### System Monitoring { #october-29-2019-system-monitoring }
* ユーザーインタラクション UI を改善しました
    * ユーザーグループ、監視グループ、監視設定などのモニタリング情報を照会・追加・修正・削除する際にローディングバーが表示されるよう修正しました
    * 操作中に不要なボタンが無効化されるよう修正しました
* 海外リージョンのバグを修正しました
    * 日本・米国リージョンで監視設定を変更したサーバーの指標収集が一時的に停止していた問題を修正しました
    * 米国リージョンでユーザーグループと監視グループの追加・修正日付が誤って表示されていた問題を修正しました

<a id="vpc"></a>
### VPC { #vpc }
* Default VPC 削除機能を追加しました
    * ユーザーが Default VPC を削除できるよう修正しました

<a id="september-24-2019"></a>
## 2019. 09. 24. { #september-24-2019 }
<a id="september-24-2019-system-monitoring"></a>
### System Monitoring { #september-24-2019-system-monitoring }
* Web コンソールの英語メッセージに対応しました
* Internet Explorer 11 ブラウザ環境でサーバーダッシュボードのレイアウト選択に失敗していた現象を修正しました

<a id="august-27-2019"></a>
## 2019. 08. 27. { #august-27-2019 }
<a id="august-27-2019-image"></a>
### Image { #august-27-2019-image }
* イメージ管理画面から公開イメージタブを削除しました

* Windows 2012 R2 STD(2019. 08. 27.)
    * 2019年7月10日のセキュリティアップデートを反映: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2012 Standard(2019. 08. 27.)
    * 2019年7月10日のセキュリティアップデートを反映: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2014 Standard(2019. 08. 27.)
    * 2019年7月10日のセキュリティアップデートを反映: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2016 Express(2019. 08. 27.)
    * 2019年7月10日のセキュリティアップデートを反映: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2019. 08. 27.)
    * 2019年7月10日のセキュリティアップデートを反映: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448

* Windows 2016 STD(2019. 08. 27.)
    * 2019年7月10日のセキュリティアップデートを反映: https://support.microsoft.com/en-us/help/4507460/windows-10-update-kb4507460
* Windows 2016 R2 STD with MS-SQL 2016 Standard(2019. 08. 27.)
    * 2019年7月10日のセキュリティアップデートを反映: https://support.microsoft.com/en-us/help/4507460/windows-10-update-kb4507460

* OS イメージサポート終了
    * Windows 2012 R2 STD with MS-SQL 2008 R2 Standard

<a id="august-27-2019-system-monitoring"></a>
### System Monitoring { #august-27-2019-system-monitoring }
* サーバーダッシュボードのチャート照会パフォーマンスを改善しました
* Internet Explorer 11 ブラウザ環境の UI を改善しました

<a id="july-23-2019"></a>
## 2019. 07. 23. { #july-23-2019 }
<a id="july-23-2019-system-monitoring"></a>
### System Monitoring { #july-23-2019-system-monitoring }
* System Monitoring サービスを追加しました
    * 作成された仮想サーバーのシステム指標チャートを提供します
    * 各システム指標チャートを任意のレイアウトに構成できます
    * 指標が特定のしきい値に達した場合、指定したユーザーグループに通知を送信するよう設定できます

<a id="june-25-2019"></a>
## 2019. 06. 25. { #june-25-2019 }
<a id="june-25-2019-instance"></a>
### Instance { #june-25-2019-instance }
* インスタンスが起動中でもイメージを作成できるよう修正しました

<a id="may-28-2019"></a>
## 2019. 05. 28. { #may-28-2019 }
<a id="may-28-2019-auto-scale"></a>
### Auto Scale { #may-28-2019-auto-scale }
* Scaling Group の使用量を確認できる統計グラフを追加しました。

<a id="may-28-2019-image"></a>
### Image { #may-28-2019-image }
* CentOS 6.10(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
* CentOS 7.5(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
* Debian 8.11 Jessie(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
* Debian 9.9 Stretch(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
* Ubuntu Server 16.04.6 LTS(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * カーネルアップデート: 4.4.0-142.168
* Ubuntu Server 18.04.2 LTS(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。

* Debian 9.9 Stretch(2019. 05. 28.)
    * カーネルアップデート: 4.9.168-1

* Windows 2012 R2 STD(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * 2019年5月14日 セキュリティアップデート: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2008 R2 Standard(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * 2019年5月14日 セキュリティアップデート: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2012 Standard(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * 2019年5月14日 セキュリティアップデート: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2014 Standard(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * 2019年5月14日 セキュリティアップデート: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2016 Express(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * 2019年5月14日 セキュリティアップデート: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * 2019年5月14日 セキュリティアップデート: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151

* Windows 2016 STD(2019. 05. 28.)
    * リージョンに応じた timezone の変更を適用しました。
    * 2019年5月14日 セキュリティアップデート: https://support.microsoft.com/ko-kr/help/4498947/windows-10-update-kb4498947

* 新規イメージ追加
    * Windows 2016 STD with MS-SQL 2016 Standard(2019. 05. 28.)


<a id="may-14-2019"></a>
## 2019. 05. 14. { #may-14-2019 }
<a id="may-14-2019-image"></a>
### Image { #may-14-2019-image }
* CentOS 6.10 with MySQL 5.6.38(2019. 05. 14.)
    * イメージを更新しました。
* CentOS 6.10 with MySQL 5.7.20(2019. 05. 14.)
    * イメージを更新しました。

* イメージサポート終了
    * CentOS 6.5
    * CentOS 7.1
    * Ubuntu 14.04
    * Windows 2008 R2 STD


<a id="april-25-2019"></a>
## 2019. 04. 25. { #april-25-2019 }
<a id="april-25-2019-auto-scale"></a>
### Auto Scale { #april-25-2019-auto-scale }
* 予約タスク作成時のタイムゾーン設定機能を追加しました。

<a id="april-25-2019-image"></a>
### Image { #april-25-2019-image }
* CentOS 6.5(2019. 04. 25.)
    * yum update 時に発生するエラー現象を改善しました。
* CentOS 6.10(2019. 04. 25.)
    * yum update 時に発生するエラー現象を改善しました。
* CentOS 7.1(2019. 04. 25.)
    * yum update 時に発生するエラー現象を改善しました。
    * 時刻同期デーモンを変更しました (ntpd)。
* CentOS 7.5(2019. 04. 25.)
    * yum update 時に発生するエラー現象を改善しました。
    * 時刻同期デーモンを変更しました (ntpd)。

* Windows 2008 R2 STD(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。
* Windows 2012 R2 STD(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。
* Windows 2016 STD(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。
* Windows 2012 R2 STD with MS-SQL 2008 R2 Standard(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。
* Windows 2012 R2 STD with MS-SQL 2012 Standard(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。
* Windows 2012 R2 STD with MS-SQL 2014 Standard(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。
* Windows 2012 R2 STD with MS-SQL 2016 Express(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2019. 04. 25.)
    * Windows Bootstrap プロセスの機能を改善しました。


<a id="march-26-2019"></a>
## 2019. 03. 26. { #march-26-2019 }
<a id="march-26-2019-image"></a>
### Image { #march-26-2019-image }
* CentOS 6.5(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* CentOS 6.10(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* CentOS 7.1(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* CentOS 7.5(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* CentOS 6.5 with MySQL 5.6.38(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* CentOS 6.5 with MySQL 5.7.20(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* Ubuntu Server 14.04.5 LTS(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* Ubuntu Server 16.04.5 LTS(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* Ubuntu Server 18.04.2 LTS(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* Debian 8.11 Jessie(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
* Debian 9.8 Stretch(2019. 03. 26.)
    * Bootstrap プロセスの機能を改善しました。
    * カーネルアップデート: 4.9.144-3


<a id="february-26-2019"></a>
## 2019. 02. 26. { #february-26-2019 }
<a id="february-26-2019-image"></a>
### Image { #february-26-2019-image }
* Ubuntu Server 18.04.2 LTS(2019. 02. 26.)
    * カーネルアップデート: 4.15.0-45
    * ネットワークインターフェースまたは Subnet の追加・削除時に間欠的に発生する通信エラーをさらに修正しました。


<a id="january-29-2019"></a>
## 2019. 01. 29. { #january-29-2019 }
<a id="january-29-2019-public-api"></a>
### Public API { #january-29-2019-public-api }
* Instance 作成時に Subnet を指定できるように修正しました。
* Image 照会 API にページネーション用のクエリパラメータを追加しました。
* Image 削除 API を追加しました。


<a id="december-27-2018"></a>
## 2018. 12. 27. { #december-27-2018 }

<a id="december-27-2018-image"></a>
### Image { #december-27-2018-image }
* Ubuntu Server 14.04.5 LTS(2018. 12. 27.)
    * shell 上でオートコンプリート (tab) 機能使用時に LC_CTYPE 関連の警告メッセージが発生する現象を修正しました。
        * デフォルト設定を "en_US.UTF-8" に変更しました。
        * /etc/default/locale を修正しました。
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 16.04.5 LTS(2018. 12. 27.)
    * shell 上でオートコンプリート (tab) 機能使用時に LC_CTYPE 関連の警告メッセージが発生する現象を修正しました。
        * デフォルト設定を "en_US.UTF-8" に変更しました。
        * /etc/default/locale を修正しました。
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 18.04.2 LTS(2018. 12. 27.)
    * shell 上でオートコンプリート (tab) 機能使用時に LC_CTYPE 関連の警告メッセージが発生する現象を修正しました。
        * デフォルト設定を "en_US.UTF-8" に変更しました。
        * /etc/default/locale を修正しました。
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Debian 8.11 Jessie(2019. 03. 26.)
    * shell 上でオートコンプリート (tab) 機能使用時に LC_CTYPE 関連の警告メッセージが発生する現象を修正しました。
        * デフォルト設定を "en_US.UTF-8" に変更しました。
        * /etc/default/locale を修正しました。
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Debian 9.8 Stretch(2019. 03. 26.)
    * shell 上でオートコンプリート (tab) 機能使用時に LC_CTYPE 関連の警告メッセージが発生する現象を修正しました。
        * デフォルト設定を "en_US.UTF-8" に変更しました。
        * /etc/default/locale を修正しました。
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"


<a id="december-11-2018"></a>
## 2018. 12. 11. { #december-11-2018 }
<a id="december-11-2018-image"></a>
### Image { #december-11-2018-image }
* ネットワークインターフェースまたは Subnet の追加・削除時に間欠的に発生する通信エラーを修正しました。
* Debian 8.11 Jessie(2018. 12. 11.)
    * カーネルアップデート: 3.16-0-6
* Debian 9.6 Stretch(2018. 12. 11.)
    * カーネルアップデート: 4.9.0-8

* CentOS 6.5(2018. 12. 11.)
    * カーネルアップデート: 2.6.32-754
* CentOS 6.10(2018. 12. 11.)
    * カーネルアップデート: 2.6.32-754
* CentOS 7.5(2018. 12. 11.)
    * カーネルアップデート: 3.10.0-862
* CentOS 7.1(2018. 12. 11.)
    * カーネルアップデート: 3.10.0-693

* Ubuntu Server 18.04.1 LTS(2018. 12. 11.)
    * カーネルアップデート: 4.15.0-29
* Ubuntu Server 16.04.5 LTS(2018. 12. 11.)
    * カーネルアップデート: 4.4.0-131
* Ubuntu Server 14.04.5 LTS(2018. 12. 11.)
    * カーネルアップデート: 4.4.0-31


<a id="november-13-2018"></a>
## 2018. 11. 13. { #november-13-2018 }
<a id="november-13-2018-image"></a>
### Image { #november-13-2018-image }
* CentOS 6.5(2018. 11. 13.)
    * カーネルアップデート: 2.6.32-754.6.3
    * Yum repository の対象を最新の repository に変更しました。
* CentOS 7.1(2018. 11. 13.)
    * カーネルアップデート: 3.10.0-693.21.1
    * Yum repository の対象を最新の repository に変更しました。

<a id="october-23-2018"></a>
## 2018. 10. 23. { #october-23-2018 }
<a id="october-23-2018-image"></a>
### Image { #october-23-2018-image }
* CentOS 7.5(2018. 10. 23.)、CentOS 7.1(2018. 10. 23.)、CentOS 6.10(2018. 10. 23.)、CentOS 6.5(2018. 10. 23.)
    * パスワード複雑度の設定: 数字・英字・特殊文字の組み合わせ + 8文字以上)(/etc/pam.d/common-password を修正)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 設定の変更(/etc/ssh/sshd_config を修正)
        * PermitRootLogin no                # root 接続の無効化
        * PasswordAuthentication no         # パスワード認証の無効化
    * 脆弱性対策のカーネルパラメータ変更(/etc/sysctl.conf を修正)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 攻撃のブロック
        * net.ipv4.conf.all.accept_source_route = 0 # ソースルーティングのブロックによる ip スプーフィング防止
        * net.ipv4.conf.all.log_martians = 1 # スプーフィングのログ記録
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 攻撃の防御
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip または tcp ヘッダーが破損した bad icmp パケットの無視
        * net.ipv4.tcp_syncookies=1 # syn フラッディング攻撃防御のための syn cookies の使用
    * ターミナルアクセス制限(/etc/securetty を修正)
        * console、vc/1、vc/2、tty1、tty2、ttyS0 以外からのアクセス不可
    * ターミナルから 120 分以上ユーザー入力がない場合にセッションを終了(/etc/profile を修正)
        * TMOUT=7200
    * その他の設定は CentOS Upstream を維持します
    * アクセスセキュリティ強化のための root アカウント接続制限
        * 変更前: root アカウントによる ssh 接続を許可
        * 変更後: 一般ユーザーアカウント「centos」で接続後に切り替え
    * インスタンス作成時に swap partition を作成しません
    * /etc/hosts ファイルのユーザー追加設定を維持します

* Ubuntu Server 16.04.5 LTS(2018. 10. 23.)
    * パスワード複雑度の設定: 数字・英字・特殊文字の組み合わせ + 8文字以上)(/etc/pam.d/common-password を修正)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 設定の変更(/etc/ssh/sshd_config を修正)
        * PermitRootLogin no                # root 接続の無効化
        * PasswordAuthentication no         # パスワード認証の無効化
    * 脆弱性対策のカーネルパラメータ変更(/etc/sysctl.conf を修正)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 攻撃のブロック
        * net.ipv4.conf.all.accept_source_route = 0 # ソースルーティングのブロックによる ip スプーフィング防止
        * net.ipv4.conf.all.log_martians = 1 # スプーフィングのログ記録
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 攻撃の防御
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip または tcp ヘッダーが破損した bad icmp パケットの無視
        * net.ipv4.tcp_syncookies=1 # syn フラッディング攻撃防御のための syn cookies の使用
    * ターミナルアクセス制限(/etc/securetty を修正)
        * console、vc/1、vc/2、tty1、tty2、ttyS0 以外からのアクセス不可
    * ターミナルから 120 分以上ユーザー入力がない場合にセッションを終了(/etc/profile を修正)
        * TMOUT=7200
    * その他の設定は Ubuntu Server 16.04 LTS Upstream を維持します
    * インスタンス作成時に swap partition を作成しません
    * /etc/hosts ファイルのユーザー追加設定を維持します

* Debian 9.5 Stretch(2018. 10. 23.)、Debian 8.11 Jessie(2018. 10. 23.)
    * パスワード複雑度の設定: 数字・英字・特殊文字の組み合わせ + 8文字以上)(/etc/pam.d/common-password を修正)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 設定の変更(/etc/ssh/sshd_config を修正)
        * PermitRootLogin no                # root 接続の無効化
        * PasswordAuthentication no         # パスワード認証の無効化
    * 脆弱性対策のカーネルパラメータ変更(/etc/sysctl.conf を修正)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 攻撃のブロック
        * net.ipv4.conf.all.accept_source_route = 0 # ソースルーティングのブロックによる ip スプーフィング防止
        * net.ipv4.conf.all.log_martians = 1 # スプーフィングのログ記録
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 攻撃の防御
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip または tcp ヘッダーが破損した bad icmp パケットの無視
        * net.ipv4.tcp_syncookies=1 # syn フラッディング攻撃防御のための syn cookies の使用
    * ターミナルアクセス制限(/etc/securetty を修正)
        * console、vc/1、vc/2、tty1、tty2、ttyS0 以外からのアクセス不可
    * ターミナルから 120 分以上ユーザー入力がない場合にセッションを終了(/etc/profile を修正)
        * TMOUT=7200
    * その他の設定は Debian 9 Upstream を維持します
    * インスタンス作成時に swap partition を作成しません
    * /etc/hosts ファイルのユーザー追加設定を維持します


<a id="september-20-2018"></a>
## 2018. 09. 20. { #september-20-2018 }
<a id="september-20-2018-instance"></a>
### Instance { #september-20-2018-instance }
* Instance 管理画面の UX/UI 改善
    * インスタンス名の検索機能を追加
    * Availability Zone、インスタンスステータスのフィルターを追加
* Instance 作成画面の機能および UX/UI 改善
    * フローティング IP 使用有無の選択機能を追加
    * セキュリティグループの作成およびポリシー確認機能を追加
    * 追加ブロックストレージの接続機能を追加
    * ユーザースクリプトの登録機能を追加

<a id="september-20-2018-image"></a>
### Image { #september-20-2018-image }
* ユーザースクリプト機能が正常に適用されない問題を修正

* Ubuntu Server 18.04.1 LTS(2018. 09. 20.)
    * Kernel 4.15.0-29: meltdown/spectre variant 1、2、3(CVE-2017-5753、5715、5754) パッチ(retpoline)
    * パスワード複雑度の設定: 数字・英字・特殊文字の組み合わせ + 8文字以上)(/etc/pam.d/common-password を修正)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 設定の変更(/etc/ssh/sshd_config を修正)
        * PermitRootLogin no                # root 接続の無効化
        * PasswordAuthentication no         # パスワード認証の無効化
    * 脆弱性対策のカーネルパラメータ変更(/etc/sysctl.conf を修正)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 攻撃のブロック
        * net.ipv4.conf.all.accept_source_route = 0 # ソースルーティングのブロックによる ip スプーフィング防止
        * net.ipv4.conf.all.log_martians = 1 # スプーフィングのログ記録
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 攻撃の防御
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip または tcp ヘッダーが破損した bad icmp パケットの無視
        * net.ipv4.tcp_syncookies=1 # syn フラッディング攻撃防御のための syn cookies の使用
    * ターミナルアクセス制限(/etc/securetty を修正)
        * console、vc/1、vc/2、tty1、tty2、ttyS0 以外からのアクセス不可
    * ターミナルから 120 分以上ユーザー入力がない場合にセッションを終了(/etc/profile を修正)
        * TMOUT=7200
    * インスタンス作成時に swap partition を作成しません(必要に応じてユーザーが別途作成してください)
    * その他の設定は Ubuntu Server 18.04 LTS upstream を維持します

* 新規イメージ追加
    * Ubuntu Linux 14.04.5(2018. 09. 20.) を追加


<a id="august-9-2018"></a>
## 2018. 08. 09. { #august-9-2018 }
<a id="august-9-2018-image"></a>
### Image { #august-9-2018-image }
* Windows 2012 R2 STD(2018. 08. 09.)
    * 韓国語使用時、ユーザーが韓国語言語パックをインストール（デフォルトは英語バージョンを提供）
    * 2018年7月10日 セキュリティアップデート: https://support.microsoft.com/en-us/help/4338815/windows-81-update-kb4338815
    * アカウント管理
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * サービス管理
        * NTP 設定: 1.pool.ntp.org, time,windows.com
        * NTP 同期周期: 256秒
    * システム管理
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled
        * Autologin 機能制限: AutoAdminLogon の値を 0 に設定

* Windows 2016 STD(2018. 08. 09.)
    * 2018年7月24日 セキュリティアップデート: https://support.microsoft.com/en-us/help/4338822/windows-10-update-kb4338822
    * アカウント管理
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * サービス管理
        * NTP 設定: 1.pool.ntp.org, time,windows.com
        * NTP 同期周期: 256秒
    * システム管理
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled

* Debian 9.4.0(2018. 08. 09.)
    * Kernel 4.9 アップデート: meltdown/spectre variant 1,2,3(CVE-2017-5753, 5715, 5754) パッチ(retpoline)
    * パスワード複雑度設定（数字・英字・特殊文字の組み合わせ + 8文字以上）: /etc/pam.d/common-password に以下の行を追加
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * 不要なアカウント/グループの削除
        * user: lp, sync, uucp, games
        * group: dip
    * 脆弱性対策のためのカーネルパラメータ変更(sysctl)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp リダイレクト攻撃のブロック
        * net.ipv4\.conf.all.accept_source_route = 0 # ソースルーティングブロックによる IP スプーフィング防止
        * net.ipv4.conf.all.log_martians = 1 # スプーフィングのログ記録
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf DoS 攻撃への防御
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # IP または TCP ヘッダーが破損した不正 ICMP パケットを無視
        * net.ipv4.tcp_syncookies=1 # SYN フラッディング攻撃対策のための SYN cookies の使用
    * SSH 設定変更
        * PermitRootLogin 無効化
        * /etc/ssh/sshd_config に immutable 属性を付与
    * setuid/setgid の除去
        * /usr/bin/chag
        * /usr/bin/gpasswd
        * /usr/bin/wall
        * /usr/bin/chfn
        * /usr/bin/chsh
        * /usr/bin/newgrp
        * /bin/mount
        * /bin/umount
        * /sbin/unix_chkpwd
    * パーミッション設定
        * /etc/passwd 644
        * /etc/hosts 644
        * /etc/rsyslog.conf 644
        * /etc/services 644
        * /etc/group 644
        * /etc/shadow 400
        * /etc/gshadow 400
        * /etc/login.defs 400
    * ターミナルアクセス制限: /etc/securetty の修正
    * profile の追加(/etc/profile)
        * TMOUT=7200      # ターミナルからのユーザー入力がない場合にセッションを終了
        * HISTSIZE=500       # history リストに保存されるコマンド数の制限
        * HISTFILESIZE=0     # history ファイルに保存されるコマンドなし
    * システムログイン前バナー設定の削除
        * /etc/issue、/etc/issue.net を削除


<a id="july-16-2018"></a>
## 2018. 07. 16. { #july-16-2018 }
<a id="july-16-2018-image"></a>
### Image { #july-16-2018-image }
* Windows 2012 R2 STD(2018. 07. 16.)
    * Auto Scale 機能でワクチンが含まれるインスタンスを作成する際に発生するエラーを修正
    * CPU 設定変更(CPU ソケットの最大数を 4 個に変更)
    * ネットワークインターフェース速度が 10G と表示されるよう修正

* Windows 2008 R2 STD(2018. 07. 16.)
    * 2018 年 6 月 12 日付けセキュリティアップデート: https://support.microsoft.com/ko-kr/help/4284826
    * アカウント管理
        * Guest アカウントの使用制限: Guest アカウントを無効に変更
        * 最終ユーザーのログイン名表示: 表示しないに設定
        * セッションがロックされている場合のユーザー情報表示: ユーザー名のみ表示に設定
        * パスワード有効期限前の変更通知: 変更通知を 14 日に設定
        * 一般ユーザーによるシステムシャットダウンの制限: シャットダウンポリシーを Administrator に設定
    * サービス管理
        * NTP 設定: 1.pool.ntp.org、time.windows.com
        * NTP 同期間隔: 256 秒
    * システム管理
        * SAM アカウントと共有の匿名列挙を許可しない: SAM アカウント関連の匿名列挙を許可しない項目を有効化
        * ログオンせずにシステムのシャットダウンを許可する制限: ログオンせずにシャットダウンを許可するポリシーを無効に設定
        * Autologin 機能の制限: AutoAdminLogon の値を 0 に設定

* Ubuntu 16.04.4 LTS(2018. 07. 16.)
    * Kernel 4.4.0-130: meltdown/spectre variant 1、2、3 (CVE-2017-5753、5715、5754) パッチ (retpoline)
    * パスワード複雑度の設定(数字・英字・特殊文字の組み合わせ + 8 文字以上): /etc/pam.d/common-password に以下の行を追加
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * 不要なアカウント/グループの削除
        * user: lp、sync、uucp、games
        * group: dip
    * 脆弱性対策のカーネルパラメータ変更 (sysctl)
        * net.ipv4.conf.all.accept_redirects = 0 # ICMP リダイレクト攻撃を遮断
        * net.ipv4\.conf.all.accept_source_route = 0 # ソースルーティング遮断による IP スプーフィング防止
        * net.ipv4.conf.all.log_martians = 1 # スプーフィングのログ記録
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # Smurf DoS 攻撃の防御
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # IP または TCP ヘッダーが破損した不正な ICMP パケットを無視
        * net.ipv4.tcp_syncookies=1 # SYN フラッディング攻撃防御のための SYN Cookie を使用
    * SSH 設定変更
        * PermitRootLogin を無効化
        * /etc/ssh/sshd_config に immutable 属性を付与
    * setuid/setgid の削除
        * /usr/bin/chag
        * /usr/bin/gpasswd
        * /usr/bin/wall
        * /usr/bin/chfn
        * /usr/bin/chsh
        * /usr/bin/newgrp
        * /bin/mount
        * /bin/umount
        * /sbin/unix_chkpwd
    * パーミッション設定
        * /etc/passwd 644
        * /etc/hosts 644
        * /etc/rsyslog.conf 644
        * /etc/services 644
        * /etc/group 644
        * /etc/shadow 400
        * /etc/gshadow 400
        * /etc/login.defs 400
    * ターミナルアクセス制限: /etc/securetty を修正
    * profile の追加 (/etc/profile)
        * TMOUT=7200      # ターミナルからのユーザー入力がない場合にセッションを終了
        * HISTSIZE=500       # history リストに保存されるコマンド数を制限
        * HISTFILESIZE=0     # history ファイルに保存されるコマンドをなしに設定
    * システムログイン前のバナー設定を削除
        * /etc/issue、/etc/issue.net を削除

<a id="may-29-2018"></a>
## 2018. 05. 29. { #may-29-2018 }
<a id="may-29-2018-auto-scale"></a>
### Auto Scale { #may-29-2018-auto-scale }
* 繰り返し予約タスク (cron expression ベース) に関するエラーを修正
    * 繰り返し予約タスクの実行タイミングが UTC を基準に動作するエラーを修正
    * 繰り返し予約タスクの初回実行が cron expression に従わず、予約タスク作成時に設定した「開始時刻」に実行されるエラーを修正

<a id="may-29-2018-instance"></a>
### Instance { #may-29-2018-instance }
* インスタンス作成時にボリュームタイプを設定する機能を追加

<a id="april-24-2018"></a>
### 2018.04.24 { #april-24-2018 }
<a id="may-29-2018-instance-2"></a>
### Instance { #may-29-2018-instance-2 }
* Windows インスタンスのログ表示機能を削除

<a id="march-22-2018"></a>
## 2018. 03. 22. { #march-22-2018 }
<a id="march-22-2018-auto-scale"></a>
### Auto Scale { #march-22-2018-auto-scale }
* Auto Scale サービスを追加
    * ユーザーが作成した Instance Template をもとに Scaling Group を作成
    * Scaling Group に属するインスタンスの数を、インスタンスの状態または予約タスクを通じて動的に管理
    * 詳細についてはガイドドキュメントを参照してください

<a id="february-22-2018"></a>
## 2018. 02. 22. { #february-22-2018 }
<a id="february-22-2018-instance"></a>
### Instance { #february-22-2018-instance }
* VPC 機能の追加に伴い、インスタンス作成時にサブネットを指定するよう変更

<a id="february-22-2018-image"></a>
### Image { #february-22-2018-image }
* Windows 2012 R2 STD(2018. 02. 22.)
    * Windows タイムゾーン設定の変更
        * 同期間隔の変更: [変更前] 604800 秒 (7 日) → [変更後] 256 秒
        * タイムゾーンピアドメインの変更: [変更前] 1.kr.pool.ntp.org、1.pool.ntp.org → [変更後] 1.pool.ntp.org、time.windows.com
    * 2018 年 2 月 13 日付けセキュリティアップデート: https://support.microsoft.com/ko-kr/help/4074594/windows-81-update-kb-4074594

* Ubuntu Linux 14.04.5(2018. 02. 22.)
    * 脆弱性パッチのための関連カーネルアップデート
        * Linux Kernel Version: 3.13.0-141
        * Variant 1(CVE-2017-5753) - patched
        * Variant 3(CVE-2017-5754) - patched

* Debian Linux 8.2.0(2018. 02. 22.)
    * インスタンス作成時に指定した名前でホスト名が適用されるよう修正
    * 脆弱性パッチのための関連カーネルアップデート
        * Linux Kernel Version: 3.16.0-5
        * Variant 3(CVE-2017-5754) - patched

* CentOS Linux 6.5(2018. 02. 22.)
    * インスタンス作成時に指定した名前でホスト名が適用されるよう修正
    * 脆弱性パッチのための関連カーネルアップデート
        * Linux Kernel Version: 2.6.32-696.20.1
        * Variant 1(CVE-2017-5753) - patched
        * Variant 3(CVE-2017-5754) - patched

* CentOS Linux 7.1(2018. 02. 22.)
    * インスタンス作成時に指定した名前でホスト名が適用されるよう修正
    * Firewall daemon のデフォルト値を変更
        * インスタンス起動時に Firewall daemon が自動起動しないよう設定を変更
    * Swap ディスクマウント設定の変更
        * 新規インスタンス作成時に swap パーティションが自動マウントされるよう設定を変更
    * 脆弱性パッチのための関連カーネルアップデート
        * Linux Kernel Version: 3.10.0-693.17.1
        * Variant 1(CVE-2017-5753) - patched
        * Variant 3(CVE-2017-5754) - patched

* 新規イメージ追加
    * CentOS Linux 6.5 with MySQL 5.6.38(2018. 02. 22.)
        * MySQL 5.6.38 パッケージがインストール済み
        * その他の設定は CentOS Linux 6.5 イメージと同じ
    * CentOS Linux 6.5 with MySQL 5.7.20(2018. 02. 22.)
        * MySQL 5.7.20 パッケージがインストール済み
        * その他の設定は CentOS Linux 6.5 イメージと同じ


<a id="september-21-2017"></a>
## 2017. 09. 21. { #september-21-2017 }
<a id="september-21-2017-public-api"></a>
### Public API { #september-21-2017-public-api }
* TOAST Compute サービスに対する API を提供
    * 現在は限定的な機能のみ利用可能であり、今後 API の追加により機能を拡張する予定です
    * サポートされている API についてはガイドドキュメントを参照してください

<a id="september-21-2017-instance"></a>
### Instance { #september-21-2017-instance }
* キーペアを指定せずにインスタンスを作成できたバグを修正


<a id="july-20-2017"></a>
## 2017. 07. 20. { #july-20-2017 }
<a id="july-20-2017-image"></a>
### Image { #july-20-2017-image }
* 大容量イメージ作成時に断続的に作成が完了しないバグを修正


<a id="august-24-2017"></a>
## 2017. 08. 24. { #august-24-2017 }
<a id="august-24-2017-instance"></a>
### Instance { #august-24-2017-instance }
* インスタンスのスペック変更機能を追加
    * 使用中のインスタンスのディスクをそのまま保持しながら、CPU/Memory をアップグレードまたはダウングレード可能
    * ブロックストレージのサイズは変更不可
    * スペック変更のためにインスタンスは停止状態である必要があります
    * 詳細な制約事項についてはガイドドキュメント [インスタンスのスペック変更](/Compute/Instance/ja/console-guide/#modify-flavor) を参照してください
* Low IOPS SSD スペック (U タイプ) を追加
    * 低価格な低スペックインスタンスをサポート
    * Linux 系 OS のみサポート
    * Local Disk を使用するため、ハードウェア障害時にデータの復旧が不可能
* High IOPS SSD スペック (I タイプ) を追加
    * 高い IOPS を保証(保証 IOPS については価格表を参照)
    * Linux 系 OS のみサポート
* インスタンス使用量照会時に値が取得されないバグを修正


<a id="may-25-2017"></a>
## 2017. 05. 25. { #may-25-2017 }
<a id="may-25-2017-instance"></a>
### Instance { #may-25-2017-instance }
* サービス終了したイメージで作成されたインスタンスが表示されないバグを修正

<a id="may-25-2017-image"></a>
### Image { #may-25-2017-image }
* Windows 系イメージのアップデート
    * Windows 2012 R2 STD(2017. 05. 25.) を追加


<a id="april-25-2017"></a>
## 2017. 04. 25. { #april-25-2017 }
<a id="april-25-2017-instance"></a>
### Instance { #april-25-2017-instance }
* インスタンス作成時の初期ボリュームサイズの最大値を 600GB から 1TB (1,000GB) に変更


<a id="march-23-2017"></a>
## 2017. 03. 23. { #march-23-2017 }
<a id="march-23-2017-instance"></a>
### Instance { #march-23-2017-instance }
* インスタンス作成時に初期ボリュームのサイズを指定する機能を追加
    * ユーザーが指定したサイズで初期ボリュームを作成
    * 基本ディスクのサイズは、イメージごとの最小要件から最大 600GB まで設定可能


<a id="january-19-2017"></a>
## 2017. 01. 19. { #january-19-2017 }
<a id="january-19-2017-instance"></a>
### Instance { #january-19-2017-instance }
* インスタンス基本情報の IP アドレス情報からサブネット名称を除外
    * 名称表記により行の幅が広がり、可読性が低下するのを防止
* インスタンス名の文字数および特殊文字の制限
    * インスタンス名は 20 文字以下の英数字と **.**（ドット）、**-**（ダッシュ）のみ使用可能
* インスタンス作成機能をイメージ作成機能に変更
    * タブと一貫した機能に変更

<a id="january-19-2017-image"></a>
### Image { #january-19-2017-image }
* イメージタブ (Private、Shared、Public) 切り替え時にイメージの選択が解除されない問題を修正


<a id="december-22-2016"></a>
## 2016. 12. 22. { #december-22-2016 }
<a id="december-22-2016-instance"></a>
### Instance { #december-22-2016-instance }
* 停止中のインスタンスのセキュリティグループを編集できるよう変更
* インスタンス作成時に選択可能なセキュリティグループが 1 つの場合、自動的に選択されるよう変更