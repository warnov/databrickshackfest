Montando el blob storage en Databricks:

    dbutils.fs.mount(
      source = "wasbs://{YOUR CONTAINER NAME}@{YOUR STORAGE ACCOUNT NAME}.blob.core.windows.net/",
      mountPoint = "/mnt/mypath",
      extraConfigs = Map("fs.azure.account.key.{YOUR STORAGE ACCOUNT NAME}.blob.core.windows.net" -> "{YOUR STORAGE ACCOUNT ACCESS KEY}"))

Creando una tabla temporal con el contenido del archivo en el blob storage:

    %sql DROP  TABLE  IF  EXISTS radio_sample_data; CREATE  TABLE radio_sample_data USING  json OPTIONS ( path  "/mnt/mypath/{filename}.json" )

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDAyNTQ0MTU5XX0=
-->