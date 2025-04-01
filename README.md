Verge.io Rust SDK created with progenitor

1. Run the generator to preprocess the OpenAPI spec and add operation IDs required by progenitor
   `cargo run -p generator --release`
   It doesn't overwrite the target file `generator/swagger/generated-opids.json` so you may need to clean this first.
2. Run progenitor to generate the SDK
   `cargo progenitor -i generator/swagger/generated-opids.json -o sdk -n verge_rs_sdk -v 0.1.0 --interface builder --license-name "UNLICENSED"`
