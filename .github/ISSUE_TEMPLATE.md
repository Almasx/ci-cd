---
title: "RELEASE {{ ref }}"
labels: "RELEASE"
---

Author: {{ actor }}
Release date: {{ date | date('dddd, MMMM Do') }}
Version number: {{ ref }}

Payload:
{% for k, v in payload %}

- {{ k }}: {{ v }}
  {% endfor %}
