Montando el blob storage en Databricks:

    dbutils.fs.mount(
      source = "wasbs://{YOUR CONTAINER NAME}@{YOUR STORAGE ACCOUNT NAME}.blob.core.windows.net/",
      mountPoint = "/mnt/mypath",
      extraConfigs = Map("fs.azure.account.key.{YOUR STORAGE ACCOUNT NAME}.blob.core.windows.net" -> "{YOUR STORAGE ACCOUNT ACCESS KEY}"))

Crra
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk4NDI5Mjc0LDEzNTkyNzM3ODJdfQ==
-->