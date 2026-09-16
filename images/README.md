# Figures

Every `<image-slot>` in `index.html` now carries a `src`. Paper figures and the
Bullet Cluster images live in this directory; photographs are hotlinked from
Wikimedia Commons through its `Special:FilePath` resizer, so nothing large is
stored in the repo.

| Slot | Chapter | Image | Source |
|---|---|---|---|
| `wl-fig-1a` | 01 Prehistory | 1919 eclipse negative | Commons `File:1919_eclipse_negative.jpg`, public domain |
| `wl-fig-1b` | 01 Prehistory | Arthur Stanley Eddington | Commons `File:Arthur_Stanley_Eddington.jpg`, public domain |
| `wl-fig-2a` | 02 Zwicky | `zwickypaper.png` — first page of Zwicky (1937) | *Phys. Rev.* **51**, 290 |
| `wl-fig-3a` | 03 Dormant decades | 3C 273 | Commons `File:Quasar_3C_273.jpg`, ESA/Hubble & NASA |
| `wl-fig-5a` | 05 First detection | Abell 1689 (ACS, 2002) | Commons `File:Abell1689_HST_2003-01-a-1280_wallpaper.jpg`, NASA/ESA/ACS team |
| `wl-fig-6a` | 06 Becomes a tool | `truedensity_kaisersquires.png` | Kaiser & Squires (1993) |
| `wl-fig-6b` | 06 Becomes a tool | `reconstruction_kaisersquires.png` | Kaiser & Squires (1993) |
| `wl-fig-7a` | 07 Galaxy–galaxy | `imagepolarizationvstheta_brainerd1996.png` | Brainerd, Blandford & Smail (1996) |
| `wl-fig-8a` | 08 Shear predictions | `magnification_jainseljakwhite.png` | Jain, Seljak & White (2000) |
| `wl-fig-8b` | 08 Shear predictions | `shear_jainseljakwhite.png` | Jain, Seljak & White (2000) |
| `wl-fig-9a` | 09 The 2000 detections | `2pt_vanWaerbeke2000.png` | Van Waerbeke et al. (2000) |
| `wl-fig-10a` | 10 Systematics | `STEP1_mc_results.png` | Heymans et al. (2006) |
| `wl-fig-11a` | 11 Dark matter | `xray_bulletcluster.jpeg` | NASA/CXC/CfA/M. Markevitch et al. |
| `wl-fig-11b` | 11 Dark matter | `weaklensing_bulletcluster.png` | Clowe et al. (2006) |

Chapter 12 has no photo slot; its figure is the drawn S₈ plot. Chapters 5, 6,
11 and 12 also carry inline SVG diagrams that need no files.

## Conventions

- Paper figures use `fit="contain"` with the file's exact pixel aspect ratio, so
  nothing is cropped, and a `max-width` on the figure so small plots are not
  upscaled to blur. Photographs may use `fit="cover"`.
- `credit` is set on every slot and shows as a small overlay. Keep it.
- Hotlinked Commons URLs have the form
  `https://commons.wikimedia.org/wiki/Special:FilePath/<File name>?width=1600`.
  If Commons renames a file the slot renders a broken image, not the placeholder
  frame, so check the four photo slots after any long gap.

## A note on rights

The Commons and NASA images are public domain or credit-only. The journal
figures are the publishers' copyright; educational reuse with attribution is
customary, but check if the site is public and you want to be careful.
