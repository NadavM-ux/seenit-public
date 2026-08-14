# Privacy Policy — SeenIt

_Last updated: 14 August 2026_

Applies to Airbnb, Yad2, and Booking.com, the sites the extension supports.

SeenIt does not collect, transmit, sell, or share any data. There is no backend, no analytics,
and no telemetry.

## What the extension stores

Only on your own computer, in the browser's local extension storage (`chrome.storage.local`):

- the listing IDs of listings you opened or hid, and which site each came from
  (Airbnb IDs are numeric; Yad2 IDs are alphanumeric tokens; Booking.com IDs are country/slug)
- for each one: whether it is marked seen or hidden, when it was first and last seen, how many
  times you opened it, how long you spent on it, and the listing title as shown in the page's
  own metadata
- your appearance, dwell-threshold, and auto-forget preferences

This data never leaves your browser. Uninstalling the extension deletes it. "Reset all" in the
popup deletes it on demand, and the reset button on an individual card deletes that one record.
Seen listings can also expire locally after 1 hour, 12 hours, or 24 hours if you turn that
option on; hidden listings are never auto-removed.

## Network activity

None. The extension makes no network requests of any kind.

## Permissions and why they are needed

- **storage** — to remember which listings you already viewed, locally.
- **Host access to Airbnb's country domains, yad2.co.il, and booking.com** — to read listing IDs
  from links and dim cards on those sites. No other site is accessed. Airbnb serves a separate
  domain per country, and Chrome match patterns cannot use a wildcard top-level domain, so each
  consumer country domain is listed explicitly rather than requesting access to all websites.
  - On Airbnb, content scripts run only on the homepage (`/` and its Homes tab, `/homes`),
    search (`/s/`), wishlist (`/wishlists/`), and listing (`/rooms/`) paths.
  - On Yad2, listing cards appear across many verticals and the homepage, so the grid script is
    allowed on the whole `yad2.co.il` domain. It only acts when listing links are present; account,
    messaging, and payment pages with no listing cards are left alone. Detail dwell tracking runs
    on item pages (`/item/…` and `/…/item/…`).
  - On Booking.com, listing cards appear on search (including localized filenames such as
    `/searchresults.he.html`), city and country pages, and carousels, so the grid script is
    allowed on the whole `booking.com` domain and only acts when `/hotel/…` listing links are
    present. Detail dwell tracking runs on hotel pages (`/hotel/…`).

## Contact

Open an issue at [github.com/NadavM-ux/seenit-public/issues](https://github.com/NadavM-ux/seenit-public/issues).
The extension source is private; that public repo is homepage, privacy, and support only.
