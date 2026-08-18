<!-- pre-align:aligned sig=f73105f85d1d -->

<a id="compute-release-notes"></a>
## Compute > Release Notes { #compute-release-notes }

<a id="august-20-2026"></a>
## August 20, 2026
### Image

* GPU-related (Linux)
    * Updated the NVIDIA driver: 580.105.08 → 580.173.02
    * Applied the NVIDIA server driver package
    * Added CUDA toolkit: 12.6
    * DCGM: 4.5.0 → 4.6.0
    * DCGM-Exporter: 4.6.0 → 4.8.3
        * Changed to run as root instead of non-root to collect PROF metrics
        * Excluded the LOW_UTIL_VIOLATION metric from collection due to negative counter issues on certain GPUs
        * Changed the listen address and port to 0.0.0.0:9400 so that Exporter data can be collected externally
    * MIG Manager: 0.13.1 → 0.14.4

* 	Added New Images
    * Ubuntu Server 22.04.5 LTS with NVIDIA (August 20, 2026)
    * Ubuntu Server 24.04.4 LTS with NVIDIA (August 20, 2026)
    * PentaSecurity WAPPLES SA 7.0.104.2-hatfix3 (August 20, 2026)

* Ended Image Support
    * Ubuntu Server 22.04.5 LTS with Redis 7.2.4 (July 15, 2025)
    * Ubuntu Server 22.04.5 LTS with NVIDIA (March 10, 2026)
    * PentaSecurity WAPPLES SA 6.0.6 (April 15, 2024)

<a id="may-27-2026"></a>
## May 27, 2026 { #may-27-2026 }
<a id="instance"></a>
### Instance { #instance }
* Adjusted the default value of the `limit` parameter in the List Instances API to 100, and the maximum value to 1,000
* Added information on whether the cumulative suspension period of an instance has exceeded 90 days

<a id="image"></a>
### Image { #image }
* Adjusted the default value of the `limit` parameter in the List Images API to 100, and the maximum value to 1,000

<a id="april-28-2026"></a>
## April 28, 2026 { #april-28-2026 }
<a id="april-28-2026-image"></a>
### Image

* Added new images
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

* End of image support
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
## March 31, 2026 { #march-31-2026 }
* End of service for the US (California) region

<a id="march-10-2026"></a>
## March 10, 2026 { #march-10-2026 }
<a id="march-10-2026-image"></a>
### Image { #march-10-2026-image }
* Disabled GRUB BLS configuration for Rocky 9.7 images
* Removed bullseye-backports repository from sources.list due to end of support for Debian 11.11

* GPU and container-related (Linux)
    * containerd: 1.6.32 → 2.2.1
    * NVIDIA driver update: 535.230.02 → 580.105.08
    * CUDA update: 12.2 → 13.0
    * DCGM: 3.3.5 → 4.5.0
    * DCGM-Exporter: 3.3.5 → 4.5.0
    * MIG Manager: 0.7.0 → 0.13.1

* GPU (Windows)
    * NVIDIA driver update: 539.19 → 581.80
    * CUDA update: 12.2 → 13.0

* Security update
    * Windows 2016: KB5071543
        * https://support.microsoft.com/en-us/topic/december-9-2025-kb5071543-os-build-14393-8688-ec93aa63-f343-4a7e-ab3c-faa096e17395
    * Windows 2019: KB5071544
        * https://support.microsoft.com/en-us/topic/december-9-2025-kb5071544-os-build-17763-8146-630aa62e-f399-4e42-9f7a-2a4d38dd1210
    * Windows 2022: KB5071547
        * https://support.microsoft.com/en-us/topic/december-9-2025-kb5071547-os-build-20348-4529-7935ca9f-cac3-4d17-93bb-fe8e57c6db32

* Added new images
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
* End of image support
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
## January 27, 2026 { #january-27-2026 }
<a id="january-27-2026-instance"></a>
### Instance { #january-27-2026-instance }
* Added serial console feature

<a id="november-25-2025"></a>
## November 25, 2025 { #november-25-2025 }
<a id="november-25-2025-image"></a>
### Image { #november-25-2025-image }
* Improved image modification feature
    * Added option to configure whether to allow image download

* Added new images
    * Rocky Linux 9.5 - Container(2025.11.18.)
    * Ubuntu Server 24.04.3 LTS - Container(2025.11.18.)

<a id="instance-template"></a>
### Instance Template { #instance-template }
* Added feature to create instances from snapshots

<a id="auto-scale"></a>
### Auto Scale { #auto-scale }
* Added feature to create instances from snapshots

<a id="october-28-2025"></a>
## October 28, 2025 { #october-28-2025 }
<a id="october-28-2025-image"></a>
### Image { #october-28-2025-image }
* Added new images
    * Ubuntu Server 22.04.5 LTS for Deep Learning v7.0.0(2025.10.28.)
* End of image support
    * Ubuntu Server 22.04.5 LTS for Deep Learning v5.0.2(2025.07.15.)

<a id="september-23-2025"></a>
## September 23, 2025 { #september-23-2025 }
<a id="september-23-2025-image"></a>
### Image { #september-23-2025-image }
* Added new images
    * PIOLINK WEBFRONT-KS 4.0.6.62.20(2025.09.23.)
    * PIOLINK WEBFRONT-KS 4.0.6.61.33(2025.09.23.)
* End of image support
    * PIOLINK WEBFRONT-KS 4.0.6.61.32(2025.07.15.)

<a id="july-15-2025"></a>
## July 15, 2025 { #july-15-2025 }
<a id="july-15-2025-image"></a>
### Image { #july-15-2025-image }
* Added new images
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

* End of image support
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
## May 27, 2025 { #may-27-2025 }
<a id="may-27-2025-instance"></a>
### Instance { #may-27-2025-instance }
* Added a placement policy feature
* Added a feature to configure whether to delete a network interface upon detachment
* Added a feature to configure the block storage deletion policy when creating an instance or attaching block storage
* Revised the deletion policy for associated resources when deleting an instance from the console
    * Snapshots are deleted together when the associated block storage is deleted

