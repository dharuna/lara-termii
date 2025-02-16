```markdown
<p align="center">
    <img title="Termii" src="https://termii.com/assets/images/logo.png"/>
</p>

## Termii Laravel Package
Lara-Termii helps you set up, test, and manage your Termii integration directly in your Laravel application.

[![Total Downloads](https://img.shields.io/packagist/dt/dharuna/lara-termii.svg?style=flat-square)](https://packagist.org/packages/dharuna/lara-termii)

## Installation

You can install the package via Composer:

```bash
composer require dharuna/lara-termii
```

## Usage:

### Declare an Instance of the Class
- Example: `$termii = new \Dharuna\LaraTermii\LaraTermii("YOUR-TERMII-API-KEY");`

### Check Your Termii Balance
- You can check your Termii balance.
- Run `$termii->balance()`

### Retrieve Reports for Messages Sent Across SMS, Voice & WhatsApp Channels
- Run `$termii->history()`

### Detect Fake Numbers or Network Porting
- Run `$termii->status(int $phone_number, string $country_code)` with the appropriate parameters.

### Verify Phone Numbers and Detect Their Status
- Run `$termii->search(int $phone_number)`

### Retrieve the Status of All Registered Sender IDs
- Run `$termii->allSenderId()`

### Request a New Sender ID
- Run `$termii->submitSenderId(string $sender_id, string $use_case, string $company)`

### Send a Message
- Run `$termii->sendMessage(int $to, string $from, string $sms, string $channel = "generic", bool $media = false, string $media_url = null, string $media_caption = null)`

### Send OTP
- Run `$termii->sendOTP(int $to, string $from, string $message_type, int $pin_attempts, int $pin_time_to_live, int $pin_length, string $pin_placeholder, string $message_text, string $channel = "generic")`

### Send Voice OTP
- Run `$termii->sendVoiceOTP(int $to, int $pin_attempts, int $pin_time_to_live, int $pin_length)`

### Send Voice Call
- Run `$termii->sendVoiceCall(int $to, int $code)`

### OTP Validation
- Run `$termii->verifyOTP(string $pinId, string $pin)`

### Send In-App OTP
- Run `$termii->sendInAppOTP(int $to, int $pin_attempts, int $pin_time_to_live, int $pin_length, string $pin_type)`

### Security

If you discover any security-related issues, please email adamsohiani@gmail.com instead of using the issue tracker.

## Credits

- [Danladi Haruna](https://github.com/dharuna)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

This package is a fork of [https://github.com/zeevx/lara-termii](https://github.com/zeevx/lara-termii) and has been updated to support Laravel 11.
```

