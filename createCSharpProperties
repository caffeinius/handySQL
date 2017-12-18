use 'database';
declare @tableName nvarchar(50) = 'tableName';

select
'public ' +
(case
	when DATA_TYPE = 'int' then 'int'
	when DATA_TYPE = 'decimal' then 'decimal'
	when DATA_TYPE = 'numeric' then 'decimal'
	when DATA_TYPE = 'varchar' then 'string'
	when DATA_TYPE = 'datetime' then 'DateTime'
	ELSE DATA_TYPE
end) + ' '
 + COLUMN_NAME + ' { get; set; }'

 from Information_Schema.columns
	where TABLE_NAME = @tableName
