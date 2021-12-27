# SQL Server

## Full-Text-Search check

Check whether the fts plugin is installed.

```sql
SELECT
	CASE FULLTEXTSERVICEPROPERTY('IsFullTextInstalled')
		WHEN 1 THEN 'Full-Text installed.'
		ELSE 'Full-Text is NOT installed.'
	END
;
```

*[source](https://stackoverflow.com/questions/6511167/full-text-search-installed-or-not)*
