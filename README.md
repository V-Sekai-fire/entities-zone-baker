# entities-zone-baker

An engine project that validates a user's avatar or map scene, exports it, and uploads the result to the multiplayer fabric's asset backend.

## What it is for

The upload pipeline runs it once per bake job in a container. The bake script imports and validates the scene, exports a clean copy, and uploads it as content-addressed chunks. The project is derived from the V-Sekai game project and kept in step with it as a git subrepo.

## Build and run

```sh
docker build .
```

The image's entry point takes the content type, `avatar` or `map`, then the scene to bake and the output path. The upload reads `ASSET_ID` and `URO_URL` from the environment.

## Licence

MIT; see LICENSE.
