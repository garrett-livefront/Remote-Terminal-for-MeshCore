# fork-ci branch

Fork-only tooling, never meant for upstream. `fork-image.yml` builds the Dockerfile from any
branch of this fork (default: `feat/companion-repeat-toggle`) and pushes it to
`ghcr.io/garrett-livefront/remoteterm-meshcore:<tag>` for the self-hosted Unraid instance.

Runs on every push to `fork-ci` (GitHub only exposes manual dispatch from the default branch, and
`main` stays a clean upstream mirror). Rebuild after the feature branch moves:
`git commit --allow-empty -m 'ci(fork): rebuild image' && git push origin fork-ci`.
Switch Unraid back to `jkingsman/remoteterm-meshcore:latest` once upstream ships the feature.
