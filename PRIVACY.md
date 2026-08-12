# Privacy Policy — SeenIt

_Last updated: 12 August 2026_

Applies to Airbnb and Yad2, the sites the extension supports.

SeenIt does not collect, transmit, sell, or share any data. There is no backend, no analytics,
and no telemetry.

## What the extension stores

Only on your own computer, in the browser's local extension storage (`chrome.storage.local`):

- the listing IDs of listings you opened or hid, and which site each came from
  (Airbnb IDs are numeric; Yad2 IDs are alphanumeric tokens)
- for each one: whether it is marked seen or hidden, when it was first and last seen, how many
  times you opened it, how long you spent on it, and the listing title as shown in the page's
  own metadata
- your appearance and threshold preferences

This data never leaves your browser. Uninstalling the extension deletes it. "Reset all" in the
popup deletes it on demand, and the reset button on an individual card deletes that one record.

## Network activity

None. The extension makes no network requests of any kind.

## Permissions and why they are needed

- **storage** — to remember which listings you already viewed, locally.
- **Host access to Airbnb's country domains and yad2.co.il** — to read listing IDs from links and
  dim cards on those two sites. No other site is accessed. Airbnb serves a separate domain per
  country, and Chrome match patterns cannot use a wildcard top-level domain, so each consumer
  country domain is listed explicitly rather than requesting access to all websites.
  - On Airbnb, the extension runs only on search, wishlist, and listing pages.
  - On Yad2, listing cards appear across many verticals and the homepage, so the extension is
    allowed on the whole `yad2.co.il` domain. It only acts when listing links are present; account,
    messaging, and payment pages with no listing cards are left alone. Time-on-page tracking runs
    only on item detail pages.

## Contact

Open an issue at [github.com/NadavM-ux/seenit-public/issues](https://github.com/NadavM-ux/seenit-public/issues).
