---
title: Range service
parent: Service package
section: guide-core
version: '2.6'
nav_order: 6
---
# Introduction

This service automatically exposes ranges of response entities. This
allows resources to not care of requested ranges and return full
representations that will then be transparently wrapped in partial
representations by this service, allowing the client to benefit from
partial downloads.
