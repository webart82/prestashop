Class StockManagerCore
=====================

StockManager : implementation of StockManagerInterface



* Class name: StockManagerCore
* Source: [classes/stock/StockManager.php line 31](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L31)
* This class implements: [StockManagerInterface](interface.StockManagerInterface.md)

Contents
--------



### Methods

* [addProduct](#method-addProduct)
* [calculateWA](#method-calculateWA)
* [getProductCoverage](#method-getProductCoverage)
* [getProductPhysicalQuantities](#method-getProductPhysicalQuantities)
* [getProductRealQuantities](#method-getProductRealQuantities)
* [getStockCollection](#method-getStockCollection)
* [isAvailable](#method-isAvailable)
* [removeProduct](#method-removeProduct)
* [transferBetweenWarehouses](#method-transferBetweenWarehouses)






Methods
-------


### <a name="method-addProduct"></a>addProduct

```php
mixed StockManagerCore::addProduct($id_product, $id_product_attribute, \Warehouse $warehouse, $quantity, $id_stock_mvt_reason, $price_te, $is_usable, $id_supply_order)
```

For a given product, adds a given quantity



* Visibility: **public**
* Source: [classes/stock/StockManager.php line 46](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L46)


#### Arguments
* $id_product **mixed**
* $id_product_attribute **mixed**
* $warehouse **[Warehouse](class.WarehouseCore.md)**
* $quantity **mixed**
* $id_stock_mvt_reason **mixed**
* $price_te **mixed**
* $is_usable **mixed**
* $id_supply_order **mixed**



### <a name="method-calculateWA"></a>calculateWA

```php
integer StockManagerCore::calculateWA(\Stock $stock, integer $quantity, float $price_te)
```

For a given stock, calculates its new WA(Weighted Average) price based on the new quantities and price
Formula : (physicalStock * lastCump + quantityToAdd * unitPrice) / (physicalStock + quantityToAdd)



* Visibility: **protected**
* Source: [classes/stock/StockManager.php line 634](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L634)


#### Arguments
* $stock **[Stock](class.StockCore.md)**
* $quantity **integer**
* $price_te **float**



### <a name="method-getProductCoverage"></a>getProductCoverage

```php
integer StockManagerCore::getProductCoverage($id_product, $id_product_attribute, $coverage, $id_warehouse)
```

For a given product, returns the time left before being out of stock.

By default, for the given product, it will use sum(quantities removed in all warehouses)

* Visibility: **public**
* Source: [classes/stock/StockManager.php line 583](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L583)


#### Arguments
* $id_product **mixed**
* $id_product_attribute **mixed**
* $coverage **mixed**
* $id_warehouse **mixed**



### <a name="method-getProductPhysicalQuantities"></a>getProductPhysicalQuantities

```php
mixed StockManagerCore::getProductPhysicalQuantities($id_product, $id_product_attribute, $ids_warehouse, $usable)
```

For a given product, returns its physical quantity
If the given product has combinations and $id_product_attribute is null, returns the sum for all combinations



* Visibility: **public**
* Source: [classes/stock/StockManager.php line 424](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L424)


#### Arguments
* $id_product **mixed**
* $id_product_attribute **mixed**
* $ids_warehouse **mixed**
* $usable **mixed**



### <a name="method-getProductRealQuantities"></a>getProductRealQuantities

```php
mixed StockManagerCore::getProductRealQuantities($id_product, $id_product_attribute, $ids_warehouse, $usable)
```

For a given product, returns its real quantity
If the given product has combinations and $id_product_attribute is null, returns the sum for all combinations
Real quantity : (physical_qty + supply_orders_qty - client_orders_qty)
If $usable is defined, real quantity: usable_qty + supply_orders_qty - client_orders_qty



* Visibility: **public**
* Source: [classes/stock/StockManager.php line 456](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L456)


#### Arguments
* $id_product **mixed**
* $id_product_attribute **mixed**
* $ids_warehouse **mixed**
* $usable **mixed**



### <a name="method-getStockCollection"></a>getStockCollection

```php
\Collection StockManagerCore::getStockCollection(integer $id_product, integer $id_product_attribute, integer $id_warehouse, integer $price_te)
```

For a given product, retrieves the stock collection



* Visibility: **protected**
* Source: [classes/stock/StockManager.php line 648](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L648)


#### Arguments
* $id_product **integer**
* $id_product_attribute **integer**
* $id_warehouse **integer** - Optional
* $price_te **integer** - Optional



### <a name="method-isAvailable"></a>isAvailable

```php
mixed StockManagerCore::isAvailable()
```

Checks if the StockManager is available



* Visibility: **public**
* This method is **static**.
* Source: [classes/stock/StockManager.php line 37](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L37)




### <a name="method-removeProduct"></a>removeProduct

```php
mixed StockManagerCore::removeProduct($id_product, $id_product_attribute, \Warehouse $warehouse, $quantity, $id_stock_mvt_reason, $is_usable, $id_order)
```

For a given product, removes a given quantity



* Visibility: **public**
* Source: [classes/stock/StockManager.php line 188](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L188)


#### Arguments
* $id_product **mixed**
* $id_product_attribute **mixed**
* $warehouse **[Warehouse](class.WarehouseCore.md)**
* $quantity **mixed**
* $id_stock_mvt_reason **mixed**
* $is_usable **mixed**
* $id_order **mixed**



### <a name="method-transferBetweenWarehouses"></a>transferBetweenWarehouses

```php
mixed StockManagerCore::transferBetweenWarehouses($id_product, $id_product_attribute, $quantity, $id_warehouse_from, $id_warehouse_to, $usable_from, $usable_to)
```

For a given product, transfers quantities between two warehouses
By default, it manages usable quantities
It is also possible to transfer a usable quantity from warehouse 1 in an unusable quantity to warehouse 2
It is also possible to transfer a usable quantity from warehouse 1 in an unusable quantity to warehouse 1



* Visibility: **public**
* Source: [classes/stock/StockManager.php line 519](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.3/classes/stock/StockManager.php#L519)


#### Arguments
* $id_product **mixed**
* $id_product_attribute **mixed**
* $quantity **mixed**
* $id_warehouse_from **mixed**
* $id_warehouse_to **mixed**
* $usable_from **mixed**
* $usable_to **mixed**


