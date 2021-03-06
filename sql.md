# SQL Statements to use

### table creation

```sql
CREATE TABLE geoloc_storage(
    client_uuid VARCHAR(36) NOT NULL PRIMARY KEY, 
    lattitude REAL NOT NULL,
    longitude REAL NOT NULL, 
    refresh TIMESTAMP NOT NULL, 
    notes TEXT
    );
``````

### insert new client into table

```sql
INSERT INTO geoloc_storage 
VALUES("{UUID}", {LATT}, {LONG}, {TIME_UTC}, "{NOTES}");
```

### update fields (lattitude, longitude, update-timestamp)

```sql
UPDATE geoloc_storage 
SET lattitude={LATT}, longitude={LONG}, refresh={TIME_UTC}
WHERE client_uuid="{UUID}"
```

### update fields (lattitude, longitude, update-timestamp,  notes)

```sql
UPDATE geoloc_storage 
SET lattitude={LATT}, longitude={LONG}, utc_refresh_timestamp={TIME_UTC}, notes
WHERE client_uuid="{UUID}"
```

### delete client (uuid)

```sql
DELETE FROM geoloc_storage
WHERE client_uuid="{UUID}"
```
# Postgres
username+pw

