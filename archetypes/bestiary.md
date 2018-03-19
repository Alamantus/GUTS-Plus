---{{ $nameSplit := split .Name "_" }}{{ $creatureType := index $nameSplit 0 }}{{ $name := index $nameSplit 1 }}
{{ if gt (len $nameSplit) 1 }}title: "{{ replace $name "-" " " | title }}"
creatureType: "{{ $creatureType | urlize }}"
slug: "{{ $creatureType | urlize }}/{{ $name | urlize }}"
stats:
- name: gumption
  value: 0
- name: utility
  value: 0
- name: thought
  value: 0
- name: slyness
  value: 0
- name: custom
  value: 0
clothing:
  torso: null
  legs: null
  feet: null
accessories:
  head: null
  neck: null
  arms: null
  back: null
  waist: null
  legs: null
inventory:
  hands:
  - null
  bag:
  - null
{{- else -}}
title: "{{ replace $creatureType "-" " " | title }}"
name: "{{ $creatureType | urlize }}"
creatureType: self{{ end }}
type: bestiary
draft: true
---
{{ if gt (len $nameSplit) 1 }}#### Appearance

Character appearance

#### Background

Character background

#### Personality

Character personality{{ else }}Explanation of the creature type.{{end}}
