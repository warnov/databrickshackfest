Montando el blob storage en Databricks:

    dbutils.fs.mount(
      source = "wasbs://{YOUR CONTAINER NAME}@{YOUR STORAGE ACCOUNT NAME}.blob.core.windows.net/",
      mountPoint = "/mnt/mypath",
      extraConfigs = Map("fs.azure.account.key.{YOUR STORAGE ACCOUNT NAME}.blob.core.windows.net" -> "{YOUR STORAGE ACCOUNT ACCESS KEY}"))

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM1OTI3Mzc4Ml19
-->