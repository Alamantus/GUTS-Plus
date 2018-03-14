---{{ $nameSplit := split .Name "_" }}{{ $campaign := index $nameSplit 0 }}{{ $character := index $nameSplit 1 }}{{ $session := index $nameSplit 2 }}{{ $instant := index $nameSplit 3 }}
title: "{{ replace $character "-" " " | title }}'s Stats for {{ replace $campaign "-" " " | title }} Session {{ int $session | add 1 }}"
type: stats
draft: true
character: "{{ $character | urlize }}"
campaign: "{{ $campaign | urlize }}"
session: {{ int $session }}
instant: {{ int $instant }}
stats:
  gumption: 0
  utility: 0
  thought: 0
  slyness: 0
  custom: 0
---

