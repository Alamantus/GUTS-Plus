---{{ $nameSplit := split .Name "_" }}{{ $campaign := index $nameSplit 0 }}{{ $session := index $nameSplit 1 }}
title: "Session {{ int $session | add 1 }}"
date: {{ .Date }}
draft: true
type: sessions
session: {{ int $session }}
campaign: "{{ $campaign | urlize}}"
---

