---
title: mybatis常用jdbctype
keywords: [mybatis常用jdbctype]
date: 2017/3/10 18:13
tags: [java,mybatis]
categories: java
---
Mybatis中javaType和jdbcType对应关系

| JDBC Type | Java Type | 
|:-----|:-----|       
| CHAR | String  
| VARCHAR | String  
| LONGVARCHAR | String  
| NUMERIC | java.math.BigDecimal  
| DECIMAL | java.math.BigDecimal  
| BIT | boolean  
| BOOLEAN | boolean  
| TINYINT | byte  
| SMALLINT | short  
| INTEGER | int  
| BIGINT | long  
| REAL | float  
| FLOAT | double  
| DOUBLE | double  
| BINARY | byte[]  
| VARBINARY | byte[]  
| LONGVARBINARY | byte[]  
| DATE | java.sql.Date  
| TIME | java.sql.Time  
| TIMESTAMP | java.sql.Timestamp  
| CLOB | Clob  
| BLOB | Blob  
| ARRAY | Array  
| DISTINCT | mapping of underlying type  
| STRUCT | Struct  
| REF | Ref  
| DATALINK | java.net.URL