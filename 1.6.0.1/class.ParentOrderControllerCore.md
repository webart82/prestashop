Class ParentOrderControllerCore
=====================





* Class name: ParentOrderControllerCore
* Parent class: [FrontController](class.FrontControllerCore.md)
* Source: [controllers/front/ParentOrderController.php line 37](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L37)


Contents
--------


### Properties

* [$nbProducts](#property-$nbProducts)
* [$php_self](#property-$php_self)
* [$ssl](#property-$ssl)

### Methods

* [_assignAddress](#method-_assignAddress)
* [_assignCarrier](#method-_assignCarrier)
* [_assignPayment](#method-_assignPayment)
* [_assignSummaryInformations](#method-_assignSummaryInformations)
* [_assignWrappingAndTOS](#method-_assignWrappingAndTOS)
* [_checkFreeOrder](#method-_checkFreeOrder)
* [_processCarrier](#method-_processCarrier)
* [_setDefaultCarrierSelection](#method-_setDefaultCarrierSelection)
* [_updateMessage](#method-_updateMessage)
* [init](#method-init)
* [setDefaultCarrierSelection](#method-setDefaultCarrierSelection)
* [setMedia](#method-setMedia)
* [setNoCarrier](#method-setNoCarrier)
* [validateDeliveryOption](#method-validateDeliveryOption)




Properties
----------


### <a name="property-$nbProducts"></a>$nbProducts

```php
public mixed $nbProducts
```





* Visibility: **public**
* Source: [controllers/front/ParentOrderController.php line 42](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L42).


### <a name="property-$php_self"></a>$php_self

```php
public mixed $php_self = 'order'
```





* Visibility: **public**
* Source: [controllers/front/ParentOrderController.php line 40](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L40).


### <a name="property-$ssl"></a>$ssl

```php
public mixed $ssl = true
```





* Visibility: **public**
* Source: [controllers/front/ParentOrderController.php line 39](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L39).


Methods
-------


### <a name="method-_assignAddress"></a>_assignAddress

```php
mixed ParentOrderControllerCore::_assignAddress()
```





* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 383](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L383)




### <a name="method-_assignCarrier"></a>_assignCarrier

```php
mixed ParentOrderControllerCore::_assignCarrier()
```





* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 463](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L463)




### <a name="method-_assignPayment"></a>_assignPayment

```php
mixed ParentOrderControllerCore::_assignPayment()
```





* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 547](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L547)




### <a name="method-_assignSummaryInformations"></a>_assignSummaryInformations

```php
mixed ParentOrderControllerCore::_assignSummaryInformations()
```





* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 283](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L283)




### <a name="method-_assignWrappingAndTOS"></a>_assignWrappingAndTOS

```php
mixed ParentOrderControllerCore::_assignWrappingAndTOS()
```





* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 505](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L505)




### <a name="method-_checkFreeOrder"></a>_checkFreeOrder

```php
boolean ParentOrderControllerCore::_checkFreeOrder()
```

Check if order is free



* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 163](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L163)




### <a name="method-_processCarrier"></a>_processCarrier

```php
mixed ParentOrderControllerCore::_processCarrier()
```





* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 207](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L207)




### <a name="method-_setDefaultCarrierSelection"></a>_setDefaultCarrierSelection

```php
\number ParentOrderControllerCore::_setDefaultCarrierSelection(array $carriers)
```

Decides what the default carrier is and update the cart with it



* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 590](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L590)


#### Arguments
* $carriers **array**



### <a name="method-_updateMessage"></a>_updateMessage

```php
mixed ParentOrderControllerCore::_updateMessage($messageContent)
```





* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 175](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L175)


#### Arguments
* $messageContent **mixed**



### <a name="method-init"></a>init

```php
mixed ParentOrderControllerCore::init()
```

Initialize parent order controller



* Visibility: **public**
* Source: [controllers/front/ParentOrderController.php line 48](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L48)




### <a name="method-setDefaultCarrierSelection"></a>setDefaultCarrierSelection

```php
\number ParentOrderControllerCore::setDefaultCarrierSelection(array $carriers)
```

Decides what the default carrier is and update the cart with it



* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 575](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L575)


#### Arguments
* $carriers **array**



### <a name="method-setMedia"></a>setMedia

```php
mixed ParentOrderControllerCore::setMedia()
```





* Visibility: **public**
* Source: [controllers/front/ParentOrderController.php line 139](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L139)




### <a name="method-setNoCarrier"></a>setNoCarrier

```php
mixed ParentOrderControllerCore::setNoCarrier()
```

Set id_carrier to 0 (no shipping price)



* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 558](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L558)




### <a name="method-validateDeliveryOption"></a>validateDeliveryOption

```php
mixed ParentOrderControllerCore::validateDeliveryOption(array $delivery_option)
```

Validate get/post param delivery option



* Visibility: **protected**
* Source: [controllers/front/ParentOrderController.php line 271](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.1/controllers/front/ParentOrderController.php#L271)


#### Arguments
* $delivery_option **array**

