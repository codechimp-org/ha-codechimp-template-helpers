[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)
![Version](https://img.shields.io/github/v/release/codechimp-org/ha-codechimp-template-helpers)
# CodeChimp Template helpers

This Template extension for Home Assistant contains various helper templates

# Installation

Install this in HACS or download the `codechimp-template-helpers.jinja` from this repository and place the files into your `config\custom_templates` directory.

# Macros

## `pluralize(value, singular, plural, spacer=True)`

A simple macro that will return the value with the given singular or plural suffix.

Arugment | Type | Default | Example | Description
:-:|:-:|:-:|:-:|---
value| string, int or float | - | `states('sensor.value')` | The value to evaluate, will be converted to float
singular | string | - | `'day'` | The string to use for singular
plural | string | - | `'days'` | The string to use for plurals & 0
spacer| boolean | `True` | `True` | (Optional) Whether to add a spacer between the value and the singular/plural suffix

### Example

```jinja
{% from 'codechimp-template-helpers.jinja' import pluralize %}
{{ pluralize( states('sensor.value'), 'day', 'days') }}
```
