---
title: Self-hosted server
parent: Operations
nav_order: 4
---

# Self-hosted server

The VFO Transmitter server is a lightweight PHP application that receives aircraft telemetry and exposes live views of the connected traffic. It is designed to be simple to deploy and does not require a traditional database.

## What the server provides

- a telemetry receive endpoint for transmitter clients
- a live radar display
- a sortable aircraft status dashboard
- embeddable map views
- an IVAO-compatible feed for external tools
- JSON endpoints for integrations

## Architecture at a glance

The server stores recent aircraft data in **APCu** memory cache. That makes the stack relatively simple:

1. a simulator client sends position data to the transmit endpoint
2. the server validates and stores the update
3. radar, status, and feed endpoints read the cached data
4. browsers and third-party tools render the live aircraft picture

## Draft deployment requirements

- PHP 7.4 or newer
- APCu enabled
- a web server such as Apache or Nginx with PHP support

## Why this is useful

For community-led flying, self-hosting gives organisers more control over:

- who connects
- how data is retained
- which views and feeds are exposed
- how the tooling is customised for events or groups

## Planned expansion

This page should eventually include a fuller deployment guide, but even in draft form it marks out the main ideas:

- simple setup
- low operational overhead
- practical support for real-time shared flying

## Related pages

- [Transmitter overview](transmitter.md)
- [Live radar and status tools](live-radar.md)
- [Community](../community.md)
