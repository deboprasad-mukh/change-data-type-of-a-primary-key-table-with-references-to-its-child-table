# change-data-type-of-a-primary-key-table-with-references-to-its-child-table
there are few steps that you have to follow
I CHANGED DATATYPE OF A PRIMARY KEY NUMBER TO VARCHAR !!
*\drop all foreign key constraints
ALTER TABLE table_name
DROP CONSTRAINT constraint_name ;

*\drop primary key
ALTER TABLE table_name
DROP PRIMARY KEY;

*\drop primary key column

ALTER TABLE table_name DROP COLUMN column_name ;

*\add primary key column with constraints

ALTER TABLE table_name ADD column_name data_type constraint pk_p_p1 PRIMARY KEY;

*\modify all foreign key data type(same as pk) + create foreign key constraints

ALTER TABLE AccInfo MODIFY ac_num varchar(20)CONSTRAINT ai_ac_nu REFERENCES customer(ac_num);
means
ALTER TABLE table_name MODIFY column_name data_type CONSTRAINT constraint_name REFERENCES table_name(column_name);
