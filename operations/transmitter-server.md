---
title: Self-hosted server
parent: Operations
nav_order: 6
---

# Self-hosted server

VFO runs a hosted transmitter server at `https://transmitter.virtualflight.online`. Most community members can use this directly with the MSFS or X-Plane client and do not need to run their own server.

This page is for those who want to host their own instance — for example, to run a private tracking server for a specific event or group.

## What the server provides

- a receive endpoint for transmitter clients
- a live radar display
- a sortable aircraft status dashboard
- an IVAO-compatible data feed for third-party tools such as LittleNavMap
- JSON endpoints for custom integrations

## How it works

The server is a PHP application that uses **APCu** memory cache to store recent aircraft positions. There is no database required.

1. A simulator client sends position data to the receive endpoint
2. The server stores the update in APCu
3. Radar, status, and feed endpoints read from the cache
4. Browsers and tools render the live picture

## Requirements

- PHP 7.4 or newer
- APCu extension enabled
- Apache or Nginx with PHP support

## Getting the server

The server source is available on GitHub. Refer to the repository README for full deployment instructions.

For community questions and help, visit the [Discord server](../community/discord.md).
