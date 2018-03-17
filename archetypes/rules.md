---{{ $nameSplit := split .Name "_" }}{{ $book := index $nameSplit 0 }}{{ $chapter := index $nameSplit 1 }}
{{ if gt (len $nameSplit) 1 }}title: "{{ replace $chapter "-" " " | title }}"
book: "{{ $book | urlize }}"
slug: "{{ $book | urlize }}/{{ $chapter | urlize }}"
weight: 0{{- else -}}
title: "{{ replace $book "-" " " | title }}"
name: "{{ $book | urlize }}
book: self{{ end }}
type: rules
draft: true
---
