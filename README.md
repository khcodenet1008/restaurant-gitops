# Restaurant GitOps

Desired-state boilerplate for the restaurant assignment.

## Purpose

- keep deployment state separate from application source
- assemble environment-specific overlays
- update image tags without editing service code

## Structure

- `base/`: shared desired state
- `overlays/dev/`: developer environment overrides
- `overlays/demo/`: instructor demo overrides

## Rule

Service owners prepare service-local manifests in `restaurant-app/platform/services/<service>/`. Integration then copies or syncs the approved versions into this GitOps repo for release control.
