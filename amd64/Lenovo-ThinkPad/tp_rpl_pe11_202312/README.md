> [!NOTE]
> Vendor Published Drivers

---

# Lenovo

---

| Released | File | Package | Rev. | Download |
|--|--|--|--|--
| 2023.12.15 | tp_rpl_pe11_202312.exe | 03 | 01 | https://download.lenovo.com/pccbbs/mobiles/tp_rpl_pe11_202312.exe |

---

## Changelog
```
2025.01.08 - Michael Escamilla updated Drivers to the latest version.
```

---

## Notes
Drivers are imported into MDT (Microsoft Deployment Toolkit) to normalize the Driver folder structure and to validate the Driver content before adding to this Repository.

```
Download the latest DriverPack.
Execute the DriverPack to a temporary folder.
  [driverpackage.exe] "/VERYSILENT /DIR=[extractiondir] /EXTRACT=YES"
Import Drivers into an empty MDT Deployment Share.
Save the MDT Import Drivers output as .\HP\ImportDrivers.txt.
Copy the MDT Drivers in "<Deployment Share>\Out-of-Box Drivers" to .\Lenovo-<FormFactor>\<DriverPackName>\MDT\*.*.
Copy "<Deployment Share>\Control\Drivers.xml" as .\Lenovo-<FormFactor>\<DriverPackName>\Drivers.xml.
In MDT Out-of-Box Drivers, run the Export List. Save the file as .\Lenovo-<FormFactor>\<DriverPackName>\ExportList.csv.
```
---

## Links
- SCCM package for Windows PE 11, 10 (64-bit) - ThinkPad
  - https://support.lenovo.com/us/en/downloads/DS561550

---

## Lenovo Description:
This package provides the device drivers in .inf form for ThinkPad computers, in order to allow you to deploy Windows images with Microsoft System Center Configuration Manager(SCCM) by importing the device drivers.INF file will be available after executing the downloaded self-extracting EXE package.

## Lenovo Notes:
Support models (Intel RaptorLake)
* ThinkPad X1 Carbon Gen 11 (Machine Types: 21HM, 21HN)
* ThinkPad X1 Yoga Gen 8 (Machine Types: 21HQ, 21HR)
* ThinkPad X1 Nano Gen 3 (Machine Types: 21K1, 21K2)
* ThinkPad P1 Gen 6 (Machine Types: 21FV, 21FW)

Operating System   Microsoft Windows PE 11

## Summary Of Changes
Package 03    Rev 01    2023/12/13
---
- Added support for Lenovo USB3.0 LAN Driver for Docks and Adapter Driver

| Software name | Build ID | Version number
|--|--|--
| Lenovo USB3.0 LAN Driver for Docks and Adapters Driver  | U3ETN10W | 11.13.0420.2023 (Win11 LAN Driver for ARM)     (Added)
|--|--| 11.13.0420.2023 (Win11 LAN Driver for Intel and AMD)
|--|--| 10.59.0420.2023 (Win 10 Intel and AMD)
|--|--| 7.62.0211.2022  (Win 7 Intel and AMD)
|--|--| Device Manager: 1153.13.0420.2023 for Win11 x64 and arm(1G Ethernet)
|--|--| 1156.13.0420.2023 for Win11 x64 and arm(2.5G Ethernet)
|--|--| 10.59.0420.2023 (Win10 LAN Driver for Intel and AMD)
|--|--| 7.62.0211.2022  (Win7 LAN Driver for Intel and AMD)

Package 02    Rev 01    2023/07/24  Initial Releas
---
- Added support for ThinkPad  P1 Gen 6

| Software name | Build ID | Version number
|--|--|--
| Intel Rapid Storage Technology Driver | N3ZIO02W | 19.5.3.1050 (Added)

Package 01    Rev 01    2023/03/10  Initial Release
---
| Software name | Build ID | Version number
|--|--|--
| Intel Serial IO Driver | N3XLI03W | 30.100.2237.26 (Added)


## TradeMarks
* Lenovo, ThinkPad, ThinkVantage and UltraNav are registered trademarks of Lenovo.
* Intel is a registered trademark of Intel Corporation.
* Microsoft and Windows are registered trademarks of Microsoft Corporation.

Other company, product, and service names may be registered trademarks, trademarks or service marks of
others.