Interface TaxManagerInterface
=========================

A TaxManager define a way to retrieve tax.



* Interface name: TaxManagerInterface
* This is an **interface**
* Source: [classes/tax/TaxManagerInterface.php line 31](https://github.com/PrestaShop/PrestaShop/blob/1.5.6.2/classes/tax/TaxManagerInterface.php#L31)

Contents
--------



### Methods

* [getTaxCalculator](#method-getTaxCalculator)
* [isAvailableForThisAddress](#method-isAvailableForThisAddress)






Methods
-------


### <a name="method-getTaxCalculator"></a>getTaxCalculator

```php
\TaxCalculator TaxManagerInterface::getTaxCalculator()
```

Return the tax calculator associated to this address



* Visibility: **public**
* Source: [classes/tax/TaxManagerInterface.php line 48](https://github.com/PrestaShop/PrestaShop/blob/1.5.6.2/classes/tax/TaxManagerInterface.php#L48)




### <a name="method-isAvailableForThisAddress"></a>isAvailableForThisAddress

```php
\TaxManager TaxManagerInterface::isAvailableForThisAddress(\Address $address)
```

This method determine if the tax manager is available for the specified address.



* Visibility: **public**
* This method is **static**.
* Source: [classes/tax/TaxManagerInterface.php line 41](https://github.com/PrestaShop/PrestaShop/blob/1.5.6.2/classes/tax/TaxManagerInterface.php#L41)


#### Arguments
* $address **[Address](class.AddressCore.md)**


