Class HelperCore
=====================





* Class name: HelperCore
* Source: [classes/helper/Helper.php line 28](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L28)


Contents
--------


### Properties

* [$base_folder](#property-$base_folder)
* [$base_tpl](#property-$base_tpl)
* [$context](#property-$context)
* [$currentIndex](#property-$currentIndex)
* [$identifier](#property-$identifier)
* [$module](#property-$module)
* [$override_folder](#property-$override_folder)
* [$ps_help_context](#property-$ps_help_context)
* [$show_toolbar](#property-$show_toolbar)
* [$table](#property-$table)
* [$title](#property-$title)
* [$token](#property-$token)
* [$toolbar_btn](#property-$toolbar_btn)
* [$toolbar_scroll](#property-$toolbar_scroll)
* [$tpl](#property-$tpl)
* [$tpl_vars](#property-$tpl_vars)

### Methods

* [__construct](#method-__construct)
* [createTemplate](#method-createTemplate)
* [generate](#method-generate)
* [l](#method-l)
* [renderAdminCategorieTree](#method-renderAdminCategorieTree)
* [renderCategoryTree](#method-renderCategoryTree)
* [renderRequiredFields](#method-renderRequiredFields)
* [renderShopList](#method-renderShopList)
* [setTpl](#method-setTpl)




Properties
----------


### <a name="property-$base_folder"></a>$base_folder

```php
public string $base_folder
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 47](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L47).


### <a name="property-$base_tpl"></a>$base_tpl

```php
public string $base_tpl = 'content.tpl'
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 60](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L60).


### <a name="property-$context"></a>$context

```php
public mixed $context
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 38](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L38).


### <a name="property-$currentIndex"></a>$currentIndex

```php
public mixed $currentIndex
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 30](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L30).


### <a name="property-$identifier"></a>$identifier

```php
public mixed $identifier
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 32](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L32).


### <a name="property-$module"></a>$module

```php
public \Module $module
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 44](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L44).


### <a name="property-$override_folder"></a>$override_folder

```php
public string $override_folder
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 50](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L50).


### <a name="property-$ps_help_context"></a>$ps_help_context

```php
public mixed $ps_help_context
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 35](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L35).


### <a name="property-$show_toolbar"></a>$show_toolbar

```php
public mixed $show_toolbar = true
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 37](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L37).


### <a name="property-$table"></a>$table

```php
public mixed $table
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 31](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L31).


### <a name="property-$title"></a>$title

```php
public mixed $title
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 36](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L36).


### <a name="property-$token"></a>$token

```php
public mixed $token
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 33](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L33).


### <a name="property-$toolbar_btn"></a>$toolbar_btn

```php
public mixed $toolbar_btn
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 34](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L34).


### <a name="property-$toolbar_scroll"></a>$toolbar_scroll

```php
public mixed $toolbar_scroll = false
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 39](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L39).


### <a name="property-$tpl"></a>$tpl

```php
protected \smartyTemplate $tpl
```





* Visibility: **protected**
* Source: [classes/helper/Helper.php line 55](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L55).


### <a name="property-$tpl_vars"></a>$tpl_vars

```php
public mixed $tpl_vars = array()
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 62](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L62).


Methods
-------


### <a name="method-__construct"></a>__construct

```php
mixed HelperCore::__construct()
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 64](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L64)




### <a name="method-createTemplate"></a>createTemplate

```php
\Template HelperCore::createTemplate(string $tpl_name)
```

Create a template from the override file, else from the base file.



* Visibility: **public**
* Source: [classes/helper/Helper.php line 80](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L80)


#### Arguments
* $tpl_name **string** - filename



### <a name="method-generate"></a>generate

```php
void HelperCore::generate()
```

default behaviour for helper is to return a tpl fetched



* Visibility: **public**
* Source: [classes/helper/Helper.php line 111](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L111)




### <a name="method-l"></a>l

```php
string HelperCore::l(mixed $string, string $class, \boolan $addslashes, boolean $htmlentities)
```

use translations files to replace english expression.



* Visibility: **protected**
* Source: [classes/helper/Helper.php line 308](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L308)


#### Arguments
* $string **mixed** - term or expression in english
* $class **string**
* $addslashes **boolan** - if set to true, the return value will pass through addslashes(). Otherwise, stripslashes().
* $htmlentities **boolean** - if set to true(default), the return value will pass through htmlentities($string, ENT_QUOTES, &#039;utf-8&#039;)



### <a name="method-renderAdminCategorieTree"></a>renderAdminCategorieTree

```php
mixed HelperCore::renderAdminCategorieTree($translations, $selected_cat, $input_name, $use_radio, $use_search, $disabled_categories, $use_in_popup)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/helper/Helper.php line 120](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L120)


#### Arguments
* $translations **mixed**
* $selected_cat **mixed**
* $input_name **mixed**
* $use_radio **mixed**
* $use_search **mixed**
* $disabled_categories **mixed**
* $use_in_popup **mixed**



### <a name="method-renderCategoryTree"></a>renderCategoryTree

```php
string HelperCore::renderCategoryTree(array $root, \type $selected_cat, string $input_name, boolean $use_radio, boolean $use_search, array $disabled_categories, boolean $use_in_popup, boolean $use_shop_context)
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 168](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L168)


#### Arguments
* $root **array** - array with the name and ID of the tree root category, if null the Shop&#039;s root category will be used
* $selected_cat **type** - array of selected categories
            Format
                Array
                (
                     [0] =&gt; 1
                 [1] =&gt; 2
            )
                OR
            Array
            (
                 [1] =&gt; Array
                      (
                            [id_category] =&gt; 1
                            [name] =&gt; Home page
                      )
            )
* $input_name **string** - name of input
* $use_radio **boolean** - use radio tree or checkbox tree
* $use_search **boolean** - display a find category search box
* $disabled_categories **array**
* $use_in_popup **boolean**
* $use_shop_context **boolean**



### <a name="method-renderRequiredFields"></a>renderRequiredFields

```php
string HelperCore::renderRequiredFields(string $class_name, string $identifier, array $table_fields)
```

Render a form with potentials required fields



* Visibility: **public**
* Source: [classes/helper/Helper.php line 326](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L326)


#### Arguments
* $class_name **string**
* $identifier **string**
* $table_fields **array**



### <a name="method-renderShopList"></a>renderShopList

```php
mixed HelperCore::renderShopList()
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/helper/Helper.php line 355](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L355)




### <a name="method-setTpl"></a>setTpl

```php
mixed HelperCore::setTpl($tpl)
```





* Visibility: **public**
* Source: [classes/helper/Helper.php line 69](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.17/classes/helper/Helper.php#L69)


#### Arguments
* $tpl **mixed**


