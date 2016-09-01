yii2-helpers
=================

[![Latest Stable Version](https://img.shields.io/packagist/v/goodizer/yii2-helpers.svg)](https://packagist.org/packages/goodizer/yii2-helpers)
[![License](https://poser.pugx.org/goodizer/yii2-helpers/license)](https://packagist.org/packages/goodizer/yii2-helpers)
[![Total Downloads](https://poser.pugx.org/goodizer/yii2-helpers/downloads)](https://packagist.org/packages/goodizer/yii2-helpers)
[![Monthly Downloads](https://poser.pugx.org/goodizer/yii2-helpers/d/monthly)](https://packagist.org/packages/goodizer/yii2-helpers)
[![Daily Downloads](https://poser.pugx.org/goodizer/yii2-helpers/d/daily)](https://packagist.org/packages/goodizer/yii2-helpers)

## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

> Note: Check the [composer.json](https://github.com/kartik-v/yii2-date-range/blob/master/composer.json) for this extension's requirements and dependencies. 

Either run

```
$ php composer.phar require goodizer/yii2-helpers
```

or add

```
"goodizer/yii2-helpers": "@stable"
```

to the ```require``` section of your `composer.json` file.

## Usage

### GridSearchHelper

```php
use goodizer\helpers\GridSearchHelper;
use yii\grid\GridView;

$searchData = GridSearchHelper::search(new Note(), ['asArray' => false]);
echo GridView::widget([
	'columns' => [
		'id',
		'name',
		'etc',
	],
    'filterModel' => $searchData->filterModel,
    'dataProvider' => $searchData->dataProvider,
]);

```

### DbSyncHelper

```php
use goodizer\helpers\GridSearchHelper;
use yii\grid\GridView;

$sync = new DbSyncHelper([
  'common\models',
  'modules\admin\models',
  'some\another\namespace',
]);
$sync->run();

```
