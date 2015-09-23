Class ImageCore
=====================





* Class name: ImageCore
* Parent class: [ObjectModel](class.ObjectModelCore.md)
* Source: [classes/Image.php line 27](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L27)


Contents
--------


### Properties

* [$_cacheGetSize](#property-$_cacheGetSize)
* [$access_rights](#property-$access_rights)
* [$cover](#property-$cover)
* [$definition](#property-$definition)
* [$existing_path](#property-$existing_path)
* [$folder](#property-$folder)
* [$id](#property-$id)
* [$id_image](#property-$id_image)
* [$id_product](#property-$id_product)
* [$image_format](#property-$image_format)
* [$legend](#property-$legend)
* [$position](#property-$position)
* [$source_index](#property-$source_index)

### Methods

* [__construct](#method-__construct)
* [add](#method-add)
* [clearTmpDir](#method-clearTmpDir)
* [createImgFolder](#method-createImgFolder)
* [delete](#method-delete)
* [deleteAllImages](#method-deleteAllImages)
* [deleteCover](#method-deleteCover)
* [deleteImage](#method-deleteImage)
* [deleteProductAttributeImage](#method-deleteProductAttributeImage)
* [duplicateAttributeImageAssociations](#method-duplicateAttributeImageAssociations)
* [duplicateProductImages](#method-duplicateProductImages)
* [getAllImages](#method-getAllImages)
* [getCover](#method-getCover)
* [getExistingImgPath](#method-getExistingImgPath)
* [getHeight](#method-getHeight)
* [getHighestPosition](#method-getHighestPosition)
* [getImages](#method-getImages)
* [getImagesTotal](#method-getImagesTotal)
* [getImgFolder](#method-getImgFolder)
* [getImgFolderStatic](#method-getImgFolderStatic)
* [getImgPath](#method-getImgPath)
* [getPathForCreation](#method-getPathForCreation)
* [getSize](#method-getSize)
* [getWidth](#method-getWidth)
* [moveToNewFileSystem](#method-moveToNewFileSystem)
* [positionImage](#method-positionImage)
* [replaceAttributeImageAssociationId](#method-replaceAttributeImageAssociationId)
* [testFileSystem](#method-testFileSystem)
* [updatePosition](#method-updatePosition)




Properties
----------


### <a name="property-$_cacheGetSize"></a>$_cacheGetSize

```php
protected mixed $_cacheGetSize = array()
```





* Visibility: **protected**
* This property is **static**.
* Source: [classes/Image.php line 76](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L76).


### <a name="property-$access_rights"></a>$access_rights

```php
protected integer $access_rights = 509
```





* Visibility: **protected**
* This property is **static**.
* Source: [classes/Image.php line 59](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L59).


### <a name="property-$cover"></a>$cover

```php
public boolean $cover
```





* Visibility: **public**
* Source: [classes/Image.php line 41](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L41).


### <a name="property-$definition"></a>$definition

```php
public mixed $definition = array('table' => 'image', 'primary' => 'id_image', 'multilang' => true, 'fields' => array('id_product' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedId', 'required' => true), 'position' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt'), 'cover' => array('type' => self::TYPE_BOOL, 'validate' => 'isBool', 'shop' => true), 'legend' => array('type' => self::TYPE_STRING, 'lang' => true, 'validate' => 'isGenericName', 'size' => 128)))
```





* Visibility: **public**
* This property is **static**.
* Source: [classes/Image.php line 64](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L64).


### <a name="property-$existing_path"></a>$existing_path

```php
protected string $existing_path
```





* Visibility: **protected**
* Source: [classes/Image.php line 56](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L56).


### <a name="property-$folder"></a>$folder

```php
protected string $folder
```





* Visibility: **protected**
* Source: [classes/Image.php line 53](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L53).


### <a name="property-$id"></a>$id

```php
public mixed $id
```





* Visibility: **public**
* Source: [classes/Image.php line 29](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L29).


### <a name="property-$id_image"></a>$id_image

```php
public integer $id_image
```





* Visibility: **public**
* Source: [classes/Image.php line 32](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L32).


### <a name="property-$id_product"></a>$id_product

```php
public integer $id_product
```





* Visibility: **public**
* Source: [classes/Image.php line 35](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L35).


### <a name="property-$image_format"></a>$image_format

```php
public string $image_format = 'jpg'
```





* Visibility: **public**
* Source: [classes/Image.php line 47](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L47).


### <a name="property-$legend"></a>$legend

```php
public string $legend
```





* Visibility: **public**
* Source: [classes/Image.php line 44](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L44).


### <a name="property-$position"></a>$position

```php
public integer $position
```





* Visibility: **public**
* Source: [classes/Image.php line 38](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L38).


### <a name="property-$source_index"></a>$source_index

```php
public string $source_index
```





* Visibility: **public**
* Source: [classes/Image.php line 50](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L50).


Methods
-------


### <a name="method-__construct"></a>__construct

```php
mixed ImageCore::__construct($id, $id_lang)
```





* Visibility: **public**
* Source: [classes/Image.php line 78](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L78)


#### Arguments
* $id **mixed**
* $id_lang **mixed**



### <a name="method-add"></a>add

```php
mixed ImageCore::add($autodate, $null_values)
```





* Visibility: **public**
* Source: [classes/Image.php line 85](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L85)


#### Arguments
* $autodate **mixed**
* $null_values **mixed**



### <a name="method-clearTmpDir"></a>clearTmpDir

```php
mixed ImageCore::clearTmpDir()
```

Clear all images in tmp dir



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 399](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L399)




### <a name="method-createImgFolder"></a>createImgFolder

```php
boolean ImageCore::createImgFolder()
```

Create parent folders for the image in the new filesystem



* Visibility: **public**
* Source: [classes/Image.php line 556](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L556)




### <a name="method-delete"></a>delete

```php
mixed ImageCore::delete()
```





* Visibility: **public**
* Source: [classes/Image.php line 93](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L93)




### <a name="method-deleteAllImages"></a>deleteAllImages

```php
boolean ImageCore::deleteAllImages(string $path, string $format)
```

Recursively deletes all product images in the given folder tree and removes empty folders.



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 479](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L479)


#### Arguments
* $path **string** - folder containing the product images to delete
* $format **string** - image format



### <a name="method-deleteCover"></a>deleteCover

```php
boolean ImageCore::deleteCover(integer $id_product)
```

Delete product cover



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 194](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L194)


#### Arguments
* $id_product **integer** - Product ID



### <a name="method-deleteImage"></a>deleteImage

```php
mixed ImageCore::deleteImage($force_delete)
```

Delete the product image from disk and remove the containing folder if empty
Handles both legacy and new image filesystems



* Visibility: **public**
* Source: [classes/Image.php line 421](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L421)


#### Arguments
* $force_delete **mixed**



### <a name="method-deleteProductAttributeImage"></a>deleteProductAttributeImage

```php
mixed ImageCore::deleteProductAttributeImage()
```

Delete Image - Product attribute associations for this image



* Visibility: **public**
* Source: [classes/Image.php line 408](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L408)




### <a name="method-duplicateAttributeImageAssociations"></a>duplicateAttributeImageAssociations

```php
boolean ImageCore::duplicateAttributeImageAssociations($combination_images)
```

Duplicate product attribute image associations



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 296](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L296)


#### Arguments
* $combination_images **mixed**



### <a name="method-duplicateProductImages"></a>duplicateProductImages

```php
mixed ImageCore::duplicateProductImages(integer $id_product_old, boolean $id_product_new, $combination_images)
```

Copy images from a product to another



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 235](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L235)


#### Arguments
* $id_product_old **integer** - Source product ID
* $id_product_new **boolean** - Destination product ID
* $combination_images **mixed**



### <a name="method-getAllImages"></a>getAllImages

```php
array ImageCore::getAllImages()
```

Return Images



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 150](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L150)




### <a name="method-getCover"></a>getCover

```php
boolean ImageCore::getCover(integer $id_product)
```

Get product cover



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 220](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L220)


#### Arguments
* $id_product **integer** - Product ID



### <a name="method-getExistingImgPath"></a>getExistingImgPath

```php
mixed ImageCore::getExistingImgPath()
```

Returns image path in the old or in the new filesystem

@ returns string image path

* Visibility: **public**
* Source: [classes/Image.php line 519](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L519)




### <a name="method-getHeight"></a>getHeight

```php
mixed ImageCore::getHeight($params, $smarty)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 390](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L390)


#### Arguments
* $params **mixed**
* $smarty **mixed**



### <a name="method-getHighestPosition"></a>getHighestPosition

```php
integer ImageCore::getHighestPosition(integer $id_product)
```

Return highest position of images for a product



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 179](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L179)


#### Arguments
* $id_product **integer** - Product ID



### <a name="method-getImages"></a>getImages

```php
array ImageCore::getImages(integer $id_lang, integer $id_product, integer $id_product_attribute)
```

Return available images for a product



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 130](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L130)


#### Arguments
* $id_lang **integer** - Language ID
* $id_product **integer** - Product ID
* $id_product_attribute **integer** - Product Attribute ID



### <a name="method-getImagesTotal"></a>getImagesTotal

```php
integer ImageCore::getImagesTotal(integer $id_product)
```

Return number of images for a product



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 164](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L164)


#### Arguments
* $id_product **integer** - Product ID



### <a name="method-getImgFolder"></a>getImgFolder

```php
string ImageCore::getImgFolder()
```

Returns the path to the folder containing the image in the new filesystem



* Visibility: **public**
* Source: [classes/Image.php line 540](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L540)




### <a name="method-getImgFolderStatic"></a>getImgFolderStatic

```php
string ImageCore::getImgFolderStatic(mixed $id_image)
```

Returns the path to the folder containing the image in the new filesystem



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 596](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L596)


#### Arguments
* $id_image **mixed**



### <a name="method-getImgPath"></a>getImgPath

```php
string ImageCore::getImgPath()
```

Returns the path to the image without file extension



* Visibility: **public**
* Source: [classes/Image.php line 581](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L581)




### <a name="method-getPathForCreation"></a>getPathForCreation

```php
string ImageCore::getPathForCreation()
```

Returns the path where a product image should be created (without file format)



* Visibility: **public**
* Source: [classes/Image.php line 694](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L694)




### <a name="method-getSize"></a>getSize

```php
mixed ImageCore::getSize($type)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 373](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L373)


#### Arguments
* $type **mixed**



### <a name="method-getWidth"></a>getWidth

```php
mixed ImageCore::getWidth($params, $smarty)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 384](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L384)


#### Arguments
* $params **mixed**
* $smarty **mixed**



### <a name="method-moveToNewFileSystem"></a>moveToNewFileSystem

```php
mixed ImageCore::moveToNewFileSystem($max_execution_time)
```

Move all legacy product image files from the image folder root to their subfolder in the new filesystem.

If max_execution_time is provided, stops before timeout and returns string "timeout".
If any image cannot be moved, stops and returns "false"

* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 612](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L612)


#### Arguments
* $max_execution_time **mixed**



### <a name="method-positionImage"></a>positionImage

```php
mixed ImageCore::positionImage(integer $position, boolean $direction)
```

Reposition image



* Visibility: **public**
* Source: [classes/Image.php line 315](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L315)


#### Arguments
* $position **integer** - Position
* $direction **boolean** - Direction



### <a name="method-replaceAttributeImageAssociationId"></a>replaceAttributeImageAssociationId

```php
mixed ImageCore::replaceAttributeImageAssociationId($combination_images, $saved_id, $id_image)
```





* Visibility: **protected**
* This method is **static**.
* Source: [classes/Image.php line 281](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L281)


#### Arguments
* $combination_images **mixed**
* $saved_id **mixed**
* $id_image **mixed**



### <a name="method-testFileSystem"></a>testFileSystem

```php
boolean ImageCore::testFileSystem()
```

Try to create and delete some folders to check if moving images to new file system will be possible



* Visibility: **public**
* This method is **static**.
* Source: [classes/Image.php line 662](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L662)




### <a name="method-updatePosition"></a>updatePosition

```php
integer ImageCore::updatePosition(integer $way, integer $position)
```

Change an image position and update relative positions



* Visibility: **public**
* Source: [classes/Image.php line 350](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/classes/Image.php#L350)


#### Arguments
* $way **integer** - position is moved up if 0, moved down if 1
* $position **integer** - new position of the moved image

