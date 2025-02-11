# MySQL InnoDB file format in use

## Description
Prior to MySQL version 8, InnoDB had two file formats: Antelope and Barracuda. Barracuda is the preferred file format.
Starting with MySQL 8, the following InnoDB file format variables are deprecated:
- Innodb_file_format
- Innodb_file_format_check
- Innodb_file_format_max
- innodb_large_prefix

The purpose of file format variables was to ensure compatibility with tables created in previous versions of InnoDB in MySQL 5.1. Since MySQL 5.1 has reached the end of its product lifecycle, these options are no longer required.


## Rule
`SELECT * from performance_schema.global_variables where VARIABLE_NAME in ('innodb_file_format','innodb_file_format_max','innodb_data_file_path');`


## Resolution
Barracuda is the recommended file format, support for Antelope is removed from MySQL 8.

## Need more support from Percona?
Subscribe to Percona Platform to get database support with guaranteed SLAs or proactive database management services from the Percona team.

[Learn more :fontawesome-solid-paper-plane:](https://per.co.na/subscribe){ .md-button }
