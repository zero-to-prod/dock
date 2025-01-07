# Zerotoprod\Dock

![](./art/logo.png)

[![Repo](https://img.shields.io/badge/github-gray?logo=github)](https://github.com/zero-to-prod/dock)
[![Packagist Downloads](https://img.shields.io/packagist/dt/zero-to-prod/dock?color=blue)](https://packagist.org/packages/zero-to-prod/dock/stats)
[![Packagist Version](https://img.shields.io/packagist/v/zero-to-prod/dock?color=f28d1a)](https://packagist.org/packages/zero-to-prod/dock)
[![GitHub repo size](https://img.shields.io/github/repo-size/zero-to-prod/dock)](https://github.com/zero-to-prod/dock)
[![License](https://img.shields.io/packagist/l/zero-to-prod/dock?color=red)](https://github.com/zero-to-prod/dock/blob/main/LICENSE.md)
[![Hits-of-Code](https://hitsofcode.com/github/zero-to-prod/dock?branch=main)](https://hitsofcode.com/github/zero-to-prod/dock/view?branch=main)

## Introduction

Dock provides a Docker powered local development experience for a PHP application.
Other than Docker, no software or libraries are required to be installed on your local computer before using Dock.
Dock's simple CLI means you can start building your PHP application without any previous Docker experience.

## Support

Supports PHP versions: `7.1` - `8.4`.

## Installation

To install this package run composer install:

```shell
composer require zero-to-prod/dock --dev
./vendor/bin/dock install
dock composer update
```

## Usage

There a few commands that come with the default script.

```shell
dock <arguments> # Forwards arguments to a service
dock test # Forwards arguments to a pre-configured test command
dock composer # Forwards arguments to the composer service
```