# Apache NiFi

# DWH ETL SCD Type 1 [Batch] [Hive] [Parquet]

Esta plantilla está pensada para realizar extracciones de datos en origen (el caso de uso en el que se basa la plantilla el origen es HIVE), transformaciones, y carga obteniendo ficheros PARQUET que compondrán la tabla destino.

Tiene implementando control de errores que se necesitaría configurar mediante una tabla de logs en una base de datos auxiliar.

El flujo real para este caso de uso corre sobre un Cloudera Flow Management (Apache NiFi Empresarial) y es orquestado externamente, esta plantilla ha sido adaptada para Apache NiFi eliminando los datos sensibles y utilizando el procesador SelectHiveQL ya que Apache NiFi a fecha de este commit no soporta el procesador SelectHive3QL disponible en Cloudera Flow Management.


![NiFi SCD-Type-1](https://i.ibb.co/DwXJk8j/Ni-Fi-SCD-Type-1.jpg)

![NiFi Filename Timestamp](https://i.ibb.co/bH8cV13/Filename.jpg)

![NiFi Hive Pool Query y Create](https://i.ibb.co/0CRKws2/Hive-Pool.jpg)

![NiFi Put Parquet](https://i.ibb.co/bPf1Lmm/Put-Parquet.jpg)

Actualización: Esta plantilla en el caso de uso real y productivo ha sufrido varias mejoras, en caso de necesitar ayuda en el diseño de una soluciona semejante puede solicitar la subida de la nueva solución.

