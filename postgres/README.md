# CMS SynPUFs to OMOP

Postgres dump of the [CMS SynPUFs data](https://data.cms.gov/collection/synthetic-medicare-enrollment-fee-for-service-claims-and-prescription-drug-event) that has been ingested into the [OMOP Common Data Model](https://github.com/OHDSI/CommonDataModel) V6.0.


- Dumped from database version 14.10  
- Dumped by `pg_dump` version 16.1

## How to use this data set?

Use the [pg_restore](https://www.postgresql.org/docs/14/app-pgrestore.html) command line tool for Postgres to restore this dataset into your Postgres instance.

Localhost:
```sql
$ createdb -T template0 newdb
$ pg_restore -d newdb synpuf_omop_db.sql
```

Remote host:
```sql
$ createdb -T template0 newdb
$ pg_restore -d newdb synpuf_omop_db.sql -h <hostname> -U <username> -W
Password: 
```

## Resources

 - OMOP GitHub: https://github.com/OHDSI/CommonDataModel
 - OMOP Table structure: https://ohdsi.github.io/CommonDataModel/
 - CMS SynPUFs docs: https://www.cms.gov/data-research/statistics-trends-and-reports/medicare-claims-synthetic-public-use-files
 - CMS SynPUFs data: https://data.cms.gov/collection/synthetic-medicare-enrollment-fee-for-service-claims-and-prescription-drug-event
