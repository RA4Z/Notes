To alter table SQLite tables in[[🐍Python]] and add or remove columns it's possible to use the following commands in terminal:
```Python
import sqlite3
conn = sqlite3.connect("automacoes.db")
cursor =conn.cursor()
cursor.execute("alter table automations add column fluxograma;")
conn.commit()
```