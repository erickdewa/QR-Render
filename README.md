# PHP QR Code Reader / Decoder

This is a PHP library to detect and decode QR-codes. <br>
This is QR code reader that works without extensions. <br>
This library supports PSR-4. <br>
Based on [QR code decoder / reader for PHP](https://github.com/khanamiryan/php-qrcode-detector-decoder) <br>
Ported from [ZXing library](https://github.com/zxing/zxing) <br>

## Installation 
Use [Composer](https://getcomposer.org/):
```
composer require libern/qr-code-reader
```

## Usage 
From image url
```php
$QRCodeReader = new Libern\QRCodeReader\QRCodeReader();
$qrcode_text = $QRCodeReader->decode("path_to_qr_code");
echo $qrcode_text;
```
From image stream
```php
$QRCodeReader = new Libern\QRCodeReader\QRCodeReader();
$qrcode_text = $QRCodeReader->decode(base64_encode("image_stream"));
echo $qrcode_text;
```

## Requirements 
* PHP >= 5.6
* GD Library
