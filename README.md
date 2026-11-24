# iec61499-mgmt-py
A Python client for the IEC 61499 management protocol of Eclipse 4diac FORTE: create, connect, write, read and query function blocks online; boot files.

```powershell
python -m pip install -e ".[test]"
python -m pytest
iec61499 --help            # deployment plans, type libraries and boot files (offline); only `types` contacts a FORTE
```

```python
from iec61499_mgmt.protocol import Client
with Client("localhost", 61499) as forte:
    ...                     # the management commands (CREATE, START, QUERY, ...) of FORTE's protocol
```

Used by [modsync](https://github.com/AAU-AASPIRE/modsync) to change a running module online and by
[modreg](https://github.com/AAU-AASPIRE/modreg) to read what runs. Part of
[AASPIRE](https://github.com/AAU-AASPIRE/aaspire).
