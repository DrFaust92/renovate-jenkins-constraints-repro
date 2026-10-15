# renovate-jenkins-constraints-repro

Minimal reproduction: `constraintsFiltering: "strict"` with a `jenkins` constraint drops every `jenkins-plugins` release that declares a `requiredCore`.

## Current behavior

No updates are proposed. Debug logs show `Invalid release constraint` with `"versioning": "maven"` and `"constraint": ">=2.541.3"` for every release.

## Expected behavior

`junit` is updated (newer releases require core <= 2.580.1). `pipeline-graph-view` stays at `1053.v9df19e6ceed2`, because releases from `1060.vd77a_9e310f75` onwards require core 2.585.
