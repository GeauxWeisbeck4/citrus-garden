---
title: Creator Platforms
description: You may wonder why I would use creator platforms when it seems like I can create everything myself as a software developer, but they actually are a great way to grow your follower base as a creator - learn why here.
publishDate: 01 May 2025
seriesId: support-andrew
orderInSeries: 3
tags: ["ko-fi", "buymeacoffee", "patreon", "github-sponsors", "open-collective"]
---

g; /* Base hue color (Background, secondary accent, text) */
		--saturation: 10%; /* Saturation of background and text, 0% - no tint */

		/* Background */
		--bg-brightness: 95%; /* Background brightness, 100% - pure white */
		--theme-bg: var(--hue) var(--saturation) var(--bg-brightness); /* Background color */

		/* Accents */
		--theme-accent-two: 351deg 66% 48%; /* Primary accent color */
		--theme-accent-base: var(--hue) 50% 27%; /* Secondary accent color */

		/* Text (foreground calculated below based on --theme-fg) */
		--fg-brightness: 9%; /* Text brightness, 0% - pure black */
		--theme-fg: var(--hue) var(--saturation) var(--fg-brightness); /* Base color for text */
		--theme-text: var(--theme-color-550); /* Text color */

		/*** SECONDARY COLORS (External links, neutral accent, quotes) ***/
		--theme-link: var(--hue) 97% 31%; /* External link color */
		--theme-accent: var(--theme-color-650); /* Neutral accent, calculated below based on --theme-fg */
		--theme-quote: var(--theme-text); /* Quote color */
		
		/*** ADDITIONAL COLORS ***/
		--theme-lightest: var(--theme-color-350);
		--theme-lighter: var(--theme-color-400);
		--theme-light: var(--theme-color-450);
		
		/*** SPECIAL THEME COLORS (Distinct settings for each theme) ***/
		--theme-special-lightest: hsl(var(--hue), var(--saturation), 100%);
		--theme-special-lighter: hsl(var(--hue), var(--saturation), 98%);
		--theme-special-light: hsl(var(--theme-bg));
		--theme-special: var(--theme-color-75);
	}

	:root[data-theme="dark"] {
		color-scheme: dark;

		/*** MAIN COLORS (Base, Background, Accents, Text) ***/
		/* Base theme hue color */
		--hue: 200deg; /* Base hue color (Background, secondary accent, text) */
		--saturation: 53%;

		/* Background */
		--bg-brightness: 17%; /* Background brightness, 0% - black */
		--theme-bg: var(--hue) var(--saturation) var(--bg-brightness); /* Background color */

		/* Accents */
		--theme-accent-two: 50deg 72% 63%; /* Primary accent color for elements (was 45deg 80% 50%) */
		--theme-accent-base: var(--hue) 0% 85%; /* Secondary accent color for elements */

		/* Text (foreground calculated below based on --theme-fg) */
		--fg-brightness: 98%; /* Text brightness, 100% - pure white */
		--theme-text: var(--theme-color-600); /* Text color */

		/*** SECONDARY COLORS (External links, neutral accent, quotes) ***/
		--theme-link: var(--hue) 66% 66%; /* External link color */
		--theme-accent: var(--theme-color-700); /* Neutral accent */
		--theme-quote: var(--theme-text); /* Quote color */

		/*** ADDITIONAL COLORS ***/
		--theme-lightest: var(--theme-color-400);
		--theme-lighter: var(--theme-color-450);
		--theme-light: var(--theme-color-500);

		/*** SPECIAL THEME COLORS (Distinct settings for each theme) ***/
		--theme-special-lightest: var(--theme-color-250);
		--theme-special-lighter: var(--theme-color-200);
		--theme-special-light: var(--theme-color-150);
		--theme-special: hsl(var(--hue) 0% 0% / 0.1275);
	}

	/* Global variables */
	:root {
		/* Base color for color gradation calculation */
		--theme-fg: var(--hue) var(--saturation) var(--fg-brightness);

		/* Gradations of the base color for text and elements */
		--theme-color-950: hsl(var(--theme-fg) / 0.9495);
		--theme-color-900: hsl(var(--theme-fg) / 0.9095);
		--theme-color-850: hsl(var(--theme-fg) / 0.8795);
		--theme-color-800: hsl(var(--theme-fg) / 0.8495);
		--theme-color-750: hsl(var(--theme-fg) / 0.7995);
		--theme-color-700: hsl(var(--theme-fg) / 0.7495);
		--theme-color-650: hsl(var(--theme-fg) / 0.7145);
		--theme-color-600: hsl(var(--theme-fg) / 0.6795);
		--theme-color-550: hsl(var(--theme-fg) / 0.6145);
		--theme-color-500: hsl(var(--theme-fg) / 0.5495);
		--theme-color-450: hsl(var(--theme-fg) / 0.4545);
		--theme-color-400: hsl(var(--theme-fg) / 0.3595);
		--theme-color-350: hsl(var(--theme-fg) / 0.2635);
		--theme-color-300: hsl(var(--theme-fg) / 0.1675);
		--theme-color-250: hsl(var(--theme-fg) / 0.1355);
		--theme-color-200: hsl(var(--theme-fg) / 0.1025);
		--theme-color-150: hsl(var(--theme-fg) / 0.0710);
		--theme-color-100: hsl(var(--theme-fg) / 0.0395);
		--theme-color-75: hsl(var(--theme-fg) / 0.0295);
		--theme-color-50: hsl(var(--theme-fg) / 0.0195);
	}
}
```

## What Does This Provide?
- **Easy Scalability**: A new theme can be created by adjusting `--hue`, `--saturation`, and base brightness.
- **Automatic Shade Generation**: The gradient system allows for dynamic color generation.
- **Flexibility**: The theme can be adapted for different contrast levels, custom schemes, and modes (e.g., `sepia`, `high contrast`).

This approach is perfect for **dynamic theming**, where the ability to easily adjust the appearance without manually inputting colors is crucial.