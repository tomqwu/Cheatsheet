
```sql
select * from v$resource_limit where resource_name in ('processes', 'sessions', 'transactions');
select count(1) from v$process;
alter system set PROCESSES=2000 scope = spfile;
alter system set db_files=2000 scope=spfile;
shutdown immediate;
show pdbs;
```