<a id="april-29-2025"></a>
## April 29, 2025 { #april-29-2025 }
<a id="april-29-2025-image"></a>
### Image { #april-29-2025-image }
* Added new images
    * Ubuntu Server 22.04.5 LTS for Deep Learning v6.0.0(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v5.0.1(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v4.0.2(2025.04.29.)
    * Ubuntu Server 22.04.5 LTS for Deep Learning v3.1.2(2025.04.29.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2025.04.29.)

* End of image support
    * Ubuntu Server 22.04.4 LTS for Deep Learning v5.0.0(2024.10.29)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v4.0.1(2024.10.29)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v3.1.1(2024.10.29)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2025.03.25)

<a id="march-25-2025"></a>
## March 25, 2025 { #march-25-2025 }
<a id="march-25-2025-image"></a>
### Image { #march-25-2025-image }
* Added new images
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1(2024.03.25)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with Cubrid 10.2.14(2025.03.25.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13(2025.03.25.)
    * Rocky Linux 8.10 with Tibero 7 Enterprise 277758(2025.03.25.)
    * Rocky Linux 8.10 with Tibero 7 Standard 277758(2025.03.25.)

* End of image support
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
## March 4, 2025 { #march-4-2025 }
<a id="march-4-2025-instance"></a>
### Instance { #march-4-2025-instance }
* Added a feature to change the instance description
* Added a restriction to prevent changing the API password to the same as the current password
* Added a feature to create instances from block storage and snapshots

<a id="march-4-2025-image"></a>
### Image { #march-4-2025-image }
* Changed the default Python for Rocky 8.10 from platform Python to system Python (Python 3.11 → 3.6)

* GPU and container-related (Linux)
    * containerd: 1.6.32 → No change
    * NVIDIA driver update: 535.216.01 → 535.230.02
    * CUDA update: 12.2 → No change
    * DCGM: 3.3.5 → No change
    * DCGM-Exporter: 3.3.5 → No change
    * MIG Manager: 0.7.0 → No change

* GPU (Windows)
    * NVIDIA driver update: 538.95 → 539.19
    * CUDA update: 12.2 → No change

* Security update
    * Windows 2016: KB5049993
        * https://support.microsoft.com/en-us/topic/january-14-2025-kb5049993-os-build-14393-7699-b148c0ad-29fd-460e-b4a2-db38e88ae937
    * Windows 2019: KB5050008
        * https://support.microsoft.com/en-us/topic/january-14-2025-kb5050008-os-build-17763-6775-9a174725-a7ea-4e37-a6f8-e86f7c4d3f31
    * Windows 2022: KB5049983
        * https://support.microsoft.com/en-us/topic/january-14-2025-kb5049983-os-build-20348-3091-789bf923-7777-419d-9c3a-23f7c814930f

* Added new images
    * Debian 11.11 Bullseye (2025.02.25.)
    * Debian 12.9 Bookworm (2025.02.25.)
    * Rocky Linux 8.10 (2025.02.25.)
    * Rocky Linux 8.10 - Container (2025.02.25.)
    * Rocky Linux 8.10 for NAT (2025.02.25.)
    * Rocky Linux 9.5 (2025.02.25.)
    * Ubuntu Server 20.04.6 LTS (2025.02.25.)
    * Ubuntu Server 20.04.6 LTS - Container (2025.02.25.)
    * Ubuntu Server 20.04.6 LTS for NAT (2025.02.25.)
    * Ubuntu Server 20.04.6 LTS with NVIDIA (2025.02.25.)
    * Ubuntu Server 22.04.5 LTS (2025.02.25.)
    * Ubuntu Server 22.04.5 LTS - Container (2025.02.25.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA (2025.02.25.)
    * Ubuntu Server 24.04.1 LTS (2025.02.25.)
    * Windows 2016 STD (2025.02.25.) EN
    * Windows 2016 STD (2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard (2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard (2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard (2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard (2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2019 Express (2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2019 Express (2025.02.25.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard (2025.02.25.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard (2025.02.25.) KO
    * Windows 2019 STD (2025.02.25.) EN
    * Windows 2019 STD (2025.02.25.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard (2025.02.25.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard (2025.02.25.) KO
    * Windows 2019 STD with NVIDIA (2025.02.25.) KO
    * Windows 2022 STD (2025.02.25.) EN
    * Windows 2022 STD (2025.02.25.) KO
    * Windows 2022 STD with MS-SQL 2022 Standard (2025.02.25.) EN
    * Windows 2022 STD with MS-SQL 2022 Standard (2025.02.25.) KO

* End of image support
    * Debian 11.11 Bullseye (2024.11.19.)
    * Debian 12.7 Bookworm (2024.11.19.)
    * Rocky Linux 8.10 (2024.11.19.)
    * Rocky Linux 8.10 - Container (2024.11.19.)
    * Rocky Linux 8.10 for NAT (2024.11.19.)
    * Rocky Linux 9.4 (2024.11.19.)
    * Ubuntu Server 20.04.6 LTS (2024.11.19.)
    * Ubuntu Server 20.04.6 LTS - Container (2024.11.19.)
    * Ubuntu Server 20.04.6 LTS for NAT (2024.11.19.)
    * Ubuntu Server 20.04.6 LTS with NVIDIA (2024.11.19.)
    * Ubuntu Server 22.04.5 LTS (2024.11.19.)
    * Ubuntu Server 22.04.5 LTS - Container (2024.11.19.)
    * Ubuntu Server 22.04.5 LTS with NVIDIA (2024.11.19.)
    * Windows 2016 STD (2024.11.19.) EN
    * Windows 2016 STD (2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2019 Express (2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2019 Express (2024.11.19.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.11.19.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.11.19.) KO
    * Windows 2019 STD (2024.11.19.) EN
    * Windows 2019 STD (2024.11.19.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.11.19.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.11.19.) KO
    * Windows 2022 STD (2024.11.19.) EN
    * Windows 2022 STD (2024.11.19.) KO


<a id="december-24-2024"></a>
## December 24, 2024 { #december-24-2024 }
<a id="december-24-2024-image"></a>
### Image { #december-24-2024-image }
* Changed Tibero image names
  * Rocky Linux 8.10 with Tibero 7 Enterprise (2024.11.19.) → Rocky Linux 8.10 with Tibero 7 Enterprise 277758 (2024.11.19.)
  * Rocky Linux 8.10 with Tibero 7 Standard (2024.11.19.) → Rocky Linux 8.10 with Tibero 7 Standard 277758 (2024.11.19.)

<a id="november-26-2024"></a>
## November 26, 2024 { #november-26-2024 }
<a id="november-26-2024-instance"></a>
### Instance { #november-26-2024-instance }
* Added a feature to update instance OS information

<a id="november-26-2024-image"></a>
### Image { #november-26-2024-image }
* Improved the image modification feature
  * Added modifiable items
    * Set OS version value
    * Set maximum CPU value
    * Set minimum CPU value
    * Set minimum memory value
    * Set minimum block storage value
    * Set whether to use the image creation feature
    * Set whether to use the user script feature
    * Set the target service

* GPU and container-related (Linux)
    * containerd: 1.6.32 → no change
    * NVIDIA driver update: 535.183.06 → 535.216.01
    * CUDA update: 12.2 → no change
    * DCGM: 3.3.5 → no change
    * DCGM-Exporter: 3.4.1 → no change
    * MIG Manager: 0.7.0 → no change
    * Minimum disk size (GB): 20 → 30
    * Patched an issue where DCGM-Exporter was not installed (NVIDIA, Deep Learning images)

* GPU (Windows)
    * NVIDIA driver update: 538.78 → 538.95
    * CUDA version: 12.2

* Security update
    * Windows 2016: KB5044293
        * https://support.microsoft.com/en-us/topic/october-8-2024-kb5044293-os-build-14393-7428-3f172048-e2d1-4eb2-b6b9-41abd891e52f
    * Windows 2019: KB5044277
        * https://support.microsoft.com/en-us/topic/october-8-2024-kb5044277-os-build-17763-6414-edccc872-2f4e-4ac6-b224-50ca8f1acd4f
    * Windows 2022: KB5044281
        * https://support.microsoft.com/en-us/topic/october-8-2024-kb5044281-os-build-20348-2762-e063059c-9122-4324-86e8-4f6f3383a20a

* Added new images
     * Rocky Linux 8.10 for NAT (2024.11.19.)
     * Rocky Linux 8.10 with Tibero 7 Enterprise (2024.11.19.)
     * Rocky Linux 8.10 with Tibero 7 Standard (2024.11.19.)
     * Rocky Linux 9.4 (2024.11.19.)

* End of image support
     * CentOS 7.9 (2024.08.20.)
     * CentOS 7.9 - Container (2024.08.20.)
     * CentOS 7.9 for NAT (2024.08.20.)
     * CentOS 7.9 with Apache Kafka 3.6.1 (2024.04.23.)
     * CentOS 7.9 with CUBRID 10.2.14 (2024.04.23.)
     * CentOS 7.9 with CUBRID 11.0.13 (2024.04.23.)
     * CentOS 7.9 with MariaDB 10.11.7 (2024.04.23.)
     * CentOS 7.9 with MySQL 8.0.36 (2024.04.23.)
     * CentOS 7.9 with PostgreSQL 15.6 (2024.04.23.)
     * CentOS 7.9 with Redis 7.2.4 (2024.04.23.)
     * CentOS 7.9 with Tibero 7 CEE (2024.04.23.)
     * CentOS 7.9 with Tibero 7 CSE (2024.04.23.)


* Image updates (Linux)
     * Debian 11.11 Bullseye (2024.11.19.)
     * Debian 12.7 Bookworm (2024.11.19.)
     * Rocky Linux 8.10 (2024.11.19.)
     * Rocky Linux 8.10 - Container (2024.11.19.)
     * Ubuntu Server 20.04.6 LTS (2024.11.19.)
     * Ubuntu Server 20.04.6 LTS - Container (2024.11.19.)
     * Ubuntu Server 20.04.6 LTS for NAT (2024.11.19.)
     * Ubuntu Server 22.04.4 LTS for Deep Learning v3.1.1 (2024.10.29.)
     * Ubuntu Server 22.04.4 LTS for Deep Learning v4.0.1 (2024.10.29.)
     * Ubuntu Server 22.04.4 LTS for Deep Learning v5.0.0 (2024.10.29.)
     * Ubuntu Server 20.04.6 LTS with NVIDIA (2024.11.19.)
     * Ubuntu Server 22.04.5 LTS (2024.11.19.)
     * Ubuntu Server 22.04.5 LTS - Container (2024.11.19.)
     * Ubuntu Server 22.04.5 LTS with NVIDIA (2024.11.19.)

* Image updates (Windows)
     * Windows 2016 STD (2024.11.19.) EN
     * Windows 2016 STD (2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2016 Standard (2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2016 Standard (2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2017 Standard (2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2017 Standard (2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2019 Express (2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2019 Express (2024.11.19.) KO
     * Windows 2016 STD with MS-SQL 2019 Standard (2024.11.19.) EN
     * Windows 2016 STD with MS-SQL 2019 Standard (2024.11.19.) KO
     * Windows 2019 STD (2024.11.19.) EN
     * Windows 2019 STD (2024.11.19.) KO
     * Windows 2019 STD with MS-SQL 2019 Standard (2024.11.19.) EN
     * Windows 2019 STD with MS-SQL 2019 Standard (2024.11.19.) KO
     * Windows 2019 STD with NVIDIA (2024.11.19.) KO
     * Windows 2022 STD (2024.11.19.) EN
     * Windows 2022 STD (2024.11.19.) KO

<a id="image-builder"></a>
### Image Builder { #image-builder }
* End of application version support
    * NHN Kubernetes Service(NKS) Worker Node 1.0
    * NHN Kubernetes Service(NKS) Worker Node(GPU) 1.0
    * MySQL 5.7
    * MariaDB 10.3
* End of base image support
    * CentOS 7.9

<a id="october-29-2024"></a>
## October 29, 2024 { #october-29-2024 }
<a id="october-29-2024-image-builder"></a>
### Image Builder { #october-29-2024-image-builder }
* Added application versions
    * Deep Learning Framework 5.0

<a id="october-29-2024-image"></a>
### Image { #october-29-2024-image }
* Added new images
    * Ubuntu Server 22.04.4 LTS for Deep Learning v3.1.1 (2024.10.29.)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v4.0.1 (2024.10.29.)
    * Ubuntu Server 22.04.4 LTS for Deep Learning v5.0.0 (2024.10.29.)

* End of image support
    * Ubuntu Server 22.04.3 LTS for Deep Learning v3.1.0 (2023.11.21.)
    * Ubuntu Server 22.04.3 LTS for Deep Learning v4.0.0 (2024.04.23.)

* Image updates (Linux)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1 (2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.14 (2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13 (2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7 (2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36 (2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15.8 (2024.10.29.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4 (2024.10.29.)

<a id="august-27-2024"></a>
## August 27, 2024 { #august-27-2024 }
<a id="august-27-2024-image"></a>
### Image { #august-27-2024-image }
* GPU and container-related (Linux)
    * containerd: 1.6.31 → 1.6.32
    * NVIDIA driver update: 535.161.08 → 535.183.06
    * CUDA update: 12.2 → No change
    * MIG Manager: 0.7.0 → No change
    * NVIDIA DCGM: 3.3.5 → No change
    * NVIDIA DCGM Exporter: 3.4.1 → No change

* GPU (Windows)
    * NVIDIA driver update: 538.46 → 538.78

* Security update (Windows)
    * Windows 2016: KB5040434
        * https://support.microsoft.com/en-us/topic/july-9-2024-kb5040434-os-build-14393-7159-40d1baef-65b4-467f-9bd9-729d369fcc4c
    * Windows 2019: KB5040430
        * https://support.microsoft.com/en-us/topic/july-9-2024-kb5040430-os-build-17763-6054-0bb10c24-db8c-47eb-8fa9-9ebc06afa4e7
    * Windows 2022: KB5040437
        * https://support.microsoft.com/en-us/topic/july-9-2024-kb5040437-os-build-20348-2582-5b28d9b8-fcba-43bb-91e6-062f43c7ec7c

* Added new images
    * Debian 12.6 Bookworm (2024.08.20.)
    * Rocky Linux 8.10 (2024.08.20.)

* End of image support
    * Debian 10.13 Buster (2024.05.21.)
    * Rocky Linux 8.9 (2024.05.21.)

* Image updates (Linux)
    * CentOS 7.9 (2024.08.20.)
    * CentOS 7.9 for NAT (2024.08.20.)
    * Debian 11.10 Bullseye (2024.08.20.)
    * Ubuntu Server 20.04.6 LTS (2024.08.20.)
    * Ubuntu Server 20.04.6 LTS for NAT (2024.08.20.)
    * Ubuntu Server 20.04.6 LTS with NVIDIA (2024.08.20.)
    * Ubuntu Server 22.04.4 LTS (2024.08.20.)
    * Ubuntu Server 22.04.4 LTS with NVIDIA (2024.08.20.)

* Image updates (Windows)
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
* Added US (California) region

<a id="august-27-2024-instance"></a>
### Instance { #august-27-2024-instance }
* Added a feature to change instance key pairs

<a id="august-27-2024-image-builder"></a>
### Image Builder { #august-27-2024-image-builder }
* Added supported application versions
    * PostgreSQL 15
    * NHN Kubernetes Service (NKS) Worker Node 1.6
    * NHN Kubernetes Service (NKS) Worker Node (GPU) 1.6
* End of application version support
    * PostgreSQL 10
    * PostgreSQL 11
    * PostgreSQL 12
    * PostgreSQL 13
    * PostgreSQL 14
    * Slurm 21.08
    * WebtoB 5.0
    * JEUS (Domain Administrator Server) 8
    * JEUS (Managed Server) 8
* Added new base images
    * Rocky Linux 8.10
    * Debian 12 Bookworm
* End of base image support
    * Rocky Linux 8.9
    * Debian 10 Buster
    * Debian 11 Bullseye
        * Applies to NHN Kubernetes Service (NKS) Worker Node / NHN Kubernetes Service (NKS) Worker Node (GPU)

<a id="may-28-2024"></a>
## May 28, 2024 { #may-28-2024 }
<a id="may-28-2024-instance"></a>
### Instance { #may-28-2024-instance }
* Expanded search/filter conditions and improved UI in the instance list
    * Added search conditions
        * Instance name
        * Instance type
        * Image ID
    * Added filter conditions
        * Image type
        * Instance status

<a id="may-28-2024-image"></a>
### Image { #may-28-2024-image }
* GPU and container-related (Linux)
    * containerd: 1.6.27 → 1.6.31
    * NVIDIA driver update: 535.154.05 → 535.161.08
    * CUDA update: 12.2 → No change
    * MIG Manager: 0.5.5 → 0.7.0
    * NVIDIA DCGM: 3.1.8 → 3.3.5
    * NVIDIA DCGM Exporter: 3.1.5 → 3.4.1

* GPU (Windows)
    * NVIDIA driver update: 538.46 → 538.15

* Security update (Windows)
    * Windows 2016: KB5036899
        * https://support.microsoft.com/en-us/topic/april-9-2024-kb5036899-os-build-14393-6897-6a0b7cdd-dd67-4ef8-8c38-8a936b2f952c
    * Windows 2019: KB5036896
        * https://support.microsoft.com/en-us/topic/april-9-2024-kb5036896-os-build-17763-5696-efb580f1-2ce4-4695-b76c-d2068a00fb92
    * Windows 2022: KB5036909
        * https://support.microsoft.com/en-us/topic/april-9-2024-kb5036909-os-build-20348-2402-36062ce9-f426-40c6-9fb9-ee5ab428da8c

* Image update (Linux)
    * CentOS 7.9 (2024.05.21.)
    * CentOS 7.9 - Container (2024.05.21.)
    * CentOS 7.9 for NAT (2024.05.21.)
    * Debian 10.13 Buster (2024.05.21.)
    * Debian 11.9 Bullseye (2024.05.21.)
    * Rocky Linux 8.9 (2024.05.21.)
    * Ubuntu Server 20.04.6 LTS (2024.05.21.)
    * Ubuntu Server 20.04.6 LTS for NAT (2024.05.21.)
    * Ubuntu Server 22.04.4 LTS (2024.05.21.)

* Image update (Windows)
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
## April 23, 2024 { #april-23-2024 }
<a id="april-23-2024-instance"></a>
### Instance { #april-23-2024-instance }
* End of instance type support — applies to Korea (Pangyo) region
    * u2 (Ephemeral Storage Instance)

<a id="april-23-2024-image"></a>
### Image { #april-23-2024-image }
* Added new images
    * CentOS 7.9 with Apache Kafka 3.6.1 (2024.04.23.)
    * CentOS 7.9 with CUBRID 10.2.14 (2024.04.23.)
    * CentOS 7.9 with CUBRID 11.0.13 (2024.04.23.)
    * CentOS 7.9 with MariaDB 10.11.7 (2024.04.23.)
    * CentOS 7.9 with MySQL 8.0.36 (2024.04.23.)
    * CentOS 7.9 with PostgreSQL 15.6 (2024.04.23.)
    * CentOS 7.9 with Redis 7.2.4 (2024.04.23.)
    * CentOS 7.9 with Tibero 7 CEE (2024.04.23.)
    * CentOS 7.9 with Tibero 7 CSE (2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.6.1 (2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.14 (2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.13 (2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.11.7 (2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.36 (2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with PostgreSQL 15.6 (2024.04.23.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.2.4 (2024.04.23.)
    * Ubuntu Server 22.04.3 LTS for Deep Learning v4.0.0 (2024.04.23.)

* End of image support
    * CentOS 7.9 with Apache Kafka 3.3.1 (2022.12.20.)
    * CentOS 7.9 with CUBRID 10.2.10 (2023.03.21.)
    * CentOS 7.9 with CUBRID 11.0.10 (2023.03.21.)
    * CentOS 7.9 with MariaDB 10.3.31 (2022.12.20.)
    * CentOS 7.9 with MariaDB 10.6.11 (2023.03.21.)
    * CentOS 7.9 with MySQL 5.7.35 (2022.12.20.)
    * CentOS 7.9 with MySQL 8.0.27 (2022.12.20.)
    * CentOS 7.9 with PostgreSQL 10.20 (2022.12.20.)
    * CentOS 7.9 with PostgreSQL 11.15 (2022.12.20.)
    * CentOS 7.9 with PostgreSQL 12.10 (2022.12.20.)
    * CentOS 7.9 with PostgreSQL 13.6 (2022.12.20.)
    * CentOS 7.9 with PostgreSQL 14.2 (2022.12.20.)
    * CentOS 7.9 with Redis 7.0.5 (2022.12.20.)
    * CentOS 7.9 with Tibero 7 CEE (2023.10.31.)
    * CentOS 7.9 with Tibero 7 CSE (2023.10.31.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.3.1 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.10 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.10 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.6.11 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.27 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.0.5 (2023.03.21.)

<a id="april-15-2024"></a>
## April 15, 2024 { #april-15-2024 }
<a id="april-15-2024-image"></a>
### Image { #april-15-2024-image }
* Image update
    * PentaSecurity WAPPLES SA 6.0.6 (2024.04.15.)

<a id="march-26-2024"></a>
## March 26, 2024 { #march-26-2024 }
<a id="march-26-2024-image-builder"></a>
### Image Builder { #march-26-2024-image-builder }
* Added application version
    * Deep Learning Framework 4.0

<a id="february-27-2024"></a>
## February 27, 2024 { #february-27-2024 }
<a id="february-27-2024-image"></a>
### Image { #february-27-2024-image }
* Added new images
    * Rocky Linux 8.9 (2024.02.20.)

* End of image support
    * Rocky Linux 8.8 (2023.11.21.)

* GPU and container-related (Linux)
    * containerd: 1.6.22 → 1.6.27
    * NVIDIA driver update: 535.104.12 → 535.154.05
    * CUDA update: 12.2 → No change
    * MIG Manager: 0.5.5 → No change

* GPU (Windows)
    * NVIDIA driver update: 537.13 → 538.15

* Security update (Windows)
    * Windows 2016: KB5034119
        * https://support.microsoft.com/en-us/topic/january-9-2024-kb5034119-os-build-14393-6614-7e7dae78-5944-4041-bf3d-4660e5ef7bb4
    * Windows 2019: KB5034127
        * https://support.microsoft.com/en-gb/topic/january-9-2024-kb5034127-os-build-17763-5329-4de58ce5-eb0d-4b9a-95d1-aa15fe30b082
    * Windows 2022: KB5034129
        * https://support.microsoft.com/en-us/topic/january-9-2024-kb5034129-os-build-20348-2227-6958a36f-efaf-4ef5-a576-c5931072a89a

* Image updates (Linux)
    * CentOS 7.9 (2024.02.20.)
    * CentOS 7.9 for NAT (2024.02.20.)
    * Debian 10.13 Buster (2024.02.20.)
    * Debian 11.8 Bullseye (2024.02.20.)
    * Rocky Linux 8.9 (2024.02.20.)
    * Ubuntu Server 20.04.6 LTS (2024.02.20.)
    * Ubuntu Server 20.04.6 LTS for NAT (2024.02.20.)
    * Ubuntu Server 22.04.3 LTS (2024.02.20.)

* Image updates (Windows)
    * Windows 2016 STD (2024.02.20.) EN
    * Windows 2016 STD (2024.02.20.) KO
    * Windows 2019 STD (2024.02.20.) EN
    * Windows 2019 STD (2024.02.20.) KO
    * Windows 2022 STD (2024.02.20.) EN
    * Windows 2022 STD (2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2016 Standard (2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2017 Standard (2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2019 Express (2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2019 Express (2024.02.20.) KO
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.02.20.) EN
    * Windows 2016 STD with MS-SQL 2019 Standard (2024.02.20.) KO
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.02.20.) EN
    * Windows 2019 STD with MS-SQL 2019 Standard (2024.02.20.) KO

<a id="february-27-2024-instance"></a>
### Instance { #february-27-2024-instance }
* Added a feature to create images from instances with encrypted root block storage
* Disabled the instance termination feature for GPU instances


<a id="november-28-2023"></a>
## November 28, 2023 { #november-28-2023 }
<a id="november-28-2023-instance"></a>
### Instance { #november-28-2023-instance }
* Added an instance shutdown feature

<a id="november-28-2023-public-api"></a>
### Public API { #november-28-2023-public-api }
* Added APIs for shutting down instances and starting shut-down instances

<a id="november-28-2023-image"></a>
### Image { #november-28-2023-image }
* Removed the limit on the number of image sharing members

* Added new images
	* Ubuntu Server 22.04.3 LTS with NVIDIA(2023.11.21.)
	* Ubuntu Server 22.04.3 LTS - Container(2023.11.21.)
	* Ubuntu Server 22.04.3 LTS for Deep Learning v3.1.0(2023.11.21.)

* End of image support
	* Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.1(2023.09.26.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.1(2023.09.26.)

* GPU and container-related (Linux)
    * debian 11 container - Added GPU driver support; clusters can now be created after selecting a GPU flavor
    * Updated NVIDIA driver: 470.199.02 → 535.104.12
    * Updated CUDA: 11.4 → 12.2
    * MIG Manager: 0.5.4 → 0.5.5

* GPU (Windows)
	* Updated NVIDIA driver: 474.44 → 537.13

* Security update (Linux)
	* CentOS 7.9: Removed SetUID from /usr/bin/newgrp and /sbin/unix_chkpwd

* Security update (Windows)
	* Windows 2016: KB5031362
		* https://support.microsoft.com/en-au/topic/october-10-2023-kb5031362-os-build-14393-6351-0c6e713e-3d6a-4593-8a75-af0a605f249c
	* Windows 2019: KB5031361
		* https://support.microsoft.com/en-gb/topic/october-10-2023-kb5031361-os-build-17763-4974-766593db-b47a-4b18-a698-906426860313
	* Windows 2022: KB5031364
		* https://support.microsoft.com/en-us/topic/october-10-2023-kb5031364-os-build-20348-2031-7f1d69e7-c468-4566-887a-1902af791bbc

* Image updates (Linux)
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

* Image updates (Windows)
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
* Launched the Bare Metal Instance service

<a id="october-31-2023"></a>
## October 31, 2023 { #october-31-2023 }

<a id="system-monitoring"></a>
### System Monitoring { #system-monitoring }
* Bug Fixes
  * Fixed an issue where alarms continued to be sent to users who had been removed from a project

<a id="october-31-2023-image"></a>
### Image { #october-31-2023-image }
* Added new images
    * CentOS 7.9 with Tibero 7 CSE(2023.10.31.)
    * CentOS 7.9 with Tibero 7 CEE(2023.10.31.)

* End of image support
    * CentOS 7.9 with Tibero 6(2022.12.20.)


<a id="september-26-2023"></a>
## September 26, 2023 { #september-26-2023 }
<a id="september-26-2023-image"></a>
### Image { #september-26-2023-image }
* Added new images
    * Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.1(2023.09.26.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.1(2023.09.26.)
    * PentaSecurity WAPPLES SA 6.0.6(2023.09.26.)

* End of image support
    * Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.0(2023.06.27.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.0(2023.08.22.)
    * Windows 2012 R2 STD(2023.08.22.) EN
    * Windows 2012 R2 STD(2023.08.22.) KO
    * Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) KO

* PIOLINK WEBFRONT-KS 4.0.6.61.28(2023.04.25.)
    * Renamed image: PLOS-WAF-KS-v4.0.6.61.28(2023.04.25.) → PIOLINK WEBFRONT-KS 4.0.6.61.28(2023.04.25.)

<a id="august-29-2023"></a>
## August 29, 2023 { #august-29-2023 }
<a id="august-29-2023-public-api"></a>
### Public API { #august-29-2023-public-api }
* Added image upload/download APIs

<a id="august-29-2023-image"></a>
### Image { #august-29-2023-image }
* Added new images
    * Rocky Linux 8.8(2023.08.22.)
    * Ubuntu Server 20.04.6 LTS for Deep Learning v3.0.0(2023.08.22.)
    * CentOS 7.9 for NAT(2023.08.22.)

* End of image support
    * Rocky Linux 8.7(2023.05.25.)

* GPU
    * NVIDIA driver updated (Linux): 470.182.03 → 470.199.02
    * dcgm updated (Linux): 3.1.7 → 3.1.8
    * NVIDIA driver updated (Windows): 474.30 → 474.44

* Image renamed
    * Ubuntu Server 20.04.6 LTS for Deep Learning(2023.06.27.) → Ubuntu Server 20.04.6 LTS for Deep Learning v2.1.0(2023.06.27.)

* CentOS 7.9(2023.08.22.)
    * Image updated
* Debian 10.13 Buster(2023.08.22.)
    * Image updated
* Debian 11.7 Bullseye(2023.08.22.)
    * Image updated
* Ubuntu Server 20.04.6 LTS(2023.08.22.)
    * Image updated
* Ubuntu Server 20.04.6 LTS for NAT(2023.08.22.)
    * Image updated
* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.08.22.)
    * Image updated
* Ubuntu Server 22.04.2 LTS(2023.08.22.)
    * Image updated
* Windows 2012 R2 STD(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2016 STD(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2016 Standard(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2017 Standard(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2017 Standard(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Express(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Express(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Standard(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Standard(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2019 STD(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with MS-SQL 2019 Standard(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with MS-SQL 2019 Standard(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with NVIDIA(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2022 STD(2023.08.22.) EN
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-us/topic/july-11-2023-security-update-kb5028171-34557119-e00c-4678-bb87-048a36ed8585
* Windows 2022 STD(2023.08.22.) KO
    * Image updated
    * July 2023 security update applied: https://support.microsoft.com/en-us/topic/july-11-2023-security-update-kb5028171-34557119-e00c-4678-bb87-048a36ed8585

<a id="august-29-2023-instance"></a>
### Instance { #august-29-2023-instance }
* Added a feature to delete the floating IP and additional block storage attached to an instance when deleting the instance

<a id="august-29-2023-instance-template"></a>
### Instance Template { #august-29-2023-instance-template }
* Added support for encrypted block storage types

<a id="scaling-group"></a>
### Scaling Group { #scaling-group }
* Added support for encrypted block storage types


<a id="july-25-2023"></a>
## July 25, 2023 { #july-25-2023 }
<a id="july-25-2023-image-builder"></a>
### Image Builder { #july-25-2023-image-builder }
* Added application versions
    * Deep Learning Framework 3.0.0


<a id="june-27-2023"></a>
## June 27, 2023 { #june-27-2023 }
<a id="june-27-2023-system-monitoring"></a>
### System Monitoring { #june-27-2023-system-monitoring }
* Fixed an issue where Excel generation occasionally failed to complete when using the **Monthly Metrics Report** feature
* Windows agent
    * Improved high availability functionality
    * Added logs

<a id="june-27-2023-image-builder"></a>
### Image Builder { #june-27-2023-image-builder }
* Added application versions
    * Deep Learning Framework 2.1.0
* End of application version support
    * Deep Learning Framework 2.0.1

<a id="june-27-2023-image"></a>
### Image { #june-27-2023-image }
* GPU
    * NVIDIA driver updated (Linux): 470.182.03

* Ubuntu Server 20.04.6 LTS for Deep Learning(2023.06.27.)
    * Image updated

<a id="may-30-2023"></a>
## May 30, 2023 { #may-30-2023 }

<a id="may-30-2023-instance"></a>
### Instance { #may-30-2023-instance }
* Improved **CloudTrail** logs for instance creation and deletion
* Improved the UI to allow specifying multiple existing network interfaces when creating an instance

<a id="may-30-2023-image-builder"></a>
### Image Builder { #may-30-2023-image-builder }
* Added applications:
    * NHN Kubernetes Service (NKS) Worker Node
    * NHN Kubernetes Service (NKS) Worker Node (GPU)

<a id="may-30-2023-image"></a>
### Image { #may-30-2023-image }
* Added new images:
    * Rocky Linux 8.7 (2023.05.25.)
    * Ubuntu Server 20.04.6 LTS for NAT (2023.05.25.)

* End of image support:
    * Rocky Linux 8.6 (2023.03.21.)
    * Ubuntu Server 18.04.6 LTS (2023.02.21.)
    * Ubuntu Server 18.04.6 LTS for NAT (2023.02.21.)
    * Ubuntu Server 18.04.5 LTS for AI (2021.06.22.)
    * Ubuntu Server 18.04.6 LTS with NVIDIA (2023.03.21.)

* GPU
    * Updated NVIDIA driver (Linux): 450.216.04 → 470.182.03
    * Updated NVIDIA driver: 453.94 → 474.30

* CentOS 7.9 (2023.05.25.)
    * Image update
* Debian 10.13 Buster (2023.05.25.)
    * Image update
    * Fixed an issue where the instance was inaccessible when Multi NIC was configured
* Debian 11.6 Bullseye (2023.05.25.)
    * Image update
    * Applied cgroup v2 disable setting
* Ubuntu Server 20.04.6 LTS (2023.05.25.)
    * Image update
* Ubuntu Server 20.04.6 LTS with NVIDIA (2023.05.25.)
    * Image update
* Ubuntu Server 20.04.6 LTS for Deep Learning (2023.05.25.)
    * Image update
* Ubuntu Server 22.04.2 LTS (2023.05.25.)
    * Image update
* Windows 2012 R2 STD (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2012 R2 STD (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2016 STD (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2019 STD (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2019 STD (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2022 STD (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-gb/topic/april-11-2023-kb5025230-os-build-20348-1668-28a5446e-6389-4a5b-ae3f-e942a604f2d3
* Windows 2022 STD (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-gb/topic/april-11-2023-kb5025230-os-build-20348-1668-28a5446e-6389-4a5b-ae3f-e942a604f2d3
* Windows 2012 R2 STD with MS-SQL 2016 Standard (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2012 R2 STD with MS-SQL 2016 Standard (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2016 STD with MS-SQL 2016 Standard (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2016 Standard (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2017 Standard (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2017 Standard (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Express (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Express (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Standard (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Standard (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2019 STD with MS-SQL 2019 Standard (2023.05.25.) EN
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2019 STD with MS-SQL 2019 Standard (2023.05.25.) KO
    * Image update
    * Applied November 2023 security update: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f

<a id="april-25-2023"></a>
## April 25, 2023 { #april-25-2023 }
<a id="april-25-2023-image"></a>
### Image { #april-25-2023-image }
* Added new images:
    * Ubuntu Server 20.04.6 LTS for Deep Learning (2023.04.25.)
    * PLOS-WFK-KS-v4.0.6.61.28 (2023.04.25.)

* End of image support:
    * Ubuntu Server 18.04.6 LTS for Deep Learning (2022.01.25.)
    * PLOS-WFK-KS-v4.0.6.61.25 (2022.09.20.)

<a id="april-25-2023-system-monitoring"></a>
### System Monitoring { #april-25-2023-system-monitoring }
* Bug Fixes
    * Fixed an issue where downloaded monthly metric reports intermittently failed to run properly

<a id="march-28-2023"></a>
## March 28, 2023 { #march-28-2023 }
<a id="march-28-2023-image"></a>
### Image { #march-28-2023-image }
* Added new images:
    * CentOS 7.9 with CUBRID 10.2.10 (2023.03.21.)
    * CentOS 7.9 with CUBRID 11.0.10 (2023.03.21.)
    * CentOS 7.9 with MariaDB 10.6.11 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.27 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.0.5 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.3.1 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.10 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.10 (2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.6.11 (2023.03.21.)

* End of image support:
    * CentOS 7.9 with CUBRID 10.2.4 (2022.12.20.)
    * CentOS 7.9 with CUBRID 11.0.2 (2022.12.20.)

* Debian 10.13 Buster (2023.03.21.)
    * Image update
* Debian 11.6 Bullseye (2023.03.21.)
    * Image update
* Rocky Linux 8.6 (2023.03.21.)
    * Image update
* Ubuntu Server 18.04.6 LTS (2023.03.21.)
    * Image update
* Ubuntu Server 18.04.6 LTS for NAT (2023.03.21.)
    * Image update
* Ubuntu Server 18.04.6 LTS with NVIDIA (2023.03.21.)
    * Image update
* Ubuntu Server 20.04.6 LTS (2023.03.21.)
    * Image update
* Ubuntu Server 20.04.6 LTS with NVIDIA (2023.03.21.)
    * Image update
* Ubuntu Server 22.04.2 LTS (2023.03.21.)
    * Image update

<a id="march-28-2023-image-builder"></a>
### Image Builder { #march-28-2023-image-builder }
* Added Features
    * Added support for selecting a personal image as the base image when building an image

<a id="march-28-2023-public-api"></a>
### Public API { #march-28-2023-public-api }
* Changed the API endpoint

<a id="march-28-2023-system-monitoring"></a>
### System Monitoring { #march-28-2023-system-monitoring }
* Removed the `1 minute` option from the period selection criteria in the monthly metric report

<a id="february-28-2023"></a>
## February 28, 2023 { #february-28-2023 }

<a id="february-28-2023-image"></a>
### Image { #february-28-2023-image }
* Added new images
    * Ubuntu Server 22.04.1 LTS (2023.02.21.)
    * Ubuntu Server 20.04.5 LTS with NVIDIA (2023.02.21.)

* Kernel update

* GPU
    * Updated NVIDIA driver (Windows): 453.51 → 453.94
    * Updated NVIDIA driver (Linux): 450.191.01 → 450.216.04

* Rocky Linux 8.6 (2023.02.21.)
    * Image update
* Debian 10.13 Buster (2023.02.21.)
    * Image update
* Debian 11.6 Bullseye (2023.02.21.)
    * Image update
* Ubuntu Server 18.04.6 LTS (2023.02.21.)
    * Image update
* Ubuntu Server 18.04.6 LTS for NAT (2023.02.21.)
    * Image update
* Ubuntu Server 20.04.5 LTS (2023.02.21.)
    * Image update
* Ubuntu Server 18.04.6 LTS with NVIDIA (2023.02.21.)
    * Image update
* Windows 2012 R2 STD (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022352-monthly-rollup-cf299bf2-707b-47db-89a5-4e22c5ce4e26
* Windows 2016 STD (2023.02.14.)
    * Image update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
    * Applied January 2023 security update
* Windows 2019 STD (2023.02.14.)
    * Image update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022286-os-build-17763-3887-48683103-7b22-4f36-aa98-0049c7a6e579
    * Applied January 2023 security update
* Windows 2022 STD (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022291-os-build-20348-1487-38772acf-103f-463e-9d60-486174e806b2
* Windows 2012 R2 STD with MS-SQL 2016 Standard (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022352-monthly-rollup-cf299bf2-707b-47db-89a5-4e22c5ce4e26
* Windows 2016 STD with MS-SQL 2016 Standard (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2017 Standard (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2019 Express (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2019 Standard (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2019 STD with MS-SQL 2019 Standard (2023.02.14.)
    * Image update
    * Applied January 2023 security update: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022286-os-build-17763-3887-48683103-7b22-4f36-aa98-0049c7a6e579

<a id="february-28-2023-image-builder"></a>
### Image Builder { #february-28-2023-image-builder }
* Added new base images
    * Ubuntu 20.04
* Added application versions
    * CUBRID 10.2.10
    * CUBRID 11.0.10
    * MariaDB 10.6.11
* End of support for application versions
    * CUBRID 10.2.4
    * CUBRID 11.0.2

<a id="january-31-2023"></a>
## January 31, 2023 { #january-31-2023 }

<a id="january-31-2023-instance"></a>
### Instance { #january-31-2023-instance }
* Improved the UI to allow modification of settings when creating an instance from an **Instance Template**
* Improved the instance information UI

<a id="january-31-2023-instance-template"></a>
### Instance Template { #january-31-2023-instance-template }
* Added the **Change Instance Template Owner** feature

<a id="january-31-2023-auto-scale"></a>
### Auto Scale { #january-31-2023-auto-scale }
* Added the **Change Scaling Group Owner** feature
* Improved the UI to allow modification of settings when creating a scaling group from an **Instance Template**

<a id="december-27-2022"></a>
## December 27, 2022 { #december-27-2022 }

<a id="december-27-2022-image"></a>
### Image { #december-27-2022-image }
* Added new images
    * CentOS 7.9 with Apache Kafka 3.3.1 (2022. 12. 20.)
    * CentOS 7.9 with CUBRID 10.2.4 (2022. 12. 20.)
    * CentOS 7.9 with CUBRID 11.0.2 (2022. 12. 20.)
    * CentOS 7.9 with JEUS8Fix1 (Domain Administrator Server 2022. 12. 20.)
    * CentOS 7.9 with JEUS8Fix1 (Managed Server 2022. 12. 20.)
    * CentOS 7.9 with MariaDB 10.3.31 (2022. 12. 20.)
    * CentOS 7.9 with MySQL 5.7.35 (2022. 12. 20.)
    * CentOS 7.9 with MySQL 8.0.27 (2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 10.20 (2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 11.15 (2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 12.10 (2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 13.6 (2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 14.2 (2022. 12. 20.)
    * CentOS 7.9 with Redis 7.0.5 (2022. 12. 20.)
    * CentOS 7.9 with Tibero 6 (2022. 12. 20.)
    * CentOS 7.9 with WebtoB5Fix4 (2022. 12. 20.)
* End of image support
    * CentOS 7.8 (2021. 12. 21.)
    * CentOS 7.8 with CUBRID 10.2.4 (2021. 12. 21.)
    * CentOS 7.8 with CUBRID 11.0.2 (2021. 12. 21.)
    * CentOS 7.8 with JEUS8Fix1 (Domain Administrator Server 2022. 03. 22.)
    * CentOS 7.8 with JEUS8Fix1 (Managed Server 2022. 03. 22.)
    * CentOS 7.8 with MariaDB 10.3.31 (2022.11.4)
    * CentOS 7.8 with MySQL 5.7.20 (2021. 12. 21.)
    * CentOS 7.8 with MySQL 5.7.32 (2021. 12. 21.)
    * CentOS 7.8 with MySQL 8.0.22 (2021. 12. 21.)
    * CentOS 7.8 with PostgreSQL 10.20 (2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 11.15 (2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 12.10 (2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 13.6 (2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 14.2 (2022. 05. 17.)
    * CentOS 7.8 with Tibero 6 (2022. 01. 25.)
    * CentOS 7.8 with WebtoB5Fix4 (2022. 03. 22.)

<a id="december-27-2022-image-builder"></a>
### Image Builder { #december-27-2022-image-builder }
* Added new base images
    * CentOS 7.9
* End of support for base images
    * CentOS 7.8

<a id="november-29-2022"></a>
## November 29, 2022 { #november-29-2022 }
<a id="november-29-2022-instance"></a>
### Instance { #november-29-2022-instance }
* Added deletion protection (All/Enabled/Disabled) to the **filter conditions** in instance management
* Improved the feature for changing security groups configured per network interface
* Improved the instance information UI
* Added a deletion protection toggle button
* Improved the bulk deletion protection configuration feature

<a id="november-29-2022-image"></a>
### Image { #november-29-2022-image }
* Added new images
    * CentOS 7.9 (November 22, 2022)
    * CentOS 7.9 for NAT (November 22, 2022)
    * Rocky Linux 8.6 (November 22, 2022)
* End of image support
    * Rocky Linux 8.5 (May 17, 2022)
* Debian 10.13 Buster (November 22, 2022)
    * Image update
* Debian 11.5 Bullseye (November 22, 2022)
    * Image update
* Ubuntu Server 18.04.6 LTS (November 22, 2022)
    * Image update
* Ubuntu Server 20.04.5 LTS (November 22, 2022)
    * Image update
* Ubuntu Server 18.04.6 LTS for NAT (November 22, 2022)
    * Image update
* Ubuntu Server 18.04.6 LTS with NVIDIA (November 22, 2022)
    * Image update
* Windows 2012 R2 STD (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018474-monthly-rollup-21182931-4a5f-4085-a37b-2e63ac3c8c0a
* Windows 2016 STD (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2019 STD (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018419-os-build-17763-3532-ca62cca7-b599-44c4-a2a6-347996662623
* Windows 2022 STD (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018421-os-build-20348-1129-115b1147-9568-4924-83b8-d27ab5b495be
* Windows 2012 R2 STD with MS-SQL 2016 Standard (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD with MS-SQL 2016 Standard (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018474-monthly-rollup-21182931-4a5f-4085-a37b-2e63ac3c8c0a
* Windows 2016 STD with MS-SQL 2019 Express (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2016 STD with MS-SQL 2017 Standard (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2016 STD with MS-SQL 2019 Standard (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2019 STD with MS-SQL 2019 Standard (November 22, 2022)
    * End of support for Japanese image
    * Applied October 2022 security update: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018419-os-build-17763-3532-ca62cca7-b599-44c4-a2a6-347996662623

<a id="november-29-2022-image-builder"></a>
### Image Builder { #november-29-2022-image-builder }
* Added applications
    * Redis
    * Apache Kafka

<a id="november-4-2022"></a>
## November 4, 2022 { #november-4-2022 }
<a id="november-4-2022-image"></a>
### Image { #november-4-2022-image }
* CentOS 7.8 with MariaDB 10.3.31 (November 4, 2022)
    * Image update

<a id="november-4-2022-image-builder"></a>
### Image Builder { #november-4-2022-image-builder }
* Updated scripts
    * MariaDB

<a id="october-25-2022"></a>
## October 25, 2022 { #october-25-2022 }
<a id="october-25-2022-image"></a>
### Image { #october-25-2022-image }
* End of image support
    * CentOS 7.8 with MySQL 5.6.38 (December 21, 2021)
    * CentOS 7.8 with MySQL 5.6.50 (December 21, 2021)

<a id="september-27-2022"></a>
## September 27, 2022 { #september-27-2022 }
<a id="september-27-2022-image"></a>
### Image { #september-27-2022-image }
* Added new images
    * Windows 2022 STD (September 20, 2022)

* PLOS-WFK-KS-v4.0.6.61.25
    * Image update

<a id="july-26-2022"></a>
## July 26, 2022 { #july-26-2022 }
<a id="july-26-2022-instance"></a>
### Instance { #july-26-2022-instance }
* Added the ability to select instance types (Instance, Ephemeral Storage Instance) when creating an instance
* Added the ability to search by image type (OS, Application, DBMS, etc.) in instance management

<a id="july-26-2022-image"></a>
### Image { #july-26-2022-image }
* Changed the Windows image so that the password can be reset even if the Administrator account name is changed

* Windows 2012 R2 STD (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows 2019 STD (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-us/topic/april-12-2022-kb5012647-os-build-17763-2803-9a10c5c9-e65f-4ae1-a9c4-2db9a8eca4fc
* Windows 2012 R2 STD with MS-SQL 2016 Standard (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD with MS-SQL 2016 Standard (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows 2016 STD with MS-SQL 2019 Express (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
    * Applied SQL Server Cumulative Update 16: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896
* Windows 2016 STD with MS-SQL 2017 Standard (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows 2016 STD with MS-SQL 2019 Standard (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
    * Applied SQL Server Cumulative Update 16: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896
* Windows 2019 STD with MS-SQL 2019 Standard (July 19, 2022)
    * Applied May 2022 security update: https://support.microsoft.com/en-us/topic/april-12-2022-kb5012647-os-build-17763-2803-9a10c5c9-e65f-4ae1-a9c4-2db9a8eca4fc
    * Applied SQL Server Cumulative Update 16: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896

<a id="july-26-2022-system-monitoring"></a>
### System Monitoring { #july-26-2022-system-monitoring }
* Added new feature: Monthly Metric Report
  * You can create and download a monthly metric report.
  * You can generate a report for up to 6 months of metrics on a monthly basis.
  * `GENERAL` in the metric selection refers to metrics available on the **Server Dashboard**, and `PROMQL` refers to metrics available on the **OpenMetrics Dashboard**.
  * You can check each request in the **Monthly Metric Report**. Reports are available for download for one month after they are generated.

<a id="may-24-2022"></a>
## May 24, 2022 { #may-24-2022 }
<a id="may-24-2022-instance"></a>
### Instance { #may-24-2022-instance }
* Added the instance screenshot feature
* Added the instance deletion protection feature
* Changed the instance retrieval API to return the instance deletion protection attribute (`NHN-EXT-ATTR:protect`)
* Removed hyphens (`-`) from the names of multiple instances created at once
    * Before: instance-1, instance-2, ...
    * After: instance1, instance2, ...
* Improved the OS image selection UI when creating an instance

<a id="may-24-2022-image"></a>
### Image { #may-24-2022-image }
* Added new images
    * Rocky Linux 8.5 (May 17, 2022)

<a id="march-29-2022"></a>
## March 29, 2022 { #march-29-2022 }
<a id="march-29-2022-image"></a>
### Image { #march-29-2022-image }
* Added new images
    * Debian 11.2 Bullseye (March 22, 2022)

* End of image support
    * Debian 9.13 Stretch (December 21, 2021)

<a id="january-25-2022"></a>
## January 25, 2022 { #january-25-2022 }
<a id="january-25-2022-public-api"></a>
### Public API { #january-25-2022-public-api }
* Changed the image retrieval API to also return images for the GPU Instance service
* Added a query parameter to the image retrieval API for filtering by infrastructure service type

<a id="january-25-2022-image"></a>
### Image { #january-25-2022-image }
* Added the ability to replicate images to other regions

<a id="january-25-2022-image-builder"></a>
### Image Builder { #january-25-2022-image-builder }
* Added application
    * Slurm

<a id="december-28-2021"></a>
## December 28, 2021 { #december-28-2021 }

<a id="december-28-2021-image"></a>
### Image { #december-28-2021-image }
* Changed so that a Prometheus-compatible exporter is no longer automatically installed when creating an instance

* CentOS 7.8 (December 21, 2021)
    * Image update
* CentOS 7.8 for NAT (December 21, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.6.38 (December 21, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.6.50 (December 21, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.7.20 (December 21, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.7.32 (December 21, 2021)
    * Image update
* CentOS 7.8 with MySQL 8.0.22 (December 21, 2021)
    * Image update
* Debian 9.13 Stretch (December 21, 2021)
    * Image update
* Debian 10.11 Buster (December 21, 2021)
    * Image update
* Ubuntu Server 18.04.6 LTS (December 21, 2021)
    * Image update
* Ubuntu Server 20.04.3 LTS (December 21, 2021)
    * Image update
* Ubuntu Server 18.04.6 LTS for NAT (December 21, 2021)
    * Image update
* Ubuntu Server 18.04.6 LTS with NVIDIA (December 21, 2021)
    * Image update
* Windows 2012 R2 STD (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007247-monthly-rollup-2c3b6017-82f4-4102-b1e2-36f366bf3520
* Windows 2016 STD (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows 2019 STD (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007206-os-build-17763-2300-c63b76fa-a9b4-4685-b17c-7d866bb50e48
* Windows Server 2012 R2 with SQL Server 2016 Standard (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007247-monthly-rollup-2c3b6017-82f4-4102-b1e2-36f366bf3520
* Windows Server 2016 with SQL Server 2016 Standard (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2019 Express (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2017 Standard (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2019 Standard (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2019 with SQL Server 2019 Standard (December 21, 2021)
    * Applied November 2021 security update: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007206-os-build-17763-2300-c63b76fa-a9b4-4685-b17c-7d866bb50e48

<a id="december-28-2021-image-builder"></a>
### Image Builder { #december-28-2021-image-builder }
* Added application:
    * Deep Learning Framework

<a id="december-28-2021-system-monitoring"></a>
### System Monitoring { #december-28-2021-system-monitoring }
* Removed the feature to add @Linux and @Windows default workspaces, and deleted existing workspaces
    * The @Linux and @Windows workspaces that were previously added automatically when creating an instance are no longer added automatically.
    * All @Linux and @Windows workspaces that were automatically created for existing instances will be deleted.

<a id="november-23-2021"></a>
## November 23, 2021 { #november-23-2021 }
<a id="november-23-2021-image"></a>
### Image { #november-23-2021-image }
* Added support for creating private images that can be used to create GPU instances

<a id="november-23-2021-image-builder"></a>
### Image Builder { #november-23-2021-image-builder }
* Added applications:
    * JEUS
    * WebtoB
    * Apache Tomcat
    * Node.js
    * MySQL

<a id="october-26-2021"></a>
## October 26, 2021 { #october-26-2021 }
<a id="october-26-2021-image-builder"></a>
### Image Builder { #october-26-2021-image-builder }
* Added the Image Builder service
    * Create private images by combining OS images, application installation components, and user scripts
* Added applications:
    * PostgreSQL
    * MariaDB
    * CUBRID

<a id="october-26-2021-system-monitoring"></a>
### System Monitoring { #october-26-2021-system-monitoring }

* OpenMetrics Dashboard → View
    * Changed so that only dates up to one year in the past can be selected when choosing a query period
    * Changed so that a guidance message is displayed on the chart when there is no data or an error occurs
* OpenMetrics Dashboard → Add/Edit Chart
    * Changed so that clicking the **Add** button without selecting a metric displays a guidance message and highlights the relevant area

<a id="september-14-2021"></a>
## September 14, 2021 { #september-14-2021 }
<a id="september-14-2021-system-monitoring"></a>
### System Monitoring { #september-14-2021-system-monitoring }
- Added new APIs: added APIs for querying, adding, and deleting workspaces and collection targets
- Added @Linux and @Windows default workspaces
    - @Linux: Collects metrics from the node exporter installed on the instance. Instances running a Linux OS are automatically registered as collection targets for @Linux when created.
    - @Windows: Collects metrics from the Windows exporter installed on the instance. Instances running a Windows OS are automatically registered as collection targets for @Windows when created.

<a id="july-27-2021"></a>
## July 27, 2021 { #july-27-2021 }

<a id="july-27-2021-instance"></a>
### Instance { #july-27-2021-instance }
* Added support for creating instances using instance templates

<a id="july-27-2021-instance-template"></a>
### Instance Template { #july-27-2021-instance-template }
* Added the Instance Template service
    * Predefine and store frequently used instance component information as templates
    * Use user-defined templates to create instances or scaling groups

<a id="july-27-2021-auto-scale"></a>
### Auto Scale { #july-27-2021-auto-scale }
* Removed the Instance Template tab
    * Create scaling groups using templates created in the Instance Template service
* Added an option to select an automatic recovery policy

<a id="july-27-2021-system-monitoring"></a>
### System Monitoring { #july-27-2021-system-monitoring }

* Bug fix: Fixed an issue where 'There are no entires.' could be selected when adding servers or user groups to a notification group
* Bug fix: Fixed an issue where more than 5 Advanced Monitoring layouts could be created when creating them quickly
* Bug fix: Fixed an issue where a different instance with the same name on the same port could not be added as a collection target in **Advanced Monitoring → Workspace → Collection Targets**

<a id="june-29-2021"></a>
## June 29, 2021 { #june-29-2021 }

<a id="june-29-2021-image"></a>
### Image { #june-29-2021-image }

* Prometheus-compatible exporter
    * This tool is automatically installed when creating an instance to support Advanced Monitoring.

* CentOS 7.8 (June 22, 2021)
    * Image update
* CentOS 7.8 for NAT (June 22, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.6.38 (June 22, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.6.50 (June 22, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.7.20 (June 22, 2021)
    * Image update
* CentOS 7.8 with MySQL 5.7.32 (June 22, 2021)
    * Image update
* CentOS 7.8 with MySQL 8.0.22 (June 22, 2021)
    * Image update
* Debian 9.13 Stretch (June 22, 2021)
    * Image update
* Debian 10.9 Buster (June 22, 2021)
    * Image update
* Ubuntu Server 18.04.5 LTS (June 22, 2021)
    * Image update
* Ubuntu Server 18.04.5 LTS for NAT (June 22, 2021)
    * Image update
* Ubuntu Server 18.04.5 LTS with NVIDIA (June 22, 2021)
    * Image update
* Ubuntu Server 20.04.2 LTS (June 22, 2021)
    * Image update
* Windows 2012 R2 STD (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27
* Windows 2012 R2 STD with MS-SQL 2016 Standard (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD with MS-SQL 2016 Standard (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Express (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2017 Standard (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Standard (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD with MS-SQL 2019 Standard (June 22, 2021)
    * Applied May 2021 security update: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27

<a id="june-29-2021-system-monitoring"></a>
### System Monitoring { #june-29-2021-system-monitoring }

* Improved the input guide text for OpenMetrics alert groups
* Improved the tooltip size for server/agent status on the server dashboard
* Fixed an issue where some dropdown menu buttons were displayed abnormally on the event status screen
* Fixed an issue where instance names changed in **Compute → Instance** were not reflected in the server list on the server dashboard
* Updated the loading bar
* Added Prometheus-compatible API (beta)

<a id="april-27-2021"></a>
## April 27, 2021 { #april-27-2021 }

<a id="april-27-2021-image"></a>
### Image { #april-27-2021-image }

* Added new images (Pyeongchon region)
    * CentOS 7.8 for NAT (April 22, 2021)
    * Ubuntu Server 18.04.5 LTS for NAT (April 22, 2021)

* End of image support
    * Ubuntu Server 16.04.7 LTS (December 22, 2020)

<a id="february-23-2021"></a>
## February 23, 2021 { #february-23-2021 }

<a id="february-23-2021-image"></a>
### Image { #february-23-2021-image }

* Added new images
    * CentOS 7.8 with MySQL 5.6.38 (February 23, 2021)
    * CentOS 7.8 with MySQL 5.6.50 (February 23, 2021)
    * CentOS 7.8 with MySQL 5.7.20 (February 23, 2021)
    * CentOS 7.8 with MySQL 5.7.32 (February 23, 2021)
    * CentOS 7.8 with MySQL 8.0.22 (February 23, 2021)

* End of image support
    * CentOS 6.10 (December 22, 2020)
    * CentOS 7.5 (December 22, 2020)
    * CentOS Linux 6.10 with MySQL 5.6.38 (December 22, 2020)
    * CentOS Linux 6.10 with MySQL 5.7.20 (December 22, 2020)

* CentOS 7.8 (February 23, 2021)
    * Image update

* Applied Linux security vulnerability patches
    * Heap-based buffer overflow in Sudo (CVE-2021-3156)
    * Applied when creating new instances

<a id="january-26-2021"></a>
## January 26, 2021 { #january-26-2021 }

<a id="january-26-2021-system-monitoring"></a>
### System Monitoring { #january-26-2021-system-monitoring }
* Added new feature: Advanced Monitoring (OpenMetrics)
    * Provides OpenMetrics (Prometheus exposition format) metric collection, query, and alerting

<a id="december-29-2020"></a>
## December 29, 2020 { #december-29-2020 }

<a id="december-29-2020-image"></a>
### Image { #december-29-2020-image }
* CentOS 6.10 (December 22, 2020)
    * Updated image
* CentOS 7.5 (December 22, 2020)
    * Updated image
* CentOS 7.8 (December 22, 2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.6.38 (December 22, 2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.7.20 (December 22, 2020)
    * Updated image
* Debian 9.13 Stretch (December 22, 2020)
    * Updated image
* Debian 10.7 Buster (December 22, 2020)
    * Updated image
* Ubuntu Server 16.04.7 LTS (December 22, 2020)
    * Updated image
* Ubuntu Server 18.04.5 LTS (December 22, 2020)
    * Updated image
* Ubuntu Server 20.04.1 LTS (December 22, 2020)
    * Updated image
* Ubuntu Server 18.04.5 LTS with NVIDIA (December 22, 2020)
    * Updated image
* Windows 2012 R2 STD (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839
* Windows 2012 R2 STD with MS-SQL 2016 Standard (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD with MS-SQL 2016 Standard (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Express (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2017 Standard (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Standard (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD with MS-SQL 2019 Standard (December 22, 2020)
    * Applied November 2020 security update: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839

<a id="november-24-2020"></a>
## November 24, 2020 { #november-24-2020 }

<a id="november-24-2020-auto-scale"></a>
### Auto Scale { #november-24-2020-auto-scale }
* Added integration with the Deploy service

<a id="august-25-2020"></a>
## August 25, 2020 { #august-25-2020 }

<a id="august-25-2020-instance"></a>
### Instance { #august-25-2020-instance }
* Added a **Reset Password** button to the **Windows Instance Access Information** tab
* Added a feature to reset the password of the original instance when creating a Windows image

<a id="august-25-2020-image"></a>
### Image { #august-25-2020-image }
* Added new images
    * Cent OS 7.8 (August 18, 2020)
    * Ubuntu 20.04 LTS (August 18, 2020)
    * Windows 2016 STD with MS-SQL 2019 Express (August 18, 2020)
    * Windows 2016 STD with MS-SQL 2017 Standard (August 18, 2020)
    * Windows 2016 STD with MS-SQL 2019 Standard (August 18, 2020)
    * Windows 2019 STD with MS-SQL 2019 Standard (August 18, 2020)

* CentOS 6.10 (August 18, 2020)
    * Updated image
* CentOS 7.5 (August 18, 2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.6.38 (August 18, 2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.7.20 (August 18, 2020)
    * Updated image
* Debian 9.9 Stretch (August 18, 2020)
    * Updated image
* Debian 10.5 Buster (August 18, 2020)
    * Updated image
* Ubuntu Server 16.04.6 LTS (August 18, 2020)
    * Updated image
* Ubuntu Server 18.04.4 LTS (August 18, 2020)
    * Updated image
* Ubuntu Server 18.04.4 LTS with NVIDIA (August 18, 2020)
    * Updated image
* Windows 2012 R2 STD (August 18, 2020)
    * Updated image
* Windows 2016 STD (August 18, 2020)
    * Updated image
* Windows 2019 STD (August 18, 2020)
    * Updated image
* Windows 2012 R2 STD with MS-SQL 2016 Standard (August 18, 2020)
    * Updated image
* Windows 2016 STD with MS-SQL 2016 Standard (August 18, 2020)
    * Updated image

* End of image support
    * Windows 2012 R2 STD with MS-SQL 2012 Standard (February 18, 2020)
    * Windows 2012 R2 STD with MS-SQL 2014 Standard (February 18, 2020)
    * Windows 2012 R2 STD with MS-SQL 2016 Express (February 18, 2020)

<a id="june-23-2020"></a>
## June 23, 2020 { #june-23-2020 }

<a id="june-23-2020-system-monitoring"></a>
### System Monitoring { #june-23-2020-system-monitoring }

* Updated chart and legend names to more clearly represent their meaning
* Added a feature to display detailed charts for metrics that have sub-items

<a id="june-23-2020-instance"></a>
### Instance { #june-23-2020-instance }
* Added a feature to look up the public key registered in a key pair
* Opened the service to allow GPU instances to be created directly from the console
* Removed the **Delete** button from the **Stop Instance** dialog box

<a id="may-26-2020"></a>
## May 26, 2020 { #may-26-2020 }

<a id="may-26-2020-instance"></a>
### Instance { #may-26-2020-instance }

* Released Public API v2
    * Changed to OpenStack-compatible API specification
    * Added Terraform support

<a id="may-26-2020-image"></a>
### Image { #may-26-2020-image }

* Released Public API v2
    * Changed to OpenStack-compatible API specification

<a id="february-25-2020"></a>
## February 25, 2020 { #february-25-2020 }
<a id="february-25-2020-image"></a>
### Image { #february-25-2020-image }
* Changed the image list to display both personal images and shared images together
* Added new images
    * Debian 10.2 Buster (February 18, 2020)

* CentOS 6.10 (February 18, 2020)
    * Updated image
* CentOS 7.5 (February 18, 2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.6.38 (February 18, 2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.7.20 (February 18, 2020)
    * Updated image
* Debian 9.9 Stretch (February 18, 2020)
    * Updated image
* Ubuntu Server 16.04.2 LTS (February 18, 2020)
    * Updated image
* Ubuntu Server 18.04.2 LTS (February 18, 2020)
    * Updated image
* Windows 2012 R2 STD (February 18, 2020)
    * Applied December 2019 security update: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2012 Standard (February 18, 2020)
    * Applied December 2019 security update: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2014 Standard (February 18, 2020)
    * Applied December 2019 security update: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Express (February 18, 2020)
    * Applied December 2019 security update: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Standard (February 18, 2020)
    * Applied December 2019 security update: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2016 STD (February 18, 2020)
    * Applied December 2019 security update: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689
* Windows 2016 R2 STD with MS-SQL 2016 Standard (February 18, 2020)
    * Applied December 2019 security update: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689
* Windows 2019 STD (February 18, 2020)
    * Updated image

* End of image support
    * Debian 8.11 Jessie (July 23, 2019)

<a id="february-25-2020-system-monitoring"></a>
### System Monitoring { #february-25-2020-system-monitoring }
* Improved the event status page
    * Added the ability to view events by region
    * Added an **All** option to the status filter in event search
    * Added a **Force Stop** button that allows users to manually stop an event
* Improved the Agent
    * Optimized the communication path with the System Monitoring server
        * Metrics can now be collected regardless of internet gateway or security group settings
    * Improved CPU and memory usage

<a id="january-31-2020"></a>
## January 31, 2020 { #january-31-2020 }
<a id="january-31-2020-image"></a>
### Image { #january-31-2020-image }
* Added new images
    * Windows 2019 STD (January 31, 2020)

<a id="january-21-2020"></a>
## January 21, 2020 { #january-21-2020 }
<a id="january-21-2020-system-monitoring"></a>
### System Monitoring { #january-21-2020-system-monitoring }
* Added an event inquiry page
    * Added a feature to view events generated by configured **monitoring settings**
* Improved the **Server List** feature on the server dashboard
    * Updated to display all instances under **Compute → Instance**
    * Updated to display instance status accurately
* Improved the **Server and User Group Integration** feature in notification groups
    * Changed so that modifications are saved only after selecting a server and user group and clicking the **Save** button

<a id="december-17-2019"></a>
## December 17, 2019 { #december-17-2019 }
<a id="december-17-2019-auto-scale"></a>
### Auto Scale { #december-17-2019-auto-scale }
* Updated the instance template list and details to display all information entered at creation time
    * List table: availability zone
    * Details: all configured network information and user script content

<a id="november-26-2019"></a>
## November 26, 2019 { #november-26-2019 }
<a id="november-26-2019-auto-scale"></a>
### Auto Scale { #november-26-2019-auto-scale }
* Auto Scaling auto-recovery
    * Added a feature that automatically creates a new instance to replace a failed instance when a failure such as network disconnection occurs on an individual instance in a scaling group

<a id="november-26-2019-instance"></a>
### Instance { #november-26-2019-instance }
* Fixed an issue where an error occurred when certain special characters were entered while searching for instances by IP in the instance list

<a id="november-26-2019-system-monitoring"></a>
### System Monitoring { #november-26-2019-system-monitoring }
* Improved the instance search feature on the server dashboard: updated to be case-insensitive

<a id="october-29-2019"></a>
## October 29, 2019 { #october-29-2019 }
<a id="october-29-2019-image"></a>
### Image { #october-29-2019-image }
* PLOS-WFK-KS-v2.0.60.0.14 (October 22, 2019)
    * Fixed a display error for storage size on the WF-KS page

* Windows 2012 R2 STD (October 22, 2019)
    * Provided images by language (KO, EN, JP)
* Windows 2016 STD (October 22, 2019)
    * Provided images by language (KO, EN, JP)
* Windows 2012 R2 STD with MS-SQL 2012 Standard (October 22, 2019)
    * Provided images by language (KO, EN, JP)
* Windows 2012 R2 STD with MS-SQL 2014 Standard (October 22, 2019)
    * Provided images by language (KO, EN, JP)
* Windows 2012 R2 STD with MS-SQL 2016 Express (October 22, 2019)
    * Provided images by language (KO, EN, JP)
* Windows 2012 R2 STD with MS-SQL 2016 Standard (October 22, 2019)
    * Provided images by language (KO, EN, JP)
* Windows 2016 R2 STD with MS-SQL 2016 Standard (October 22, 2019)
    * Provided images by language (KO, EN, JP)

<a id="october-29-2019-system-monitoring"></a>
### System Monitoring { #october-29-2019-system-monitoring }
* Improved the user interaction UI
    * Updated to display a loading bar when viewing, adding, modifying, or deleting monitoring information such as user groups, monitoring groups, and monitoring settings
    * Updated to disable unnecessary buttons during interactions
* Fixed bugs in overseas regions
    * Fixed an issue where metric collection was temporarily interrupted for servers that had monitoring settings changed in the Japan and US regions
    * Fixed an issue where the creation and modification dates for user groups and monitoring groups were displayed incorrectly in the US region

<a id="vpc"></a>
### VPC { #vpc }
* Added the ability to delete the default VPC
    * Updated to allow users to delete the default VPC

<a id="september-24-2019"></a>
## September 24, 2019 { #september-24-2019 }
<a id="september-24-2019-system-monitoring"></a>
### System Monitoring { #september-24-2019-system-monitoring }
* Added English message support for the web console
* Fixed an issue where selecting a server dashboard layout failed in Internet Explorer 11

<a id="august-27-2019"></a>
## August 27, 2019 { #august-27-2019 }
<a id="august-27-2019-image"></a>
### Image { #august-27-2019-image }
* Removed the public image tab from the image management screen

* Windows 2012 R2 STD (August 27, 2019)
    * Applied July 10, 2019 security update: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2012 Standard (August 27, 2019)
    * Applied July 10, 2019 security update: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2014 Standard (August 27, 2019)
    * Applied July 10, 2019 security update: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2016 Express (August 27, 2019)
    * Applied July 10, 2019 security update: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2016 Standard (August 27, 2019)
    * Applied July 10, 2019 security update: https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448

* Windows 2016 STD (August 27, 2019)
    * Applied July 10, 2019 security update: https://support.microsoft.com/en-us/help/4507460/windows-10-update-kb4507460
* Windows 2016 R2 STD with MS-SQL 2016 Standard (August 27, 2019)
    * Applied July 10, 2019 security update: https://support.microsoft.com/en-us/help/4507460/windows-10-update-kb4507460

* End of OS image support
    * Windows 2012 R2 STD with MS-SQL 2008 R2 Standard

<a id="august-27-2019-system-monitoring"></a>
### System Monitoring { #august-27-2019-system-monitoring }
* Improved chart query performance on the server dashboard
* Improved the UI for Internet Explorer 11

<a id="july-23-2019"></a>
## July 23, 2019 { #july-23-2019 }
<a id="july-23-2019-system-monitoring"></a>
### System Monitoring { #july-23-2019-system-monitoring }
* Added the System Monitoring service
    * Provides system metric charts for created virtual servers
    * Allows you to arrange each system metric chart in a custom layout
    * Allows you to configure notifications to be sent to a specific user group when a metric reaches a certain threshold

<a id="june-25-2019"></a>
## June 25, 2019 { #june-25-2019 }
<a id="june-25-2019-instance"></a>
### Instance { #june-25-2019-instance }
* Updated to allow images to be created while an instance is running

<a id="may-28-2019"></a>
## May 28, 2019 { #may-28-2019 }
<a id="may-28-2019-auto-scale"></a>
### Auto Scale { #may-28-2019-auto-scale }
* Added a statistics graph for checking the usage of Scaling Groups

<a id="may-28-2019-image"></a>
### Image { #may-28-2019-image }
* CentOS 6.5(May 28, 2019)
    * Applied timezone changes based on region
* CentOS 6.10(May 28, 2019)
    * Applied timezone changes based on region
* CentOS 7.5(May 28, 2019)
    * Applied timezone changes based on region
* Debian 8.11 Jessie(May 28, 2019)
    * Applied timezone changes based on region
* Debian 9.9 Stretch(May 28, 2019)
    * Applied timezone changes based on region
* Ubuntu Server 16.04.6 LTS(May 28, 2019)
    * Applied timezone changes based on region
    * Kernel update: 4.4.0-142.168
* Ubuntu Server 18.04.2 LTS(May 28, 2019)
    * Applied timezone changes based on region

* Debian 9.9 Stretch(May 28, 2019)
    * Kernel update: 4.9.168-1

* Windows 2012 R2 STD(May 28, 2019)
    * Applied timezone changes based on region
    * Security update for May 14, 2019: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2008 R2 Standard(May 28, 2019)
    * Applied timezone changes based on region
    * Security update for May 14, 2019: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2012 Standard(May 28, 2019)
    * Applied timezone changes based on region
    * Security update for May 14, 2019: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2014 Standard(May 28, 2019)
    * Applied timezone changes based on region
    * Security update for May 14, 2019: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2016 Express(May 28, 2019)
    * Applied timezone changes based on region
    * Security update for May 14, 2019: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2016 Standard(May 28, 2019)
    * Applied timezone changes based on region
    * Security update for May 14, 2019: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151

* Windows 2016 STD(May 28, 2019)
    * Applied timezone changes based on region
    * Security update for May 14, 2019: https://support.microsoft.com/ko-kr/help/4498947/windows-10-update-kb4498947

* Added new images
    * Windows 2016 STD with MS-SQL 2016 Standard(May 28, 2019)


<a id="may-14-2019"></a>
## May 14, 2019 { #may-14-2019 }
<a id="may-14-2019-image"></a>
### Image { #may-14-2019-image }
* CentOS 6.10 with MySQL 5.6.38(May 14, 2019)
    * Image update
* CentOS 6.10 with MySQL 5.7.20(May 14, 2019)
    * Image update

* End of image support
    * CentOS 6.5
    * CentOS 7.1
    * Ubuntu 14.04
    * Windows 2008 R2 STD


<a id="april-25-2019"></a>
## April 25, 2019 { #april-25-2019 }
<a id="april-25-2019-auto-scale"></a>
### Auto Scale { #april-25-2019-auto-scale }
* Added timezone configuration when creating scheduled tasks

<a id="april-25-2019-image"></a>
### Image { #april-25-2019-image }
* CentOS 6.5(April 25, 2019)
    * Improved errors occurring during yum update
* CentOS 6.10(April 25, 2019)
    * Improved errors occurring during yum update
* CentOS 7.1(April 25, 2019)
    * Improved errors occurring during yum update
    * Changed time synchronization daemon (ntpd)
* CentOS 7.5(April 25, 2019)
    * Improved errors occurring during yum update
    * Changed time synchronization daemon (ntpd)

* Windows 2008 R2 STD(April 25, 2019)
    * Improved Windows Bootstrap process
* Windows 2012 R2 STD(April 25, 2019)
    * Improved Windows Bootstrap process
* Windows 2016 STD(April 25, 2019)
    * Improved Windows Bootstrap process
* Windows 2012 R2 STD with MS-SQL 2008 R2 Standard(April 25, 2019)
    * Improved Windows Bootstrap process
* Windows 2012 R2 STD with MS-SQL 2012 Standard(April 25, 2019)
    * Improved Windows Bootstrap process
* Windows 2012 R2 STD with MS-SQL 2014 Standard(April 25, 2019)
    * Improved Windows Bootstrap process
* Windows 2012 R2 STD with MS-SQL 2016 Express(April 25, 2019)
    * Improved Windows Bootstrap process
* Windows 2012 R2 STD with MS-SQL 2016 Standard(April 25, 2019)
    * Improved Windows Bootstrap process


<a id="march-26-2019"></a>
## March 26, 2019 { #march-26-2019 }
<a id="march-26-2019-image"></a>
### Image { #march-26-2019-image }
* CentOS 6.5(March 26, 2019)
    * Improved Bootstrap process
* CentOS 6.10(March 26, 2019)
    * Improved Bootstrap process
* CentOS 7.1(March 26, 2019)
    * Improved Bootstrap process
* CentOS 7.5(March 26, 2019)
    * Improved Bootstrap process
* CentOS 6.5 with MySQL 5.6.38(March 26, 2019)
    * Improved Bootstrap process
* CentOS 6.5 with MySQL 5.7.20(March 26, 2019)
    * Improved Bootstrap process
* Ubuntu Server 14.04.5 LTS(March 26, 2019)
    * Improved Bootstrap process
* Ubuntu Server 16.04.5 LTS(March 26, 2019)
    * Improved Bootstrap process
* Ubuntu Server 18.04.2 LTS(March 26, 2019)
    * Improved Bootstrap process
* Debian 8.11 Jessie(March 26, 2019)
    * Improved Bootstrap process
* Debian 9.8 Stretch(March 26, 2019)
    * Improved Bootstrap process
    * Kernel update: 4.9.144-3


<a id="february-26-2019"></a>
## February 26, 2019 { #february-26-2019 }
<a id="february-26-2019-image"></a>
### Image { #february-26-2019-image }
* Ubuntu Server 18.04.2 LTS(February 26, 2019)
    * Kernel update: 4.15.0-45
    * Fixed intermittent communication errors occurring when adding or removing a network interface or subnet


<a id="january-29-2019"></a>
## January 29, 2019 { #january-29-2019 }
<a id="january-29-2019-public-api"></a>
### Public API { #january-29-2019-public-api }
* Updated the Instance creation API to allow specifying a subnet
* Added query parameters for pagination to the Image retrieval API
* Added the Image delete API


<a id="december-27-2018"></a>
## December 27, 2018 { #december-27-2018 }

<a id="december-27-2018-image"></a>
### Image { #december-27-2018-image }
* Ubuntu Server 14.04.5 LTS(December 27, 2018)
    * Fixed an issue where an LC_CTYPE-related warning message appeared when using the tab auto-completion feature in the shell
        * Changed the default setting to "en_US.UTF-8"
        * Modified /etc/default/locale
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 16.04.5 LTS(December 27, 2018)
    * Fixed an issue where an LC_CTYPE-related warning message appeared when using the tab auto-completion feature in the shell
        * Changed the default setting to "en_US.UTF-8"
        * Modified /etc/default/locale
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 18.04.2 LTS(December 27, 2018)
    * Fixed an issue where an LC_CTYPE-related warning message appeared when using the tab auto-completion feature in the shell
        * Changed the default setting to "en_US.UTF-8"
        * Modified /etc/default/locale
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Debian 8.11 Jessie(March 26, 2019)
    * Fixed an issue where an LC_CTYPE-related warning message appeared when using the tab auto-completion feature in the shell
        * Changed the default setting to "en_US.UTF-8"
        * Modified /etc/default/locale
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Debian 9.8 Stretch(March 26, 2019)
    * Fixed an issue where an LC_CTYPE-related warning message appeared when using the tab auto-completion feature in the shell
        * Changed the default setting to "en_US.UTF-8"
        * Modified /etc/default/locale
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"


<a id="december-11-2018"></a>
## December 11, 2018 { #december-11-2018 }
<a id="december-11-2018-image"></a>
### Image { #december-11-2018-image }
* Fixed intermittent communication errors occurring when adding or removing a network interface or subnet
* Debian 8.11 Jessie(December 11, 2018)
    * Kernel update: 3.16-0-6
* Debian 9.6 Stretch(December 11, 2018)
    * Kernel update: 4.9.0-8

* CentOS 6.5(December 11, 2018)
    * Kernel update: 2.6.32-754
* CentOS 6.10(December 11, 2018)
    * Kernel update: 2.6.32-754
* CentOS 7.5(December 11, 2018)
    * Kernel update: 3.10.0-862
* CentOS 7.1(December 11, 2018)
    * Kernel update: 3.10.0-693

* Ubuntu Server 18.04.1 LTS(December 11, 2018)
    * Kernel update: 4.15.0-29
* Ubuntu Server 16.04.5 LTS(December 11, 2018)
    * Kernel update: 4.4.0-131
* Ubuntu Server 14.04.5 LTS(December 11, 2018)
    * Kernel update: 4.4.0-31


<a id="november-13-2018"></a>
## November 13, 2018 { #november-13-2018 }
<a id="november-13-2018-image"></a>
### Image { #november-13-2018-image }
* CentOS 6.5(November 13, 2018)
    * Kernel update: 2.6.32-754.6.3
    * Changed the Yum repository target to the latest repository
* CentOS 7.1(November 13, 2018)
    * Kernel update: 3.10.0-693.21.1
    * Changed the Yum repository target to the latest repository

<a id="october-23-2018"></a>
## October 23, 2018 { #october-23-2018 }
<a id="october-23-2018-image"></a>
### Image { #october-23-2018-image }
* CentOS 7.5 (2018. 10. 23.), CentOS 7.1 (2018. 10. 23.), CentOS 6.10 (2018. 10. 23.), CentOS 6.5 (2018. 10. 23.)
    * Password complexity settings: combination of numbers, English characters, and special characters, 8 or more characters (/etc/pam.d/common-password modified)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * SSH configuration changes (/etc/ssh/sshd_config modified)
        * PermitRootLogin no                # Disable root login
        * PasswordAuthentication no         # Disable password authentication
    * Kernel parameter changes to address vulnerabilities (/etc/sysctl.conf modified)
        * net.ipv4.conf.all.accept_redirects = 0 # Block ICMP redirect attacks
        * net.ipv4.conf.all.accept_source_route = 0 # Prevent IP spoofing by blocking source routing
        * net.ipv4.conf.all.log_martians = 1 # Log spoofing attempts
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # Defend against smurf DoS attacks
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # Ignore bad ICMP packets with corrupted IP or TCP headers
        * net.ipv4.tcp_syncookies=1 # Use SYN cookies to defend against SYN flooding attacks
    * Terminal access restrictions (/etc/securetty modified)
        * Access restricted to console, vc/1, vc/2, tty1, tty2, and ttyS0 only
    * Session termination after 120 minutes of no user input from the terminal (/etc/profile modified)
        * TMOUT=7200
    * All other settings follow CentOS Upstream
    * Root account login restricted to enhance access security
        * Before: SSH login with the root account was allowed
        * After: Log in with the general user account "centos" and then switch to root
    * No swap partition is created when an instance is created
    * User-added settings in the /etc/hosts file are preserved

* Ubuntu Server 16.04.5 LTS (2018. 10. 23.)
    * Password complexity settings: combination of numbers, English characters, and special characters, 8 or more characters (/etc/pam.d/common-password modified)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * SSH configuration changes (/etc/ssh/sshd_config modified)
        * PermitRootLogin no                # Disable root login
        * PasswordAuthentication no         # Disable password authentication
    * Kernel parameter changes to address vulnerabilities (/etc/sysctl.conf modified)
        * net.ipv4.conf.all.accept_redirects = 0 # Block ICMP redirect attacks
        * net.ipv4.conf.all.accept_source_route = 0 # Prevent IP spoofing by blocking source routing
        * net.ipv4.conf.all.log_martians = 1 # Log spoofing attempts
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # Defend against smurf DoS attacks
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # Ignore bad ICMP packets with corrupted IP or TCP headers
        * net.ipv4.tcp_syncookies=1 # Use SYN cookies to defend against SYN flooding attacks
    * Terminal access restrictions (/etc/securetty modified)
        * Access restricted to console, vc/1, vc/2, tty1, tty2, and ttyS0 only
    * Session termination after 120 minutes of no user input from the terminal (/etc/profile modified)
        * TMOUT=7200
    * All other settings follow Ubuntu Server 16.04 LTS Upstream
    * No swap partition is created when an instance is created
    * User-added settings in the /etc/hosts file are preserved

* Debian 9.5 Stretch (2018. 10. 23.), Debian 8.11 Jessie (2018. 10. 23.)
    * Password complexity settings: combination of numbers, English characters, and special characters, 8 or more characters (/etc/pam.d/common-password modified)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * SSH configuration changes (/etc/ssh/sshd_config modified)
        * PermitRootLogin no                # Disable root login
        * PasswordAuthentication no         # Disable password authentication
    * Kernel parameter changes to address vulnerabilities (/etc/sysctl.conf modified)
        * net.ipv4.conf.all.accept_redirects = 0 # Block ICMP redirect attacks
        * net.ipv4.conf.all.accept_source_route = 0 # Prevent IP spoofing by blocking source routing
        * net.ipv4.conf.all.log_martians = 1 # Log spoofing attempts
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # Defend against smurf DoS attacks
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # Ignore bad ICMP packets with corrupted IP or TCP headers
        * net.ipv4.tcp_syncookies=1 # Use SYN cookies to defend against SYN flooding attacks
    * Terminal access restrictions (/etc/securetty modified)
        * Access restricted to console, vc/1, vc/2, tty1, tty2, and ttyS0 only
    * Session termination after 120 minutes of no user input from the terminal (/etc/profile modified)
        * TMOUT=7200
    * All other settings follow Debian 9 Upstream
    * No swap partition is created when an instance is created
    * User-added settings in the /etc/hosts file are preserved


<a id="september-20-2018"></a>
## September 20, 2018 { #september-20-2018 }
<a id="september-20-2018-instance"></a>
### Instance { #september-20-2018-instance }
* Improved UX/UI of the instance management screen
    * Added instance name search
    * Added availability zone and instance status filters
* Improved features and UX/UI of the instance creation screen
    * Added an option to select whether to use a floating IP
    * Added security group creation and policy check features
    * Added additional block storage attachment feature
    * Added user script registration feature

<a id="september-20-2018-image"></a>
### Image { #september-20-2018-image }
* Fixed an issue where the user script feature was not applied correctly

* Ubuntu Server 18.04.1 LTS (2018. 09. 20.)
    * Kernel 4.15.0-29: Applied meltdown/spectre variant 1, 2, 3 (CVE-2017-5753, 5715, 5754) patches (retpoline)
    * Password complexity settings: combination of numbers, English characters, and special characters, 8 or more characters (/etc/pam.d/common-password modified)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * SSH configuration changes (/etc/ssh/sshd_config modified)
        * PermitRootLogin no                # Disable root login
        * PasswordAuthentication no         # Disable password authentication
    * Kernel parameter changes to address vulnerabilities (/etc/sysctl.conf modified)
        * net.ipv4.conf.all.accept_redirects = 0 # Block ICMP redirect attacks
        * net.ipv4.conf.all.accept_source_route = 0 # Prevent IP spoofing by blocking source routing
        * net.ipv4.conf.all.log_martians = 1 # Log spoofing attempts
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # Defend against smurf DoS attacks
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # Ignore bad ICMP packets with corrupted IP or TCP headers
        * net.ipv4.tcp_syncookies=1 # Use SYN cookies to defend against SYN flooding attacks
    * Terminal access restrictions (/etc/securetty modified)
        * Access restricted to console, vc/1, vc/2, tty1, tty2, and ttyS0 only
    * Session termination after 120 minutes of no user input from the terminal (/etc/profile modified)
        * TMOUT=7200
    * No swap partition is created when an instance is created (create one manually if needed)
    * All other settings follow Ubuntu Server 18.04 LTS upstream

* Added new images
    * Added Ubuntu Linux 14.04.5 (2018. 09. 20.)


<a id="august-9-2018"></a>
## August 9, 2018 { #august-9-2018 }
<a id="august-9-2018-image"></a>
### Image { #august-9-2018-image }
* Windows 2012 R2 STD (August 9, 2018)
    * Users who want to use Korean must install the Korean language pack manually (English version is provided by default).
    * Security update of July 10, 2018: https://support.microsoft.com/en-us/help/4338815/windows-81-update-kb4338815
    * Account management
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * Service management
        * NTP settings: 1.pool.ntp.org, time.windows.com
        * NTP synchronization interval: 256 seconds
    * System management
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled
        * Autologin restriction: AutoAdminLogon value set to 0

* Windows 2016 STD (August 9, 2018)
    * Security update of July 24, 2018: https://support.microsoft.com/en-us/help/4338822/windows-10-update-kb4338822
    * Account management
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * Service management
        * NTP settings: 1.pool.ntp.org, time.windows.com
        * NTP synchronization interval: 256 seconds
    * System management
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled

* Debian 9.4.0 (August 9, 2018)
    * Kernel 4.9 update: Meltdown/Spectre variant 1, 2, 3 (CVE-2017-5753, 5715, 5754) patch (retpoline)
    * Password complexity settings (combination of numbers, letters, and special characters + 8 or more characters): Added the following line to /etc/pam.d/common-password
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * Removed unnecessary accounts/groups
        * user: lp, sync, uucp, games
        * group: dip
    * Kernel parameter changes to protect against vulnerabilities (sysctl)
        * net.ipv4.conf.all.accept_redirects = 0 # Block ICMP redirect attacks
        * net.ipv4\.conf.all.accept_source_route = 0 # Prevent IP spoofing by blocking source routing
        * net.ipv4.conf.all.log_martians = 1 # Log spoofing attempts
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # Defend against Smurf DoS attacks
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # Ignore bad ICMP packets with corrupted IP or TCP headers
        * net.ipv4.tcp_syncookies=1 # Use SYN cookies to defend against SYN flooding attacks
    * SSH configuration changes
        * PermitRootLogin disabled
        * /etc/ssh/sshd_config set to immutable
    * Removed setuid/setgid
        * /usr/bin/chag
        * /usr/bin/gpasswd
        * /usr/bin/wall
        * /usr/bin/chfn
        * /usr/bin/chsh
        * /usr/bin/newgrp
        * /bin/mount
        * /bin/umount
        * /sbin/unix_chkpwd
    * Permission settings
        * /etc/passwd 644
        * /etc/hosts 644
        * /etc/rsyslog.conf 644
        * /etc/services 644
        * /etc/group 644
        * /etc/shadow 400
        * /etc/gshadow 400
        * /etc/login.defs 400
    * Terminal access restriction: Modified /etc/securetty
    * Profile additions (/etc/profile)
        * TMOUT=7200      # Terminate session when there is no user input from the terminal
        * HISTSIZE=500       # Limit the number of commands stored in the history list
        * HISTFILESIZE=0     # No commands saved to the history file
    * Removed pre-login system banner settings
        * Deleted /etc/issue and /etc/issue.net


<a id="july-16-2018"></a>
## July 16, 2018 { #july-16-2018 }
<a id="july-16-2018-image"></a>
### Image { #july-16-2018-image }
* Windows 2012 R2 STD (July 16, 2018)
    * Fixed an error that occurred when creating instances with antivirus software included using the Auto Scale feature
    * Changed CPU settings (maximum CPU socket count: 4)
    * Fixed the network interface speed to display as 10G

* Windows 2008 R2 STD (July 16, 2018)
    * Security update dated June 12, 2018: https://support.microsoft.com/ko-kr/help/4284826
    * Account management
        * Restricted Guest account use: changed to disable Guest account
        * Display last logged-in username: set to not display
        * Display user information when the session is locked: set to display username only
        * Password expiration change notification: set to notify 14 days before expiration
        * Restricted system shutdown by general users: set system shutdown policy to Administrator only
    * Service management
        * NTP settings: 1.pool.ntp.org, time.windows.com
        * NTP sync interval: 256 seconds
    * System management
        * Disabled anonymous enumeration of SAM accounts and shares: enabled the setting to disallow anonymous enumeration of SAM accounts
        * Restricted system shutdown without logon: set the allow system shutdown without logon policy to disabled
        * Restricted Autologin: set AutoAdminLogon value to 0

* Ubuntu 16.04.4 LTS (July 16, 2018)
    * Kernel 4.4.0-130: applied patches (retpoline) for meltdown/spectre variant 1, 2, 3 (CVE-2017-5753, 5715, 5754)
    * Password complexity settings (combination of numbers, letters, and special characters, 8 or more characters): added the following line to /etc/pam.d/common-password
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * Removed unnecessary accounts/groups
        * user: lp, sync, uucp, games
        * group: dip
    * Changed kernel parameters (sysctl) to address vulnerabilities
        * net.ipv4.conf.all.accept_redirects = 0 # block ICMP redirect attacks
        * net.ipv4\.conf.all.accept_source_route = 0 # prevent IP spoofing by blocking source routing
        * net.ipv4.conf.all.log_martians = 1 # log spoofing attempts
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # defend against smurf DoS attacks
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ignore bad ICMP packets with corrupted IP or TCP headers
        * net.ipv4.tcp_syncookies=1 # use SYN cookies to defend against SYN flooding attacks
    * Changed SSH settings
        * Disabled PermitRootLogin
        * Set /etc/ssh/sshd_config as immutable
    * Removed setuid/setgid
        * /usr/bin/chag
        * /usr/bin/gpasswd
        * /usr/bin/wall
        * /usr/bin/chfn
        * /usr/bin/chsh
        * /usr/bin/newgrp
        * /bin/mount
        * /bin/umount
        * /sbin/unix_chkpwd
    * Permission settings
        * /etc/passwd 644
        * /etc/hosts 644
        * /etc/rsyslog.conf 644
        * /etc/services 644
        * /etc/group 644
        * /etc/shadow 400
        * /etc/gshadow 400
        * /etc/login.defs 400
    * Restricted terminal access: modified /etc/securetty
    * Added profile settings (/etc/profile)
        * TMOUT=7200      # terminate session when there is no user input from the terminal
        * HISTSIZE=500       # limit the number of commands stored in the history list
        * HISTFILESIZE=0     # no commands stored in the history file
    * Removed pre-login system banner settings
        * Deleted /etc/issue and /etc/issue.net

<a id="may-29-2018"></a>
## May 29, 2018 { #may-29-2018 }
<a id="may-29-2018-auto-scale"></a>
### Auto Scale { #may-29-2018-auto-scale }
* Fixed errors related to recurring scheduled tasks (cron expression-based)
    * Fixed an error where recurring scheduled tasks ran based on UTC time
    * Fixed an error where the first execution of a recurring scheduled task did not follow the cron expression, but instead ran at the start time set when the scheduled task was created

<a id="may-29-2018-instance"></a>
### Instance { #may-29-2018-instance }
* Added the ability to set the volume type when creating an instance

<a id="april-24-2018"></a>
### April 24, 2018 { #april-24-2018 }
<a id="may-29-2018-instance-2"></a>
### Instance { #may-29-2018-instance-2 }
* Removed the view Windows instance log feature

<a id="march-22-2018"></a>
## March 22, 2018 { #march-22-2018 }
<a id="march-22-2018-auto-scale"></a>
### Auto Scale { #march-22-2018-auto-scale }
* Added the Auto Scale service
    * Creates a Scaling Group based on an Instance Template created by the user
    * Dynamically manages the number of instances in a Scaling Group based on instance status or scheduled tasks
    * For more information, see the guide documentation

<a id="february-22-2018"></a>
## February 22, 2018 { #february-22-2018 }
<a id="february-22-2018-instance"></a>
### Instance { #february-22-2018-instance }
* Changed instance creation to require a subnet to be specified, following the addition of the VPC feature

<a id="february-22-2018-image"></a>
### Image { #february-22-2018-image }
* Windows 2012 R2 STD (February 22, 2018)
    * Changed Windows Time Zone settings
        * Changed sync interval: [before] 604800 seconds (7 days) → [after] 256 seconds
        * Changed Time Zone Peer domain: [before] 1.kr.pool.ntp.org, 1.pool.ntp.org → [after] 1.pool.ntp.org, time.windows.com
    * Security update dated February 13, 2018: https://support.microsoft.com/ko-kr/help/4074594/windows-81-update-kb-4074594

* Ubuntu Linux 14.04.5 (February 22, 2018)
    * Kernel update to address vulnerability patches
        * Linux Kernel Version: 3.13.0-141
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched

* Debian Linux 8.2.0 (February 22, 2018)
    * Fixed the hostname to be set to the name specified when creating an instance
    * Kernel update to address vulnerability patches
        * Linux Kernel Version: 3.16.0-5
        * Variant 3 (CVE-2017-5754) - patched

* CentOS Linux 6.5 (February 22, 2018)
    * Fixed the hostname to be set to the name specified when creating an instance
    * Kernel update to address vulnerability patches
        * Linux Kernel Version: 2.6.32-696.20.1
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched

* CentOS Linux 7.1 (February 22, 2018)
    * Fixed the hostname to be set to the name specified when creating an instance
    * Changed the Firewall daemon default value
        * Changed the setting so that the Firewall daemon does not start automatically when the instance boots
    * Changed Swap Disk Mount settings
        * Changed the setting so that the swap partition is automatically mounted when a new instance is created
    * Kernel update to address vulnerability patches
        * Linux Kernel Version: 3.10.0-693.17.1
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched

* Added new images
    * CentOS Linux 6.5 with MySQL 5.6.38 (February 22, 2018)
        * MySQL 5.6.38 package installed
        * All other settings are the same as the CentOS Linux 6.5 image
    * CentOS Linux 6.5 with MySQL 5.7.20 (February 22, 2018)
        * MySQL 5.7.20 package installed
        * All other settings are the same as the CentOS Linux 6.5 image

<a id="september-21-2017"></a>
## September 21, 2017 { #september-21-2017 }
<a id="september-21-2017-public-api"></a>
### Public API { #september-21-2017-public-api }
* Added APIs for the TOAST Compute service
    * Currently, only a limited set of features is available; additional APIs will be added to expand functionality in the future
    * For supported APIs, see the guide documentation

<a id="september-21-2017-instance"></a>
### Instance { #september-21-2017-instance }
* Fixed a bug where an instance could be created without specifying a key pair

<a id="july-20-2017"></a>
## July 20, 2017 { #july-20-2017 }
<a id="july-20-2017-image"></a>
### Image { #july-20-2017-image }
* Fixed a bug where the creation of large images would intermittently fail to complete

<a id="august-24-2017"></a>
## August 24, 2017 { #august-24-2017 }
<a id="august-24-2017-instance"></a>
### Instance { #august-24-2017-instance }
* Added the instance flavor change feature
    * You can upgrade or downgrade the CPU/Memory while keeping the disk of the instance intact
    * Block storage size cannot be changed
    * The instance must be in a stopped state to change its flavor
    * For detailed constraints, see [Modify Instance Flavor](/Compute/Instance/en/console-guide/#modify-flavor) in the guide documentation
* Added the Low IOPS SSD flavor (U type)
    * Supports low-spec instances at a reasonable price
    * Supports Linux-based OS only
    * Because Local Disk is used, data recovery is not possible in the event of a hardware failure
* Added the High IOPS SSD flavor (I type)
    * Guarantees high IOPS (see the price list for guaranteed IOPS)
    * Supports Linux-based OS only
* Fixed a bug where values were not retrieved when querying instance usage

<a id="may-25-2017"></a>
## May 25, 2017 { #may-25-2017 }
<a id="may-25-2017-instance"></a>
### Instance { #may-25-2017-instance }
* Fixed a bug where instances created from end-of-service images were not displayed

<a id="may-25-2017-image"></a>
### Image { #may-25-2017-image }
* Updated Windows images
    * Added Windows 2012 R2 STD (May 25, 2017)

<a id="april-25-2017"></a>
## April 25, 2017 { #april-25-2017 }
<a id="april-25-2017-instance"></a>
### Instance { #april-25-2017-instance }
* Changed the maximum initial volume size when creating an instance from 600 GB to 1 TB (1,000 GB)

<a id="march-23-2017"></a>
## March 23, 2017 { #march-23-2017 }
<a id="march-23-2017-instance"></a>
### Instance { #march-23-2017-instance }
* Added the ability to specify the initial volume size when creating an instance
    * Creates the initial volume to the size specified by the user
    * The base disk size can be set from the minimum requirement for each image up to 600 GB

<a id="january-19-2017"></a>
## January 19, 2017 { #january-19-2017 }
<a id="january-19-2017-instance"></a>
### Instance { #january-19-2017-instance }
* Removed subnet names from the IP address information in the instance basic information
    * Prevents reduced readability caused by rows becoming too wide due to name display
* Restricted instance name length and special characters
    * Instance names must be 20 characters or fewer, and only alphanumeric characters, **.**  (dot), and **-** (dash) are allowed
* Changed the create instance feature to the create image feature
    * Changed to a feature consistent with the tab

<a id="january-19-2017-image"></a>
### Image { #january-19-2017-image }
* Fixed an issue where the image selection was not cleared when switching between image tabs (Private, Shared, Public)

<a id="december-22-2016"></a>
## December 22, 2016 { #december-22-2016 }
<a id="december-22-2016-instance"></a>
### Instance { #december-22-2016-instance }
* Changed to allow security group modification for stopped instances
* Changed to automatically select a security group when only one security group is available when creating an instance