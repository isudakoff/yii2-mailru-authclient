# yii2-mailru-authclient

This extension adds MailRu OAuth2 supporting for [yii2-authclient](https://github.com/yiisoft/yii2-authclient).

## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist isudakoff/yii2-mailru-authclient "*"
```

or add

```json
"isudakoff/yii2-mailru-authclient": "*"
```

to the `require` section of your composer.json.

## Usage

You must read the yii2-authclient [docs](https://github.com/yiisoft/yii2-authclient/tree/master/docs/guide)

Register your application [in MailRu](https://api.mail.ru/apps/my/add/)

and add the MailRu client to your auth clients.

```php
'components' => [
    'authClientCollection' => [
        'class' => 'yii\authclient\Collection',
        'clients' => [
            'mailru' => [
                'class' => 'isudakoff\authclient\MailRu',
                'clientId' => 'mailru_app_id',
                'clientSecret' => 'mailru_app_secret',
            ],
            // other clients
        ],
    ],
    // ...
 ]
 ```