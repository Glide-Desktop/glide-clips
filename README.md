# Glide Clips

The video player of the [Glide desktop](https://github.com/Glide-Desktop), on
GStreamer: a borderless player, subtitles, chapters, trimming, clips and
export, picture in picture. `glide-video` is its engine.

## Build

```sh
cargo build --release
```

Needs the GStreamer 1.24+ development files (`gstreamer-1.0`,
`gstreamer-app-1.0`, `gstreamer-video-1.0`, `gstreamer-pbutils-1.0`).

The shared crates come from a tag of
[glide-libs](https://github.com/Glide-Desktop/glide-libs). To build against a
checkout of glide-libs next to this one, create `.cargo/config.toml` (ignored
by git):

```toml
[patch."https://github.com/Glide-Desktop/glide-libs"]
glide-app = { path = "../glide-libs/crates/glide-app" }
glide-config = { path = "../glide-libs/crates/glide-config" }
glide-sdk = { path = "../glide-libs/crates/glide-sdk" }
```

Split from the Glide monorepo with its history in November 2026.
