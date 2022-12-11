===========================
1. GD32 SoC Series Overview
===========================

Below table list GD32 Series peripheral overview:

+------------+-----+----------+-------------------+
| Soc Series | HAL | FMC Type | pin-control model |
+============+=====+==========+===================+
| GD32A50x   | Y   | v2       | AF                |
+------------+-----+----------+-------------------+
| GD32E10x   | Y   | v1       | AFIO              |
+------------+-----+----------+-------------------+
| GD32E50x   | Y   | v1       | AFIO              |
+------------+-----+----------+-------------------+
| GD32F3x0   | Y   | v1       | AF                |
+------------+-----+----------+-------------------+
| GD32F403   | Y   | v2       | AFIO              |
+------------+-----+----------+-------------------+
| GD32F4xx   | Y   | v3       | AF                |
+------------+-----+----------+-------------------+
| GD32L23x   | Y   | v1       | AF                |
+------------+-----+----------+-------------------+
| GD32VF103  | Y   | v1       | AFIO              |
+------------+-----+----------+-------------------+
| GD32W51x   | N   | N        | AF                |
+------------+-----+----------+-------------------+
| GD32C10x   | N   | v1       | AFIO              |
+------------+-----+----------+-------------------+
| GD32C11x   | N   | v1       | AFIO              |
+------------+-----+----------+-------------------+
| GD32E11x   | N   | v1       | AFIO              |
+------------+-----+----------+-------------------+
| GD32E23x   | N   | v1       | AF                |
+------------+-----+----------+-------------------+
| GD32F10x   | N   | v2       | AFIO              |
+------------+-----+----------+-------------------+
| GD32F1x0   | N   | v1       | AF                |
+------------+-----+----------+-------------------+
| GD32F20x   | N   | v2       | AFIO              |
+------------+-----+----------+-------------------+
| GD32F30x   | N   | v2       | AFIO              |
+------------+-----+----------+-------------------+

======
2. FMC
======

Currently, Zephyr support three GD32 FMC, v1, v2 and v3.

----------
2.1 FMC v1
----------

This FMC's flash memory has 1 bank, page size is equal in the
bank, flash size is smaller than 512KB.

----------
2.2 FMC v2
----------

This FMC's flash memory has 2 banks. Page size equal within the
same bank but different between banks. Flash size can be up to 3072KB.
FMC v2 has two registers to control bank0 and bank1 separately.

----------
2.3 FMC v3
----------

This FMC's flash memory has 2 banks, use sector size as the
minimum operating unit, the sector size is not equal.

----------
2.4 Others
----------

GD32W51x series FMC support on Zephyr require new driver.

==========
3. PINCTRL
==========
There have two types pinctrl modes, AF model and AFIO model.

------------
3.1 AF Model
------------

Peripheral signals can be mapped separately.

--------------
3.2 AFIO Model
--------------

Peripheral signals need to mapped to simultaneously.
