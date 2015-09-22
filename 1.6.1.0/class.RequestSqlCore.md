Class RequestSqlCore
=====================





* Class name: RequestSqlCore
* Parent class: [ObjectModel](class.ObjectModelCore.md)
* Source: [classes/RequestSql.php line 27](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L27)


Contents
--------


### Properties

* [$attributes](#property-$attributes)
* [$definition](#property-$definition)
* [$error_sql](#property-$error_sql)
* [$name](#property-$name)
* [$sql](#property-$sql)
* [$tested](#property-$tested)

### Methods

* [attributExistInTable](#method-attributExistInTable)
* [checkedFrom](#method-checkedFrom)
* [checkedGroupBy](#method-checkedGroupBy)
* [checkedHaving](#method-checkedHaving)
* [checkedLimit](#method-checkedLimit)
* [checkedOrder](#method-checkedOrder)
* [checkedSelect](#method-checkedSelect)
* [checkedWhere](#method-checkedWhere)
* [cutAttribute](#method-cutAttribute)
* [cutJoin](#method-cutJoin)
* [getAttributesByTable](#method-getAttributesByTable)
* [getRequestSql](#method-getRequestSql)
* [getRequestSqlById](#method-getRequestSqlById)
* [getTables](#method-getTables)
* [parsingSql](#method-parsingSql)
* [returnNameTable](#method-returnNameTable)
* [testedRequired](#method-testedRequired)
* [testedUnauthorized](#method-testedUnauthorized)
* [validateParser](#method-validateParser)
* [validateSql](#method-validateSql)




Properties
----------


### <a name="property-$attributes"></a>$attributes

```php
public mixed $attributes = array('passwd' => '*******************', 'secure_key' => '*******************')
```





* Visibility: **public**
* Source: [classes/RequestSql.php line 68](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L68).


### <a name="property-$definition"></a>$definition

```php
public mixed $definition = array('table' => 'request_sql', 'primary' => 'id_request_sql', 'fields' => array('name' => array('type' => self::TYPE_STRING, 'validate' => 'isString', 'required' => true, 'size' => 200), 'sql' => array('type' => self::TYPE_SQL, 'validate' => 'isString', 'required' => true)))
```





* Visibility: **public**
* This property is **static**.
* Source: [classes/RequestSql.php line 35](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L35).


### <a name="property-$error_sql"></a>$error_sql

```php
public array $error_sql = array()
```





* Visibility: **public**
* Source: [classes/RequestSql.php line 74](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L74).


### <a name="property-$name"></a>$name

```php
public mixed $name
```





* Visibility: **public**
* Source: [classes/RequestSql.php line 29](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L29).


### <a name="property-$sql"></a>$sql

```php
public mixed $sql
```





* Visibility: **public**
* Source: [classes/RequestSql.php line 30](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L30).


### <a name="property-$tested"></a>$tested

```php
public array $tested = array('required' => array('SELECT', 'FROM'), 'option' => array('WHERE', 'ORDER', 'LIMIT', 'HAVING', 'GROUP', 'UNION'), 'operator' => array('AND', '&&', 'BETWEEN', 'AND', 'BINARY', '&', '~', '|', '^', 'CASE', 'WHEN', 'END', 'DIV', '/', '<=>', '=', '>=', '>', 'IS', 'NOT', 'NULL', '<<', '<=', '<', 'LIKE', '-', '%', '!=', '<>', 'REGEXP', '!', '||', 'OR', '+', '>>', 'RLIKE', 'SOUNDS', '*', '-', 'XOR', 'IN'), 'function' => array('AVG', 'SUM', 'COUNT', 'MIN', 'MAX', 'STDDEV', 'STDDEV_SAMP', 'STDDEV_POP', 'VARIANCE', 'VAR_SAMP', 'VAR_POP', 'GROUP_CONCAT', 'BIT_AND', 'BIT_OR', 'BIT_XOR'), 'unauthorized' => array('DELETE', 'ALTER', 'INSERT', 'REPLACE', 'CREATE', 'TRUNCATE', 'OPTIMIZE', 'GRANT', 'REVOKE', 'SHOW', 'HANDLER', 'LOAD', 'ROLLBACK', 'SAVEPOINT', 'UNLOCK', 'INSTALL', 'UNINSTALL', 'ANALZYE', 'BACKUP', 'CHECK', 'CHECKSUM', 'REPAIR', 'RESTORE', 'CACHE', 'DESCRIBE', 'EXPLAIN', 'USE', 'HELP', 'SET', 'DUPLICATE', 'VALUES', 'INTO', 'RENAME', 'CALL', 'PROCEDURE', 'FUNCTION', 'DATABASE', 'SERVER', 'LOGFILE', 'DEFINER', 'RETURNS', 'EVENT', 'TABLESPACE', 'VIEW', 'TRIGGER', 'DATA', 'DO', 'PASSWORD', 'USER', 'PLUGIN', 'FLUSH', 'KILL', 'RESET', 'START', 'STOP', 'PURGE', 'EXECUTE', 'PREPARE', 'DEALLOCATE', 'LOCK', 'USING', 'DROP', 'FOR', 'UPDATE', 'BEGIN', 'BY', 'ALL', 'SHARE', 'MODE', 'TO', 'KEY', 'DISTINCTROW', 'DISTINCT', 'HIGH_PRIORITY', 'LOW_PRIORITY', 'DELAYED', 'IGNORE', 'FORCE', 'STRAIGHT_JOIN', 'SQL_SMALL_RESULT', 'SQL_BIG_RESULT', 'QUICK', 'SQL_BUFFER_RESULT', 'SQL_CACHE', 'SQL_NO_CACHE', 'SQL_CALC_FOUND_ROWS', 'WITH'))
```





* Visibility: **public**
* Source: [classes/RequestSql.php line 45](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L45).


Methods
-------


### <a name="method-attributExistInTable"></a>attributExistInTable

```php
boolean RequestSqlCore::attributExistInTable($attr, $table)
```

Check if an attributes existe in an table



* Visibility: **public**
* Source: [classes/RequestSql.php line 318](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L318)


#### Arguments
* $attr **mixed**
* $table **mixed**



### <a name="method-checkedFrom"></a>checkedFrom

```php
boolean RequestSqlCore::checkedFrom($from)
```

Check a "FROM" sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 371](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L371)


#### Arguments
* $from **mixed**



### <a name="method-checkedGroupBy"></a>checkedGroupBy

```php
boolean RequestSqlCore::checkedGroupBy($group, $from)
```

Check a "GROUP BY" sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 613](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L613)


#### Arguments
* $group **mixed**
* $from **mixed**



### <a name="method-checkedHaving"></a>checkedHaving

```php
boolean RequestSqlCore::checkedHaving($having, $from)
```

Check a "HAVING" sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 526](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L526)


#### Arguments
* $having **mixed**
* $from **mixed**



### <a name="method-checkedLimit"></a>checkedLimit

```php
boolean RequestSqlCore::checkedLimit($limit)
```

Check a "LIMIT" sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 649](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L649)


#### Arguments
* $limit **mixed**



### <a name="method-checkedOrder"></a>checkedOrder

```php
boolean RequestSqlCore::checkedOrder($order, $from)
```

Check a "ORDER" sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 576](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L576)


#### Arguments
* $order **mixed**
* $from **mixed**



### <a name="method-checkedSelect"></a>checkedSelect

```php
boolean RequestSqlCore::checkedSelect($select, $from, boolean $in)
```

Check a "SELECT" sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 422](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L422)


#### Arguments
* $select **mixed**
* $from **mixed**
* $in **boolean**



### <a name="method-checkedWhere"></a>checkedWhere

```php
boolean RequestSqlCore::checkedWhere($where, $from, $sql)
```

Check a "WHERE" sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 472](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L472)


#### Arguments
* $where **mixed**
* $from **mixed**
* $sql **mixed**



### <a name="method-cutAttribute"></a>cutAttribute

```php
array|boolean RequestSqlCore::cutAttribute($attr, $from)
```

Cut an attribute with or without the alias



* Visibility: **public**
* Source: [classes/RequestSql.php line 245](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L245)


#### Arguments
* $attr **mixed**
* $from **mixed**



### <a name="method-cutJoin"></a>cutJoin

```php
array|boolean RequestSqlCore::cutJoin($attrs, $from)
```

Cut an join sentence



* Visibility: **public**
* Source: [classes/RequestSql.php line 223](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L223)


#### Arguments
* $attrs **mixed**
* $from **mixed**



### <a name="method-getAttributesByTable"></a>getAttributesByTable

```php
array RequestSqlCore::getAttributesByTable($table)
```

Get list of all attributes by an table



* Visibility: **public**
* Source: [classes/RequestSql.php line 211](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L211)


#### Arguments
* $table **mixed**



### <a name="method-getRequestSql"></a>getRequestSql

```php
array|boolean RequestSqlCore::getRequestSql()
```

Get list of request SQL



* Visibility: **public**
* This method is **static**.
* Source: [classes/RequestSql.php line 81](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L81)




### <a name="method-getRequestSqlById"></a>getRequestSqlById

```php
array RequestSqlCore::getRequestSqlById($id)
```

Get list of request SQL by id request



* Visibility: **public**
* This method is **static**.
* Source: [classes/RequestSql.php line 99](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L99)


#### Arguments
* $id **mixed**



### <a name="method-getTables"></a>getTables

```php
array RequestSqlCore::getTables()
```

Get list of all tables



* Visibility: **public**
* Source: [classes/RequestSql.php line 194](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L194)




### <a name="method-parsingSql"></a>parsingSql

```php
boolean RequestSqlCore::parsingSql($sql)
```

Call the parserSQL() method in Tools class
Cut the request in table for check it



* Visibility: **public**
* Source: [classes/RequestSql.php line 111](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L111)


#### Arguments
* $sql **mixed**



### <a name="method-returnNameTable"></a>returnNameTable

```php
array|boolean RequestSqlCore::returnNameTable(boolean $alias, $tables, $attr)
```

Get name of table by alias



* Visibility: **public**
* Source: [classes/RequestSql.php line 279](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L279)


#### Arguments
* $alias **boolean**
* $tables **mixed**
* $attr **mixed**



### <a name="method-testedRequired"></a>testedRequired

```php
boolean RequestSqlCore::testedRequired($tab)
```

Check if all required sentence existing



* Visibility: **public**
* Source: [classes/RequestSql.php line 337](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L337)


#### Arguments
* $tab **mixed**



### <a name="method-testedUnauthorized"></a>testedUnauthorized

```php
boolean RequestSqlCore::testedUnauthorized($tab)
```

Check if an unauthorized existing in an array



* Visibility: **public**
* Source: [classes/RequestSql.php line 354](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L354)


#### Arguments
* $tab **mixed**



### <a name="method-validateParser"></a>validateParser

```php
boolean RequestSqlCore::validateParser($tab, boolean $in, $sql)
```

Check if the parsing of the SQL request is good or not



* Visibility: **public**
* Source: [classes/RequestSql.php line 124](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L124)


#### Arguments
* $tab **mixed**
* $in **boolean**
* $sql **mixed**



### <a name="method-validateSql"></a>validateSql

```php
boolean RequestSqlCore::validateSql($tab, $in, $sql)
```

Cut the request for check each cutting



* Visibility: **public**
* Source: [classes/RequestSql.php line 148](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/RequestSql.php#L148)


#### Arguments
* $tab **mixed**
* $in **mixed**
* $sql **mixed**

