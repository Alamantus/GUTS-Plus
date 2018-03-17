---{{ $nameSplit := split .Name "_" }}{{ $campaign := index $nameSplit 0 }}{{ $character := index $nameSplit 1 }}{{ $session := index $nameSplit 2 }}{{ $instant := index $nameSplit 3 }}
title: "{{ replace $character "-" " " | title }}'s Injuries for {{ replace $campaign "-" " " | title }} Session {{ int $session | add 1 }}"
type: injuries
draft: true
character: "{{ $character | urlize }}"
campaign: "{{ $campaign | urlize }}"
session: {{ int $session }}
instant: {{ int $instant }}
injuries:
- name: Head
  minor: 0
  maxMinor: 2
  major: 0
  maxMajor: 1
- name: Torso (Front)
  minor: 0
  maxMinor: 2
  major: 0
  maxMajor: 2
- name: Torso (Back)
  minor: 0
  maxMinor: 2
  major: 0
  maxMajor: 2
- name: Left Arm
  minor: 0
  maxMinor: 2
  major: 0
  maxMajor: 2
- name: Right Arm
  minor: 0
  maxMinor: 2
  major: 0
  maxMajor: 2
- name: Left Hand
  minor: 0
  maxMinor: 3
  major: 0
  maxMajor: 2
- name: Right Hand
  minor: 0
  maxMinor: 3
  major: 0
  maxMajor: 2
- name: Left Leg
  minor: 0
  maxMinor: 2
  major: 0
  maxMajor: 2
- name: Right Leg
  minor: 0
  maxMinor: 2
  major: 0
  maxMajor: 2
- name: Left Foot
  minor: 0
  maxMinor: 3
  major: 0
  maxMajor: 2
- name: Right Foot
  minor: 0
  maxMinor: 3
  major: 0
  maxMajor: 2
strain: 0
maxStrain: 10
---

