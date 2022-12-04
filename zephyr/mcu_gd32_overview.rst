===========================
1. GD32 SoC Series Overview
===========================

Below table list GD32 Series peripheral overview:

+-----------------+----------+-------------------+
| GD32 SoC Series | FMC Type | pin-control model |
+=================+==========+===================+
| GD32A50x        | v2       | AF                |
+-----------------+----------+-------------------+
| GD32C10x        | v1       | AFIO              |
+-----------------+----------+-------------------+
| GD32C11x        | v1       | AFIO              |
+-----------------+----------+-------------------+
| GD32E10x        | v1       | AFIO              |
+-----------------+----------+-------------------+
| GD32E11x        | v1       | AFIO              |
+-----------------+----------+-------------------+
| GD32E23x        | v1       | AF                |
+-----------------+----------+-------------------+
| GD32E50x        | v1       | AFIO              |
+-----------------+----------+-------------------+
| GD32F10x        | v2       | AFIO              |
+-----------------+----------+-------------------+
| GD32F1x0        | v1       | AF                |
+-----------------+----------+-------------------+
| GD32F20x        | v2       | AFIO              |
+-----------------+----------+-------------------+
| GD32F30x        | v2       | AFIO              |
+-----------------+----------+-------------------+
| GD32F3x0        | v1       | AF                |
+-----------------+----------+-------------------+
| GD32F403        | v2       | AFIO              |
+-----------------+----------+-------------------+
| GD32F4xx        | v3       | AF                |
+-----------------+----------+-------------------+
| GD32L23x        | v1       | AF                |
+-----------------+----------+-------------------+
| GD32VF103       | v1       | AFIO              |
+-----------------+----------+-------------------+
| GD32W51x        | N/A      | AF                |
+-----------------+----------+-------------------+

===========
2. GD32 FMC
===========

Currently, Zephyr support three GD32 FMC, v1, v2 and v3.

---------------
2.1 GD32 FMC v1
---------------

This FMC's flash memory has 1 bank, page size is equal in the
bank, flash size is smaller than 512KB.

---------------
2.2 GD32 FMC v2
---------------

This FMC's flash memory has 2 banks. Page size equal within the
same bank but different between banks. Flash size can be up to 3072KB.
FMC v2 has two registers to control bank0 and bank1 separately.

---------------
2.3 GD32 FMC v3
---------------

This FMC's flash memory has 2 banks, use sector size as the
minimum operating unit, the sector size is not equal.

----------
2.4 Others
----------

GD32W51x series FMC support on Zephyr require new driver.
