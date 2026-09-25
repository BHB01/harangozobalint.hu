---
title: '{{ .File.ContentBaseName | replaceRE `^\d{4}-\d{2}-` "" | replaceRE "-" " " | title }}'
slug: '{{ .File.ContentBaseName | replaceRE `^\d{4}-\d{2}-` "" }}'
date: '{{ .Date }}'
draft: true
tags: []
description: ""
---
