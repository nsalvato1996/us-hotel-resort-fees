# US hotel resort fees, as each hotel states them

What 2,703 hotels in 62 US cities and towns say on
their own websites (or their brand's) about a mandatory nightly resort,
destination, amenity or facility fee. Every answer carries the page it came
from and the day it was read; a hotel whose site could not be read, or did
not say, is listed as unconfirmed. Read through 2026-10-10.

| | Hotels |
|---|---:|
| State a mandatory fee | 502 |
| State they charge none | 81 |
| Could not be confirmed | 2120 |

Maintained by [NJSTravel](https://njstravel.com), a US hotel booking site that ranks every
hotel by its true total price. How each row is read and checked:
[https://njstravel.com/methodology](https://njstravel.com/methodology). Every city has a page:
[https://njstravel.com/hotels](https://njstravel.com/hotels).

## Files

- `data/resort-fees.csv`: one row per hotel, the same file as
  [https://njstravel.com/data/resort-fees.csv](https://njstravel.com/data/resort-fees.csv).
- `data/resort-fees.json`: the same rows grouped by city, with the hotel's
  verbatim quote for each stated fee. Fees are integer cents.

## Reading it

- **Per night, before tax.** A fee is the figure the hotel states, per night,
  before any tax it says it adds on top (`taxed_on_top`).
- **`unconfirmed` is not "no fee".** The hotel's site could not be read, or
  it did not state the fee. Never count these as zero.
- **A condition is printed, never applied.** `conditions` holds a waiver or
  discount in the hotel's words (booked direct, long stays); the figure is the
  fee as stated.
- **A second charge is listed, never summed** (`also_charges`), in the
  hotel's words, because not every such sentence gives a per-night basis.
- **Dates matter.** Hotels change fees. Cite a row with its `checked_on`.

## Licence and credit

[Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/).
Use it, republish it, build on it; credit **NJSTravel** and link
[https://njstravel.com/methodology](https://njstravel.com/methodology).

Corrections: help@njstravel.com, with the page that shows the hotel's
current fee.
