## PostgresSql
增量字段：from_date
```sql
SELECT "dept_emp"."emp_no", "dept_emp"."dept_no", to_char("dept_emp"."from_date", 'YYYY-MM-DD HH24:MI:SS'), to_char("dept_emp"."to_date", 'YYYY-MM-DD HH24:MI:SS') FROM "employees"."public"."dept_emp" WHERE 1 = 1 and "dept_emp"."from_date" >= (now() - interval '7 days')
```

## Oracle
增量字段：ETL_DATE
```sql
SELECT "TB_CIS_CONSULT_DETAIL"."ID", "TB_CIS_CONSULT_DETAIL"."RECORD_ID", "TB_CIS_CONSULT_DETAIL"."CONSULT_SERIAL_NUMBER", "TB_CIS_CONSULT_DETAIL"."MEDICAL_INSTITUT_CODE", "TB_CIS_CONSULT_DETAIL"."CONSULT_DATE", "TB_CIS_CONSULT_DETAIL"."CONSULT_IDEA", "TB_CIS_CONSULT_DETAIL"."IDEA_SORT", "TB_CIS_CONSULT_DETAIL"."CONSULT_DOCTOR_CODE", "TB_CIS_CONSULT_DETAIL"."CONSULT_DOCTOR_NAME", "TB_CIS_CONSULT_DETAIL"."CONSULT_INSTITUT_CODE", "TB_CIS_CONSULT_DETAIL"."CONSULT_INSTITUT_NAME", "TB_CIS_CONSULT_DETAIL"."SECRECY_LEVEL", "TB_CIS_CONSULT_DETAIL"."REVISE_SIGN", "TB_CIS_CONSULT_DETAIL"."RESERVE1", "TB_CIS_CONSULT_DETAIL"."RESERVE2", "TB_CIS_CONSULT_DETAIL"."ETL_DATE", "TB_CIS_CONSULT_DETAIL"."STATUS", "TB_CIS_CONSULT_DETAIL"."CREATE_BY", "TB_CIS_CONSULT_DETAIL"."CREATE_DATE", "TB_CIS_CONSULT_DETAIL"."UPDATE_BY", "TB_CIS_CONSULT_DETAIL"."UPDATE_DATE", "TB_CIS_CONSULT_DETAIL"."COMMENTS" FROM "GZFY"."TB_CIS_CONSULT_DETAIL" WHERE 1 = 1 and "TB_CIS_CONSULT_DETAIL"."ETL_DATE" >= sysdate - 1
```

## Mysql
增量字段：create_date
```sql
SELECT `student`.`id`, `student`.`name`, `student`.`age`, `student`.`address`, cast(`student`.`create_date` as datetime) FROM `test`.`student` WHERE 1 = 1 and DATE_SUB(CURDATE(), INTERVAL 10 DAY) <= `student`.`create_date`
```

## Sqlserver
增量字段：IND_CREAT_TIME
```sql
SELECT [DH_INDICATORS].[PK_ID], [DH_INDICATORS].[IND_CODE], [DH_INDICATORS].[IND_NAME], [DH_INDICATORS].[IND_S_NAME], [DH_INDICATORS].[IND_DATA_TYPE], [DH_INDICATORS].[IND_TYPE], [DH_INDICATORS].[IND_SIGNIFICANCE], [DH_INDICATORS].[IND_DIR_CODE], [DH_INDICATORS].[IND_STATISTICS], [DH_INDICATORS].[IND_STA_DESCRIPTION], [DH_INDICATORS].[IND_TERM], [DH_INDICATORS].[IND_MDX], [DH_INDICATORS].[IND_APPLICANT], convert(NVARCHAR(120), [DH_INDICATORS].[IND_CREAT_TIME], 120), [DH_INDICATORS].[IND_DEPARTMENT], [DH_INDICATORS].[IND_AUDIT_PERSON], convert(NVARCHAR(120), [DH_INDICATORS].[IND_AUDIT_TIME], 120), convert(NVARCHAR(120), [DH_INDICATORS].[IND_START], 120), convert(NVARCHAR(120), [DH_INDICATORS].[IND_STOP], 120), [DH_INDICATORS].[IND_REMARK], [DH_INDICATORS].[CUBE_NAME], [DH_INDICATORS].[FORMULA_MDX], [DH_INDICATORS].[FILE_PATH], [DH_INDICATORS].[IND_CALCULATE_STRING], [DH_INDICATORS].[IND_CALCULATE] FROM [medicare_ZhuHaiJinWan].[dbo].[DH_INDICATORS] WHERE 1 = 1 and [DH_INDICATORS].[IND_CREAT_TIME] >= DATEADD(day, -10, getdate())
```