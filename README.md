# Zerotoprod\Dock

![](./art/logo.png)

[![Repo](https://img.shields.io/badge/github-gray?logo=github)](https://github.com/zero-to-prod/dock)
[![Packagist Downloads](https://img.shields.io/packagist/dt/zero-to-prod/dock?color=blue)](https://packagist.org/packages/zero-to-prod/dock/stats)
[![Packagist Version](https://img.shields.io/packagist/v/zero-to-prod/dock?color=f28d1a)](https://packagist.org/packages/zero-to-prod/dock)
[![GitHub repo size](https://img.shields.io/github/repo-size/zero-to-prod/dock)](https://github.com/zero-to-prod/dock)
[![License](https://img.shields.io/packagist/l/zero-to-prod/dock?color=red)](https://github.com/zero-to-prod/dock/blob/main/LICENSE.md)
[![Hits-of-Code](https://hitsofcode.com/github/zero-to-prod/dock?branch=main)](https://hitsofcode.com/github/zero-to-prod/dock/view?branch=main)
[![wakatime](https://wakatime.com/badge/github/zero-to-prod/dock.svg)](https://wakatime.com/badge/github/zero-to-prod/dock)

## Contents

- [Introduction](#introduction)
- [Supported Php Versions](#supported-php-versions)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Initialization](#initialization)
- [Usage](#usage)
    - [Configuration](#configuration)
    - [Building Containers](#building-containers)
    - [Install Dependencies for a Runtime](#install-dependencies-for-a-runtime)
    - [Commands](#commands)

## Introduction

Dock provides a Docker powered local development experience for a PHP application.
Other than Docker, no software or libraries are required to be installed on your local computer before using Dock.
Dock's simple CLI means you can start building your PHP application without any previous Docker experience.

**Why you’ll love it**:
> - **Test Multiple PHP Versions** with one script.
> - **Switch Versions Easily** via `.env` settings.
> - **Comprehensive Docker Support** through docker-compose.
> - **PHP Debugging** already setup across all supported versions.
> - **Available with Composer**.

## Supported PHP Versions

Compatible with PHP:

- 7.1
- 7.2
- 7.3
- 7.4
- 8.0
- 8.1
- 8.2
- 8.3

## Prerequisites

- Docker installed and running

## Installation

Add `dock` to your project with Composer:

```shell
composer require zero-to-prod/dock --dev
```

## Initialization

Once you have the composer package installed, you can set up Dock in your project directory:

```shell
./vendor/bin/dock
```

This copies necessary configuration files to your project.

## Usage

Dock includes scripts to build and manage your PHP environments effortlessly.

### Configuration

Before starting development, verify that your `.env` file contains the correct settings.

You can specify which PHP version to use for local development, debugging, and Composer operations by updating these variables in your `.env` file:

```dotenv
PHP_VERSION=8.1
PHP_DEBUG=8.1
PHP_COMPOSER=8.1
```

### Building Containers

Build Docker containers based on your `.env` PHP versions:

```shell
sh dock build
```

This will create the following containers:

- php<PHP_VERSION> (example service: `php7.1`)
- debug<PHP_VERSION> (example service: `debug7.1`)
- composer<PHP_VERSION> (example service: `composer7.1`)

### Install Dependencies for a Runtime

Update Composer dependencies as defined in your `.env`:

```shell
sh dock composer update
```

### Commands

There a few commands that come with the default script.

```shell
sh dock build      # Builds the php, debug, and composer containers
sh dock init       # Initialize the .env file from .env.example if it doesn't exist.
sh dock test       # Run PHPUnit tests using the specified PHP version.
sh dock composer   # Run Composer commands using the specified PHP version.
sh dock <service>  # Run a specified Docker service with optional arguments.
```