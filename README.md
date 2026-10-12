
# Documents for App Store

The repository to maintain material for the Mac App Store


## Contribution

Feel free to add description in your language or to fix typos.
To add a description in another language, please translate the files in [metadata/en-US](metadata/en-US) as they are, and do not create your own description.
Place the translated files in `metadata/<locale>/` using a [supported App Store Connect locale code](https://developer.apple.com/documentation/appstoreconnectapi/managing-metadata-in-your-app-by-using-locale-shortcodes).


## Structure

- `metadata/<locale>/`: Localized App Store text, split into
    - `subtitle.txt` (up to 30 characters)
    - `keywords.txt`
    - `description.txt` (up to 4000 characters).
- `screenshots/<locale>/`: App Store screenshots, ordered by their numbered filenames corresponding to the order in the store.
- `scripts/`: The screenshot capture script, background, and demo files. See [screenshot documentation](scripts/README.md).

Directory names use App Store Connect locale codes, such as `en-US`, `de-DE`, and `pt-BR`.

Release notes are maintained in `metadata/default/release_notes.txt` for English and `metadata/ja/release_notes.txt` for Japanese only. Since other languages use the default English version, you don't need to include a `release_notes.txt` file for other languages.


## Upload

Install [fastlane](https://docs.fastlane.tools/) and configure [App Store Connect API authentication](https://docs.fastlane.tools/app-store-connect-api/).
Prepare an editable macOS version in App Store Connect, then run the following command from the repository root:

```sh
fastlane deliver --api_key_path /path/to/api-key.json
```

To upload only the text, add `--skip_screenshots` to the command.


## License

The materials are distributed under the terms of the __Attribution 4.0 International (CC BY 4.0)__. See the bundled [LICENSE](LICENSE) for details.
