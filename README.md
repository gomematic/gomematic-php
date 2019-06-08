# Gomematic: SDK for PHP

[![Build Status](https://cloud.drone.io/api/badges/gomematic/gomematic-php/status.svg)](https://cloud.drone.io/gomematic/gomematic-php)
[![Join the Matrix chat at https://matrix.to/#/#gomematic:matrix.org](https://img.shields.io/badge/matrix-%23gomematic%3Amatrix.org-7bc9a4.svg)](https://matrix.to/#/#gomematic:matrix.org)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/f16e721cb3d54bf5afcb611df57aeab9)](https://www.codacy.com/app/gomematic/gomematic-php?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=gomematic/gomematic-php&amp;utm_campaign=Badge_Grade)
[![PHP version](https://badge.fury.io/ph/gomematic%2Fgomematic.svg)](https://badge.fury.io/ph/gomematic%2Fgomematic)

**This project is under heavy development, it's not in a working state yet!**

This repository will provide a client SDK for PHP. This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0-alpha1
- Package version: 1.0.0-alpha1
- Build package: org.openapitools.codegen.languages.PhpClientCodegen


## Installation


### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json` and run `composer install` after that:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/gomematic/gomematic-php.git"
    }
  ],
  "require": {
    "gomematic/gomematic": "*@dev"
  }
}
```


### Manual

Download the files and include `autoload.php` whereever you need this SDK:

```php
require_once('/path/to/gomematic/vendor/autoload.php');
```


## Tests

To run the unit tests:

```bash
composer install
./vendor/bin/phpunit
```


## Getting Started

Please follow the [installation](#installation) instructions and then run the following code:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$api = new Gomematic\Api\AuthApi(
    new GuzzleHttp\Client()
);

$authLogin = new \Gomematic\Model\AuthLogin(); // \Gomematic\Model\AuthLogin | The credentials to authenticate

try {
    $result = $api->loginUser($authLogin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->loginUser: ', $e->getMessage(), PHP_EOL;
}

?>
```


## Documentation for endpoints

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthApi* | [**loginUser**](docs/Api/AuthApi.md#loginuser) | **POST** /auth/login | Authenticate an user by credentials
*AuthApi* | [**refreshAuth**](docs/Api/AuthApi.md#refreshauth) | **GET** /auth/refresh | Refresh an auth token before it expires
*AuthApi* | [**verifyAuth**](docs/Api/AuthApi.md#verifyauth) | **GET** /auth/verify/{token} | Verify validity for an authentication token
*ProfileApi* | [**showProfile**](docs/Api/ProfileApi.md#showprofile) | **GET** /profile/self | Retrieve an unlimited auth token
*ProfileApi* | [**tokenProfile**](docs/Api/ProfileApi.md#tokenprofile) | **GET** /profile/token | Retrieve an unlimited auth token
*ProfileApi* | [**updateProfile**](docs/Api/ProfileApi.md#updateprofile) | **PUT** /profile/self | Retrieve an unlimited auth token
*TeamApi* | [**appendTeamToUser**](docs/Api/TeamApi.md#appendteamtouser) | **POST** /teams/{team_id}/users | Assign a user to team
*TeamApi* | [**createTeam**](docs/Api/TeamApi.md#createteam) | **POST** /teams | Create a new team
*TeamApi* | [**deleteTeam**](docs/Api/TeamApi.md#deleteteam) | **DELETE** /teams/{team_id} | Delete a specific team
*TeamApi* | [**deleteTeamFromUser**](docs/Api/TeamApi.md#deleteteamfromuser) | **DELETE** /teams/{team_id}/users | Remove a user from team
*TeamApi* | [**listTeamUsers**](docs/Api/TeamApi.md#listteamusers) | **GET** /teams/{team_id}/users | Fetch all users assigned to team
*TeamApi* | [**listTeams**](docs/Api/TeamApi.md#listteams) | **GET** /teams | Fetch all available teams
*TeamApi* | [**permitTeamUser**](docs/Api/TeamApi.md#permitteamuser) | **PUT** /teams/{team_id}/users | Update user perms for team
*TeamApi* | [**showTeam**](docs/Api/TeamApi.md#showteam) | **GET** /teams/{team_id} | Fetch a specific team
*TeamApi* | [**updateTeam**](docs/Api/TeamApi.md#updateteam) | **PUT** /teams/{team_id} | Update a specific team
*UserApi* | [**appendUserToTeam**](docs/Api/UserApi.md#appendusertoteam) | **POST** /users/{user_id}/teams | Assign a team to user
*UserApi* | [**createUser**](docs/Api/UserApi.md#createuser) | **POST** /users | Create a new user
*UserApi* | [**deleteUser**](docs/Api/UserApi.md#deleteuser) | **DELETE** /users/{user_id} | Delete a specific user
*UserApi* | [**deleteUserFromTeam**](docs/Api/UserApi.md#deleteuserfromteam) | **DELETE** /users/{user_id}/teams | Remove a team from user
*UserApi* | [**listUserTeams**](docs/Api/UserApi.md#listuserteams) | **GET** /users/{user_id}/teams | Fetch all teams assigned to user
*UserApi* | [**listUsers**](docs/Api/UserApi.md#listusers) | **GET** /users | Fetch all available users
*UserApi* | [**permitUserTeam**](docs/Api/UserApi.md#permituserteam) | **PUT** /users/{user_id}/teams | Update team perms for user
*UserApi* | [**showUser**](docs/Api/UserApi.md#showuser) | **GET** /users/{user_id} | Fetch a specific user
*UserApi* | [**updateUser**](docs/Api/UserApi.md#updateuser) | **PUT** /users/{user_id} | Update a specific user


## Documentation for models

 - [AuthLogin](docs/Model/AuthLogin.md)
 - [AuthToken](docs/Model/AuthToken.md)
 - [AuthVerify](docs/Model/AuthVerify.md)
 - [GeneralError](docs/Model/GeneralError.md)
 - [Profile](docs/Model/Profile.md)
 - [Team](docs/Model/Team.md)
 - [TeamUser](docs/Model/TeamUser.md)
 - [TeamUserParams](docs/Model/TeamUserParams.md)
 - [User](docs/Model/User.md)
 - [UserTeamParams](docs/Model/UserTeamParams.md)
 - [ValidationError](docs/Model/ValidationError.md)
 - [ValidationErrorErrors](docs/Model/ValidationErrorErrors.md)


## Documentation for authorization



## BasicAuth


- **Type**: HTTP basic authentication



## HeaderAuth


- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header




## Security

If you find a security issue please contact gomematic@webhippie.de first.


## Contributing

Fork -> Patch -> Push -> Pull Request


## Authors

* [Thomas Boerger](https://github.com/tboerger)


## License

Apache-2.0


## Copyright

```
Copyright (c) 2018 Thomas Boerger <thomas@webhippie.de>
```
