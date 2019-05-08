# ![LOGO](logo.png) WINSMS **flow**ground Connector

## Description

A generated **flow**ground connector for the WINSMS API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/winsms.co.za/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:44:57+03:00

## API Description

WinSMS RESTful API

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Get your current WinSMS credit balance

> Get the current remaining credit balance for the account.<br/>
> <br/>
> ***Note*** - The credit balance is expressed as a value with a single decimal place.

*Tags:* `credits`

### Transfer credits between main and sub accounts.

> Transfer credits between accounts.<br/>
> - From Main account to Sub account.<br/>
> <br/>
> - From Sub account to Main account.<br/>
> <br/>
> - From Sub account to another Sub account.<br/>
> <br/>
> Your WinSMS account number and sub account number/s can be obtained by logging in to the WinSMS Client Zone (www.winsms.co.za/cz) with the main account's credentials.<br/>
> <br/>
> The main account number is on the home tab and the sub account numbers are under the sub accounts tab.<br/>
> <br/>
> Account numbers should be submitted as integers. Do not add the 'W' prefix.

*Tags:* `credits`

### Get a list of incoming short/long code messages

> ***Only available to users with a [WinSMS Short/Long Code](https://support.winsms.co.za/winsms-long-short-code-system/).***<br/>
> Get a list of all incoming short/long code messages received by the account.<br/>
> <br/>
> Only the first 100 incoming short/long code messages will be returned if no ***offset*** and ***limit*** parameters are specified.

*Tags:* `shortcode`

#### Input Parameters
* `offset` - _optional_ - ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0.

* `limit` - _optional_ - ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000.


### Get a list of incoming SMS messages

> Get a list of all incoming SMS messages received by the account.<br/>
> <br/>
> Only the first 100 incoming messages will be returned if no ***offset*** and ***limit*** parameters are specified.

*Tags:* `sms`

#### Input Parameters
* `offset` - _optional_ - ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0.

* `limit` - _optional_ - ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000.


### Get a list of incoming opt-out SMS messages

> Get a list of all opt-out SMS messages received by the account, as well as all manually added opt-out numbers.<br>

*Tags:* `sms`

### Send SMS messages

> Submit 1 or more SMS messages to be sent by WinSMS. Maximum 1000 recipients per request.<br/>
> <br/>
> The SMS message text can be a maximum of 918 characters long. If you are submitting a message longer than 160 characters, you should change the value of ***maxSegments***.

*Tags:* `sms`

### Get SMS delivery statuses

> Get a list of previously submitted SMS message delivery statuses.<br/>
> <br/>
> Post an array of API Message Ids received from the ***/sms/outgoing/send*** endpoint.

*Tags:* `sms`

### Get a list of scheduled SMS messages

> Get a list of all scheduled SMS messages that have not yet been sent.<br/>
> <br/>
> Only the first 100 scheduled messages will be returned if no ***offset*** and ***limit*** parameters are specified.

*Tags:* `sms`

#### Input Parameters
* `offset` - _optional_ - ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0.

* `limit` - _optional_ - ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000.


### Delete scheduled SMS messages and refund credits

> Delete a list of previously scheduled SMS messages that have not yet been sent.<br/>
> <br/>
> Credits originally deducted for each SMS message will be refunded to your account upon successful deletion.

*Tags:* `sms`

### Get a list of all Sub Accounts.

> Get a list of all the Sub Accounts owned by the Main Account.

*Tags:* `subaccounts`

## License

**flow**ground :- Telekom iPaaS / winsms-co-za-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
