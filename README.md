# Akane Rize Starlight

A dependency-free [BetterDiscord](https://betterdiscord.app/) theme: a full-screen background image with dark, translucent Discord surfaces so text stays readable.

> The theme loads its default background from `assets/background.png` in this repository (via raw.githubusercontent.com), so it works out of the box. You can swap in your own image, see below.

## Install

1. Install BetterDiscord.
2. Open Discord → **Settings → BetterDiscord → Themes → Open Themes Folder**.
3. Copy `AkaneRizeStarlight.theme.css` into that folder.
4. Enable **Akane Rize Starlight** in the Themes list.

## Set your background image

Edit the top of `AkaneRizeStarlight.theme.css`:

```css
--ars-bg-image: url("https://your-host.example/akane-rize.png");
```

- Use a direct `https://` link to the image file (e.g. a Discord CDN, Imgur or GitHub raw link) that you are allowed to use.
- Alternatively use a `data:` URI to embed it (makes the file large).
- Optionally keep the image in this repo under `assets/` and link its raw GitHub URL, e.g. `https://raw.githubusercontent.com/moonravit23/akane-rize-starlight/main/assets/background.png` (see License note first).

The reference illustration is 597×337 (landscape). That's small for full-screen use, so it will be upscaled and look soft on large monitors. Tips: use `--ars-bg-blur: 2px`–`4px`, a stronger `--ars-bg-overlay`, or an upscaled version of the image.

## Customize

All options are CSS variables in the `:root` block:

| Variable | Purpose |
|---|---|
| `--ars-bg-image` | Image URL |
| `--ars-bg-position` | Focal point (`center`, `70% 30%`, ...) |
| `--ars-bg-size` | `cover` (fill), `contain`, or e.g. `auto 100%` |
| `--ars-bg-overlay` | Dark tint over the image |
| `--ars-bg-blur` | Blur applied to the image |
| `--ars-surface-1/2/3` | Translucency of chat / sidebars / server list |
| `--ars-input` | Message box background |
| `--ars-accent` | Accent colour |
| `--ars-text`, `--ars-text-muted` | Text colours |

Raise the alpha value of the `rgba()` surfaces for better readability, lower it to show more image.

Responsive behaviour: the image always covers the window; the focal point shifts right on narrow or portrait windows (see the `@media` rules at the bottom).

## Notes

Discord periodically changes its class names. The theme matches on partial class names (`[class*="sidebar_"]`) to remain resilient, but some surfaces may need tweaks after Discord updates. Issues and PRs are welcome.

## Submit to the BetterDiscord theme gallery

Publishing this repository on GitHub does not automatically add the theme to BetterDiscord's searchable gallery.

1. Keep this repository public and keep `AkaneRizeStarlight.theme.css` at its current path so BetterDiscord can verify and track updates.
2. Sign in at [betterdiscord.app/themes](https://betterdiscord.app/themes) and connect your Discord account.
3. Use **Submit a theme** and submit this public repository/theme file for verification and review.
4. The theme becomes searchable in BetterDiscord only after it passes review and is approved. Updating the theme CSS later may trigger another review.

Review the [BetterDiscord theme guidelines](https://docs.betterdiscord.app/themes/publishing/guidelines) before submitting. The gallery expects themes to be substantially authored by their creator, so make sure you understand and can stand behind the CSS implementation before submitting it under your name.

## License

The theme code (CSS and README) is released under the MIT License, see [LICENSE](./LICENSE).

**Artwork is not covered by this license.** Akane Rize artwork belongs to its respective creator/rights holder. The bundled `assets/background.png` is included with the repository owner's confirmation that they have the right to redistribute it; it is not covered by the MIT license. If you fork this repo or use your own image, you must have the rights to use, and especially to redistribute, any image you configure or add to a fork. Do not publish artwork you do not have permission to share.
