---
title: "{{ replace .Name "-" " " | title }}"
name: "{{ .Name | urlize }}"
type: campaigns
date: {{ .Date }}
endDate: null
draft: true
---
## Story
Story setup text

## Characters
{{ range where (where .Site.Pages "Section" "characters") ".Params.campaign" .Name }}
- [{{ .Title }}]({{ .RelPermalink }})
{{ end }}

## Sessions
{{ range where (where .Site.Pages "Section" "sessions") ".Params.campaign" .Name }}
- [{{ .Title }}]({{ .RelPermalink }})
{{ end }}
