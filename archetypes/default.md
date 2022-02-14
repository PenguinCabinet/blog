---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
description: "{{ replace .Name "-" " " |substr 0 100| description }}"
---

