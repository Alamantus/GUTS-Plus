---{{ $nameSplit := split .Name "_" }}{{ $book := index $nameSplit 0 }}{{ $chapter := index $nameSplit 1 }}
{{ if gt (len $nameSplit) 1 }}title: "{{ replace $chapter "-" " " | title }}"
book: "{{ $book | urlize }}"
slug: "{{ $book | urlize }}/{{ $chapter | urlize }}"{{- else -}}
title: "{{ replace $book "-" " " | title }}"
name: "{{ $book | urlize }}
book: self{{ end }}
weight: 0
type: rules
draft: true
---
{{ if eq (len $nameSplit) 1 }}# Introduction

Introduction of the book.{{ end }}
