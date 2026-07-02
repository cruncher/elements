# Figma → Elements component mapping

Maps the components in the Figma file **"EPFL Masters – Exploration"**
(`n0hB19uzLY9pWJuYfBGkBh`) to the styleguide's atoms / molecules / organisms.

Derived from the Figma "Composants" page plus everything instantiated across the
focus frames: **Home**, **Masters list**, **Masters detail**, **Event list**.
(The *Galaxy* pages are out of scope — a separate discussion.)

## Direct matches — existing styleguide component fits

| Figma component | Styleguide | Type | Notes |
|---|---|---|---|
| `gradient btn`, `Button` | `button` | atom | ✅ done (`.btn-gradient`) |
| `Card`, `highlight card` | `card` | molecule | close fit; needs restyle (16px radius, shadow) |
| `badge`, `Badge` | `tag` | atom | no "badge" atom exists; `tag` is the analogue (or Bootstrap `.badge`) |
| `Tooltip` | `popover` | atom | Bootstrap tooltip/popover |
| `Select` | `select` | atom | |
| `Icon`, `Icon wrapper`, `Primary/Secondary icon` | `icon` | atom | 282× — the icon system, heavily used |
| `VIdéo verticale` | `video` | atom | vertical variant |
| `Minor / SPE acordeon` | `collapse-group` | molecule | accordion |
| `Segmented control` | `tabs` | molecule | (or nav-pills) |
| `Directory` | `list-group` | molecule | |
| `Filter-chip` | `filters` + `tag` | molecule/atom | chips inside filter bar |
| `Header`, `Menu`, `Nav item`, `_menu item` | `header` / `nav-main` / `access-nav` | organism/molecule | |
| `Footer` | `footer` | organism | |
| `Contact` | `contact` | organism | |
| `Posts` | `news` / `card` | content-type | |
| `Master combination card/Event card` | `event` | content-type | |
| (Hero "Your perspectives…") | `hero` | organism | |
| (Highlights slider) | `card-slider` | organism | |
| (section titles) | `headlines` / `introduction` | organism | |
| (breadcrumb on Masters detail) | `breadcrumb` | molecule | |
| (carousel dots / paging) | `carousel` / `pagination` | molecule | |
| **Event list** (page) | `event-list` | page | ✅ page already exists |

## Domain-specific — no styleguide equivalent (new components, built on existing atoms)

| Figma component | Closest base | Notes |
|---|---|---|
| `Master combination card` (32×) | `card` / `card-deck` | core Masters concept — likely a new molecule |
| `Minor /SPE card` | `card` | |
| `SPE or Minor` | `tag` | coloured category pill w/ hover states |
| `Master builder form` | `form` (organism) | the interactive interest/bachelor selector |
| `Legend` | — | weak; map/form legend |
| `Fond coloré` ("coloured background") | `.bg-gradient-*` / `.bg-tint-*` | ✅ utilities already exist |
| `Masters detail` (page) | new `page` | assembled from content-types |

## Ignore

- `Galaxy`, `Master galaxy`, `Galaxy 1` — deferred (separate discussion).
- `cursor-arrow`, `Spec post it`, `Group 1` — design annotations / decoration, not real components.

## Notes

The design leans hard on **Card** (67 instances + several bespoke card types) and
**Icon** (282), so restyling `card` and the icon treatment gives the most coverage
fastest. The genuinely *new* work is the Masters-specific set (combination card,
builder form, SPE/Minor pills); everything else is a restyle of something that
already exists.
