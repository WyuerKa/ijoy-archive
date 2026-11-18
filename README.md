# IJOY downloads archive

A preservation copy of everything that could still be downloaded from the IJOY website
(ijoycig.com) and from the Internet Archive in November 2026: firmware, the firmware update
tool, user manuals, EU TPD documents and marketing material for IJOY devices (2015–2025).

IJOY has been removing older devices and their files from the site, so this collects them in
one place while they are still reachable.

## Layout

| Folder | Contents |
|---|---|
| [`firmware/`](firmware) | 23 firmware packages (`.dfu`, `.bin` or `.hex` inside, most with upgrade instructions) |
| [`software/`](software) | IJOY Update installer (Windows DFU flashing tool + PDF guide) |
| [`manuals/`](manuals) | 68 user manuals |
| [`tpd/`](tpd) | 18 EU TPD documents |
| [`marketing/`](marketing) | posters, banners, product pictures, logos, catalog, site video |
| [`other/`](other) | one stray file served by the download handler |
| [`index.csv`](index.csv) | every file: size, SHA-256, name on the site, original URL(s), Wayback URL |
| [`sources/`](sources) | how it was collected: link lists, Wayback CDX dumps, archived HTML pages |

Files are kept exactly as served; only the file names were tidied (site ID prefixes removed).
Identical files found at several URLs are stored once, with every URL listed in `index.csv`.
Many manual names are in Chinese as IJOY uploaded them; the device model is usually in the name
(e.g. `IM926`, `K813`, `Avenger 270`).

## Firmware

| Device | Version | File |
|---|---|---|
| Avenger 270 (PD270) | 1.72 | `Avenger PD270_Ver1.72.zip` |
| Avenger Baby | 1.3 | `AvengerBaby.zip` |
| CAPO 100 | 1.4 | `Capo100 firmware v1.4.zip` |
| CAPO 216 | 1.3 | `CAPO216_Ver1.3.zip` |
| Captain PD1865 | 1.2 | `Captain PD1865 firmware v1.2.zip` |
| Captain PD270 | 1.5 | `Captain PD270 firmware ver1.5.zip` |
| Captain PD270 | 1.6 | `Captain PD270 firmware ver1.6.zip` and `.rar` (two packagings, identical `.dfu` files) |
| Captain X3 | 1.3 | `Captain X3 firmware ver1.3.zip` |
| Captain 2 | 1.1 | `Captain2_v1.1.zip` |
| Diamond PD270 | 1.3 | `Diamond firmware ver1.3.zip` |
| Diamond Mini | 1.4 | `Diamond mini_firmware ver1.4.zip` |
| EXO PD270 | 1.2 | `EXO PD270 _firmware ver1.2.zip` |
| Genie PD270 | 1.1 | `Genie pd270 firmware v1.1.zip` |
| LUX | 1.1, 1.2 | `IJOY lux firmware ver1.1.rar`, `ver1.2.rar` |
| MAXO | 1.2 | `The MAXO firmware ver1.2.zip` |
| MAXO QUAD 1865 | 2.1 | `MAXO QUAD 1865 firmware v2.1.zip` |
| ELITE PS2170 | 1.6 | `PS2170 firmware ver1.6.zip` |
| RDTA Box | 2.1, 2.2 | `RDTABOX firmware ver2.1.zip`, `Rdta_box firmware v2.2.zip` |
| RDTA Box Mini | 1.23 | `Rdtaboxmini firmware ver1.23.rar` |
| Shogun | 1.5 | `Shogun firmware ver1.5.zip` |

Three kinds of packages:

- `.dfu` (2016–2018 devices): flash with `software/IJOY Update installer.zip`.
- `.bin` + `IJOY Update.exe` (Avenger 270, Avenger Baby, CAPO 216, Captain 2): the tool is bundled.
- `.hex` + `IJOY_ISP V2.0.exe` (Diamond, Diamond Mini, EXO, PS2170): the tool is bundled.

Follow the `Upgrade instructions` image inside each package. Flashing is at your own risk.

## Not recovered

These were linked from the site at some point but are gone from both the site and the
Internet Archive:

- Captain PD270 firmware ver1.23 (`/upload/201706/07/201706071906507418.zip`)
- Captain PD270 firmware ver1.4 (`/upload/201706/20/201706201743319402.zip`)
- Captain PD270 firmware ver1.5, `.rar` packaging (`/upload/201708/12/201708122102238057.rar`; the `.zip` is here)
- IJOY MAXO firmware ver1.11 (`/upload/201611/03/201611031056236623.rar`)
- IJOY Update installer, 2016 `.rar` (`/upload/201609/10/201609101750052219.rar`; the `.zip` is here)
- IJOY logo `.rar` (`/upload/201712/09/201712091143471865.rar`)
- 2015 manuals at `/asolo/t160.zip`, `/reaper.zip`, `/solomini.zip` (T160 and Solo Mini manuals are here from other links)
- `flavor_list.xls`

Partial: `marketing/ijoycatalog.PARTIAL.zip` — the 2015 catalog; the Wayback copy is cut off
at 16.2 of 44.4 MB.

If you have any of these, please open an issue or a pull request.

## How it was collected

- **Live site.** The site's download handler `tools/download.ashx?id=N&type=1` serves files
  even after their links are removed from the pages; ids 1–400 were probed (live: 9–161).
  Older direct links under `/upload/` were taken from archived pages and fetched where still live.
- **Internet Archive.** All Wayback captures of `ijoycig.com/upload/*`, `tools/download.ashx*`
  and every file extension on the domain were listed via the CDX API, and ~1,500 archived pages
  (downloads, software, manuals, TPD, posters, logos, product pages) were scanned for links.
  Files missing from the live site were fetched from their exact Wayback capture.
- Archives were tested with `7z t`; PDFs and images were checked by signature.
- Other IJOY domains (ijoy-vape.com, ijoymall.com, ijoygroup.com, ijoyvapedirect.com,
  ijoyau.com) had nothing downloadable.

## Disclaimer

All files are © IJOY / Shenzhen IJOY Technology Co., Ltd. This is an unofficial archive kept for
preservation and for owners of discontinued devices. It is not affiliated with IJOY. If you are a
rights holder and want something removed, open an issue.

