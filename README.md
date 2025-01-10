# Zerotoprod\Dock

![](./art/logo.png)

[![Repo](https://img.shields.io/badge/github-gray?logo=github)](https://github.com/zero-to-prod/dock)
[![Packagist Downloads](https://img.shields.io/packagist/dt/zero-to-prod/dock?color=blue)](https://packagist.org/packages/zero-to-prod/dock/stats)
[![Packagist Version](https://img.shields.io/packagist/v/zero-to-prod/dock?color=f28d1a)](https://packagist.org/packages/zero-to-prod/dock)
[![GitHub repo size](https://img.shields.io/github/repo-size/zero-to-prod/dock)](https://github.com/zero-to-prod/dock)
[![License](https://img.shields.io/packagist/l/zero-to-prod/dock?color=red)](https://github.com/zero-to-prod/dock/blob/main/LICENSE.md)
[![Hits-of-Code](https://hitsofcode.com/github/zero-to-prod/dock?branch=main)](https://hitsofcode.com/github/zero-to-prod/dock/view?branch=main)
[![wakatime](https://wakatime.com/badge/github/zero-to-prod/dock.svg)](https://wakatime.com/badge/github/zero-to-prod/dock)

## Introduction

Dock provides a Docker powered local development experience for a PHP application.
Other than Docker, no software or libraries are required to be installed on your local computer before using Dock.
Dock's simple CLI means you can start building your PHP application without any previous Docker experience.

**Why you’ll love it**:
> - **Simplify Multiple PHP Version Testing** with a single command
> - **Simple Version Switching** with a single value in your `.env`
> - **Full Docker Support** with a simple docker-compose file.
> - **PHP Debugging** with all supported PHP versions.
> - **Pull it in with Composer** and run the installation script.

## Support

Supports PHP versions: `7.1` - `8.4`.

## Installation

To install this package run composer install:

```shell
composer require zero-to-prod/dock --dev
```

## Initialization
This copies the relevant file into the project directory

```shell
./vendor/bin/dock
```

## Usage

### Building a Containers

You can build the containers for the versions of php specified in your `.env` file.

This will create the following containers:
- php
- debug
- composer

```shell
sh dock build
```

### Install Dependencies for a Runtime

This will update the composer dependencies set in the `.env` file of your project.

```shell
sh dock composer update
```

There a few commands that come with the default script.

```shell
sh dock build      # Builds the php, debug, and composer containers
sh dock init       # Initialize the .env file from .env.example if it doesn't exist.
sh dock test       # Run PHPUnit tests using the specified PHP version.
sh dock composer   # Run Composer commands using the specified PHP version.
sh dock <service>  # Run a specified Docker service with optional arguments.
```