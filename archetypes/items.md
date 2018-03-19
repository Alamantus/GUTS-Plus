---{{ $nameSplit := split .Name "_" }}{{ $itemType := index $nameSplit 0 }}{{ $name := index $nameSplit 1 }}
{{ if gt (len $nameSplit) 1 }}title: "{{ replace $name "-" " " | title }}"
itemType: "{{ $itemType | urlize }}"
slug: "{{ $itemType | urlize }}/{{ $name | urlize }}"
{{ if or (eq $itemType "clothing") (eq $itemType "accessories") }}
location: torso|legs|feet|head|neck|arms|back|waist
perception: casual|fancy|lazy|athletic|nerdy|historical|futuristic
{{ end }}
{{- else -}}
title: "{{ replace $itemType "-" " " | title }}"
name: "{{ $itemType | urlize }}
itemType: self{{ end }}
type: items
draft: true
---
Item description
