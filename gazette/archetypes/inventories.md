---{{ $nameSplit := split .Name "_" }}{{ $campaign := index $nameSplit 0 }}{{ $character := index $nameSplit 1 }}{{ $session := index $nameSplit 2 }}{{ $instant := index $nameSplit 3 }}
title: "{{ replace $character "-" " " | title }}'s Equipment for {{ replace $campaign "-" " " | title }} Session {{ int $session | add 1 }}"
type: inventories
draft: true
character: "{{ $character | urlize }}"
campaign: "{{ $campaign | urlize }}"
session: {{ int $session }}
instant: {{ int $instant }}
inventory:
  hands:
  - null
  bag:
  - null
---

