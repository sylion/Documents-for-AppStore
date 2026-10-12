# README

## Capture

Run the script from the repository root:

```sh
swift scripts/capture_screenshots.swift
```

To capture one language, pass its name, app locale code, or App Store locale code:

```sh
swift scripts/capture_screenshots.swift ja
swift scripts/capture_screenshots.swift pt-BR
```

The script saves screenshots to `screenshots/<App Store locale>/` with the numbered filenames corresponding to the order in which items are listed in the store.

## Setting notes

- Background color: HSB 83°, 67% 67%
- Window size: 700 px, 780 px
