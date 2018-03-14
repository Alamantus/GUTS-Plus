---{{ $nameSplit := split .Name "_" }}{{ $campaign := index $nameSplit 0 }}{{ $name := index $nameSplit 1 }}
title: "{{ replace $name "-" " " | title }}"
name: "{{ $name }}"
type: characters
campaign: "{{ $campaign | urlize }}"
draft: true
---
### Appearance

Character appearance

### Background

Character background

### Personality

Character personality
