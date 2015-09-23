Class AuthControllerCore
=====================





* Class name: AuthControllerCore
* Parent class: [FrontController](class.FrontControllerCore.md)
* Source: [controllers/front/AuthController.php line 27](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L27)


Contents
--------


### Properties

* [$create_account](#property-$create_account)
* [$id_country](#property-$id_country)
* [$php_self](#property-$php_self)
* [$ssl](#property-$ssl)

### Methods

* [assignAddressFormat](#method-assignAddressFormat)
* [assignCountries](#method-assignCountries)
* [assignDate](#method-assignDate)
* [displayAjax](#method-displayAjax)
* [init](#method-init)
* [initContent](#method-initContent)
* [postProcess](#method-postProcess)
* [processCustomerNewsletter](#method-processCustomerNewsletter)
* [processSubmitAccount](#method-processSubmitAccount)
* [processSubmitCreate](#method-processSubmitCreate)
* [processSubmitLogin](#method-processSubmitLogin)
* [sendConfirmationMail](#method-sendConfirmationMail)
* [setMedia](#method-setMedia)
* [updateContext](#method-updateContext)




Properties
----------


### <a name="property-$create_account"></a>$create_account

```php
protected boolean $create_account
```





* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 35](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L35).


### <a name="property-$id_country"></a>$id_country

```php
protected mixed $id_country
```





* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 36](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L36).


### <a name="property-$php_self"></a>$php_self

```php
public mixed $php_self = 'authentication'
```





* Visibility: **public**
* Source: [controllers/front/AuthController.php line 30](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L30).


### <a name="property-$ssl"></a>$ssl

```php
public mixed $ssl = true
```





* Visibility: **public**
* Source: [controllers/front/AuthController.php line 29](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L29).


Methods
-------


### <a name="method-assignAddressFormat"></a>assignAddressFormat

```php
mixed AuthControllerCore::assignAddressFormat()
```

Assign address var to smarty



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 209](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L209)




### <a name="method-assignCountries"></a>assignCountries

```php
mixed AuthControllerCore::assignCountries()
```

Assign countries var to smarty



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 191](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L191)




### <a name="method-assignDate"></a>assignDate

```php
mixed AuthControllerCore::assignDate()
```

Assign date var to smarty



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 167](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L167)




### <a name="method-displayAjax"></a>displayAjax

```php
mixed AuthControllerCore::displayAjax()
```

Run ajax process



* Visibility: **public**
* Source: [controllers/front/AuthController.php line 75](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L75)




### <a name="method-init"></a>init

```php
mixed AuthControllerCore::init()
```

Initialize auth controller



* Visibility: **public**
* Source: [controllers/front/AuthController.php line 42](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L42)




### <a name="method-initContent"></a>initContent

```php
mixed AuthControllerCore::initContent()
```

Assign template vars related to page content



* Visibility: **public**
* Source: [controllers/front/AuthController.php line 84](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L84)




### <a name="method-postProcess"></a>postProcess

```php
mixed AuthControllerCore::postProcess()
```

Start forms process



* Visibility: **public**
* Source: [controllers/front/AuthController.php line 236](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L236)




### <a name="method-processCustomerNewsletter"></a>processCustomerNewsletter

```php
mixed AuthControllerCore::processCustomerNewsletter(\Customer $customer)
```

Process the newsletter settings and set the customer infos.



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 348](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L348)


#### Arguments
* $customer **[Customer](class.CustomerCore.md)** - Reference on the customer Object.



### <a name="method-processSubmitAccount"></a>processSubmitAccount

```php
mixed AuthControllerCore::processSubmitAccount()
```

Process submit on an account



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 364](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L364)




### <a name="method-processSubmitCreate"></a>processSubmitCreate

```php
mixed AuthControllerCore::processSubmitCreate()
```

Process submit on a creation



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 659](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L659)




### <a name="method-processSubmitLogin"></a>processSubmitLogin

```php
mixed AuthControllerCore::processSubmitLogin()
```

Process login



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 251](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L251)




### <a name="method-sendConfirmationMail"></a>sendConfirmationMail

```php
boolean AuthControllerCore::sendConfirmationMail(\Customer $customer)
```

sendConfirmationMail



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 705](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L705)


#### Arguments
* $customer **[Customer](class.CustomerCore.md)**



### <a name="method-setMedia"></a>setMedia

```php
mixed AuthControllerCore::setMedia()
```

Set default medias for this controller



* Visibility: **public**
* Source: [controllers/front/AuthController.php line 57](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L57)




### <a name="method-updateContext"></a>updateContext

```php
mixed AuthControllerCore::updateContext(\Customer $customer)
```

Update context after customer creation



* Visibility: **protected**
* Source: [controllers/front/AuthController.php line 681](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.13/controllers/front/AuthController.php#L681)


#### Arguments
* $customer **[Customer](class.CustomerCore.md)** - Created customer

