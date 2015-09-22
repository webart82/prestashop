Class ModuleGraphEngineCore
=====================





* Class name: ModuleGraphEngineCore
* This is an **abstract** class
* Parent class: [Module](class.ModuleCore)
* Source: [classes/module/ModuleGraphEngine.php line 27](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L27)



Properties
----------

* [$_type](#property-$_type)

Methods
-------
* [__construct](#method-__construct)
* [createValues](#method-createValues)
* [draw](#method-draw)
* [getGraphEngines](#method-getGraphEngines)
* [install](#method-install)
* [setLegend](#method-setLegend)
* [setSize](#method-setSize)
* [setTitles](#method-setTitles)




Properties
----------


### <a name="property-$_type"></a>$_type

    protected mixed $_type





* Visibility: **protected**
* Source: [classes/module/ModuleGraphEngine.php line 29](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L29)


Methods
-------


### <a name="method-__construct"></a>__construct

    mixed ModuleGraphEngineCore::__construct($type)





* Visibility: **public**
* Source: [classes/module/ModuleGraphEngine.php line 31](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L31)


#### Arguments
* $type **mixed**



### <a name="method-createValues"></a>createValues

    mixed ModuleGraphEngineCore::createValues($values)





* Visibility: **public**
* This method is **abstract**.
* Source: [classes/module/ModuleGraphEngine.php line 66](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L66)


#### Arguments
* $values **mixed**



### <a name="method-draw"></a>draw

    mixed ModuleGraphEngineCore::draw()





* Visibility: **public**
* This method is **abstract**.
* Source: [classes/module/ModuleGraphEngine.php line 70](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L70)




### <a name="method-getGraphEngines"></a>getGraphEngines

    mixed ModuleGraphEngineCore::getGraphEngines()





* Visibility: **public**
* This method is **static**.
* Source: [classes/module/ModuleGraphEngine.php line 44](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L44)




### <a name="method-install"></a>install

    mixed ModuleGraphEngineCore::install()





* Visibility: **public**
* Source: [classes/module/ModuleGraphEngine.php line 36](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L36)




### <a name="method-setLegend"></a>setLegend

    mixed ModuleGraphEngineCore::setLegend($legend)





* Visibility: **public**
* This method is **abstract**.
* Source: [classes/module/ModuleGraphEngine.php line 68](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L68)


#### Arguments
* $legend **mixed**



### <a name="method-setSize"></a>setSize

    mixed ModuleGraphEngineCore::setSize($width, $height)





* Visibility: **public**
* This method is **abstract**.
* Source: [classes/module/ModuleGraphEngine.php line 67](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L67)


#### Arguments
* $width **mixed**
* $height **mixed**



### <a name="method-setTitles"></a>setTitles

    mixed ModuleGraphEngineCore::setTitles($titles)





* Visibility: **public**
* This method is **abstract**.
* Source: [classes/module/ModuleGraphEngine.php line 69](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.1/classes/module/ModuleGraphEngine.php#L69)


#### Arguments
* $titles **mixed**

