---{{ $nameSplit := split .Name "_" }}{{ $campaign := index $nameSplit 0 }}{{ $character := index $nameSplit 1 }}{{ $session := index $nameSplit 2 }}{{ $instant := index $nameSplit 3 }}
title: "{{ replace $character "-" " " | title }}'s Stats for {{ replace $campaign "-" " " | title }} Session {{ int $session | add 1 }}"
type: stats
draft: true
character: "{{ $character | urlize }}"
campaign: "{{ $campaign | urlize }}"
session: {{ int $session }}
instant: {{ int $instant }}
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
---

