NEUSEBIRDS + SEPARATE PHOTO CREDITS

NeuseBirds is a personal viewer for BirdWeather station 22946 (Neuse River).
BirdWeather remains the data source; this app is not an official BirdWeather product.

Unzip this entire folder. Double-click index.html to open it in Brave.
No server, installation, account, token, dependencies or Terminal required.

The small Credits link at the bottom opens credits.html in a NEW TAB, leaving
viewer filters, period and auto-refresh state untouched in the original tab.
Keep all three files together. Credits can also be opened directly (defaults
to rolling 24 hours). Its Back link opens index.html in that credits tab.

The viewer has no photo-credit overlays or info buttons. Photos still open
species Wikipedia articles in a new tab. Cards and table thumbnails remain.
The Credits page shows readable photographer, license and image-source details
for every species in the chosen period, not merely search-filtered species.
It fetches current public BirdWeather metadata on opening, so new species are
included. A saved rolling-24-hour snapshot remains visible on fetch failure
and is clearly labeled; it is not relabeled Today. Missing authors/licenses
are honestly marked unavailable. Images are displayed even without credit
metadata. Unsafe or absent URLs and failed images use placeholders.

Last 24 hours remains the default. Today uses America/New_York midnight until
each request time, including DST transitions, independent of computer timezone.
Changing period updates the Credits link's period too. Refresh now and automatic
refresh (default 5 minutes, any integer 1–1440, or off) work as before. Invalid
intervals pause automatic refresh. Browser background throttling and computer
sleep can delay timers. Fetch errors retain last-good data and its true window.
Switching period during a fetch discards stale results without overlapping
requests. Search, sort and Cards/Table selections survive refreshes.

Data is automated detection activity, not individual birds or verified human
sightings. Full species coverage; no extra score filter. Photos illustrate species,
not photographs taken at this station. Main included real snapshot retrieved 2026-11-08 12:03:22 PM Eastern;
see its on-page species/detection totals. Credits retains its separately labeled
November 8, 2026, 11:04:52 AM Eastern fallback snapshot.
Live results and settings live in the browser tab only; no HTML files are
rewritten. No observation/media archive, offline photo guarantee or database.

Public API documentation: https://app.birdweather.com/api/
Endpoint: https://app.birdweather.com/graphql (no credentials).
Photo/Wikipedia metadata: documented Species fields imageUrl, thumbnailUrl,
imageCredit, imageLicense, imageLicenseUrl, wikipediaUrl. The live public
InputDuration schema supports exact date-times plus timezone; Today sends
from=Eastern-dateT00:00:00, to=current UTC ISO timestamp, timezone=America/New_York.
API-provided author HTML is reduced to inert text and validated links, never
inserted as HTML. Links/images use safe HTTPS URLs. No extra libraries/fonts,
analytics, precise coordinates or secrets. Images load from remote API-provided
hosts; attribution remains that of the respective creators.
Independent implementation inspired by Tweet Sheet; not copied source.
Automated DOM/fetch/timer checks are not real browser visual QA.

CARD COUNT AND MOST RECENT
Card detection counts are now badges over the photo; table counts are unchanged.
Most recent sorts by each species' actual latest station-22946 detection within
the displayed exact window, newest first; missing/invalid dates sort last.
Ties sort by name. It uses documented detections(first:1, stationIds:[22946],
speciesId:..., period:...) with newest-first ordering verified on the live API.
There is no aggregate latest field on SpeciesCount. Lookups are sequential
batches of at most three aliases, respecting the API limit, on every refresh
so all views can display true station-specific last-heard ages.
Latest times are cached only for the current snapshot/window; a fresh refresh
invalidates them. Failed lookups keep the last good data and report that recent
sorting is unavailable. The entire refresh has a 120-second deadline (30 seconds per request).
Rolling windows are frozen exact 24-hour timestamps, shared by counts and all
latest lookups. Today retains exact Eastern midnight-to-request-time behavior.

CARD FOOTER LINKS
Wiki: BirdWeather-provided English Wikipedia article.
ebird: BirdWeather-provided eBird species overview.
Sightings: worldwide eBird map using the API-provided ebirdCode. This is a
verified eBird map route, not a confirmed copy of Tweet Sheet's exact target;
no station coordinates are supplied.
BW: BirdWeather-provided species page.
Images: Brave image search for the common plus scientific name, not Google.
All open new tabs and have descriptive tooltips. Missing/unsafe service metadata
shows an unavailable label rather than a fabricated species URL. Table view
remains unchanged. Built-in count/latest snapshot time is unchanged; eBird
link metadata was separately refreshed from the public allSpecies query.

LAST HEARD
Cards and table rows show the age of each bird's actual latest station
detection in the selected window. Under an hour, age is rounded to the nearest
minute (0 minutes says just now). From one hour through exactly 24 hours, it is rounded to the
nearest whole hour. Above 24 hours, it is rounded to the nearest whole elapsed
day (1 day ago / N days ago), not calendar days. Invalid, missing or future timestamps say unavailable.
A minute timer and returning to the visible tab update existing age text only,
even with auto-refresh off; they never request data or recreate photos/links.
Every data refresh now loads latest times in bounded batches for all sorts.
Sort/search/view changes make no extra web requests. The included timestamps
remain tied to the genuine saved snapshot; no retrieval time is substituted.

LAYOUT
Sort options: Most detections, Most recent, Name A-Z. Toolbar order is Time Period,
Sort, View, Search species, Refresh. Both pages use Tweet Sheet's verified
light paper base color #f9f3e4 (not its texture or radial-gradient shading):
https://tweetsheet.app/assets/index-DisDh1UW.css
:root --paper; body background-color: var(--paper).

THEME REFINEMENT
Tweet Sheet's verified #f9f3e4 paper color now covers both pages' cards,
toolbars, fields, ordinary buttons, table/header and placeholder/empty areas
as well as page backgrounds. Functional green accents and photo content stay
unchanged. Search text and its placeholder are italic. Historical period controls are described below.

HISTORICAL PERIODS
The selector now includes Last 7 days, Last 30 days and Last 365 days. These
are rolling exact 24-hour-day windows ending at request time, not previous
calendar weeks/months/years. Today remains Eastern midnight-to-now.
Both viewer and Credits request 200 species initially; if aggregate counts
report more, they request that full count with the same frozen window.
Species coverage and summed detection totals are checked before replacing
the last good snapshot. Incomplete/API-limited data reports an error rather
than silently truncating. No 100-species display cap remains.
Historical lists need more sequential last-heard batches; progress is shown.
Updates allow 120 seconds overall and 30 seconds per individual request,
with no automatic retry on rate limits. Sorting/searching and minute age
updates still make no requests. The API reports station history beginning
February 19, 2026; a 365-day query only includes available recorded history,
not proof of an uninterrupted full year. No local archive is needed or made.

Some historical aggregate species may have no matching retrievable latest
detection; those keep their totals and say Last heard unavailable, never an
invented timestamp.

TWO-PHASE UPDATES
Complete, validated totals and the species list appear immediately, with the
correct window and aggregate-completion timestamp. Last-heard times then load
in small batches without recreating cards or photos as each batch arrives.
If optional timestamp enrichment fails, the NEW totals remain visible; known
times stay accurate and unqueried times say unavailable. Most recent sorting
only becomes ready after every lookup batch finishes; meanwhile it explicitly
displays count order. An aggregate-query failure still preserves the previous
snapshot. Progress and timeout messages distinguish these cases.
