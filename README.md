NEUSEBIRDS + SEPARATE PHOTO CREDITS

NeuseBirds is a personal viewer for BirdWeather station 22946 (Neuse River).
BirdWeather remains the data source; this app is not an official BirdWeather product.

Unzip this entire folder. Double-click index.html to open it in Brave.
No server, installation, account, token, dependencies or Terminal required.

credits.html remains available by direct URL only (not linked from the main page;
defaults to rolling 24 hours when opened that way). Its Back link opens index.html.
Keep the files together if you also use the Credits page.

The viewer has no photo-credit overlays or info buttons. Photos still open
species Wikipedia articles in a new tab. Cards and table thumbnails remain.
The Credits page shows readable photographer, license and image-source details
for every species in the chosen period, not merely search-filtered species.
It fetches current public BirdWeather metadata on opening, so new species are
included. A saved rolling-24-hour snapshot remains visible on fetch failure
and is clearly labeled; it is not relabeled Today. Missing authors/licenses
are honestly marked unavailable. Images are displayed even without credit
metadata. Unsafe or absent URLs and failed images use placeholders.

Today is the default Time Period (still computed from America/New_York midnight until
each request time, including DST transitions, independent of computer timezone).
Most recent is the default Sort. 24 hours remains available in the list.
The auto-refresh line shows the last-updated time to the minute (Eastern, no
seconds or zone label; the embedded snapshot first paints as “Updated 12:03 PM”),
then Auto-refresh every [minutes], then Refresh now (moved off the toolbar).
Refresh now and automatic
refresh (default 5 minutes, any integer 1–99, or off) work as before. The
minutes field is a short text box (no stepper arrows); non-digits are stripped
as you type. Empty or 0 values fall back to the previous or default interval. Browser background throttling and computer
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
Species cards use tighter vertical spacing in the text block (name,
scientific name, last-heard line, and pills), with font sizes, photos,
and count badges unchanged.
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

SPECIES PAGE
Clicking a species name, card, table row, or the bird’s photo (in cards
or the table) opens a detail view at #species/<id> (slugs such as
#species/belted-kingfisher also work). The Wiki pill still goes to
Wikipedia. The browser back button and a “← All species” link return to
the list and keep the current period, sort, view, and search where
practical. The page stays on station 22946. It shows the official
BirdWeather photo, the same Wiki / eBird / Sightings / BW / Images pills,
and the Wikipedia summary with a Read more link. Photo credit is not
shown on the species page.
Time of day, then Calendar, then Recordings. The hour chart heading reads
“Detections by hour of day for today”, “for last week”, “for past month”,
“for past year”, or “for all time”, with past windows worded “for that
day/week/month/year” and the date shown beside the period control. The
period list includes All time (station earliest detection through now;
arrows are hidden, as on the main list). The hour chart’s X axis is
labeled every three hours as 12a, 3a, 6a, 9a, 12p, 3p, 6p, and 9p,
starting at 12:00a and ending at 9p, unless a detection falls after
9 pm; then the last tick is the hour after that last detection and is
labeled too. Bars and ticks share that scale, with tick marks at hour
boundaries so a 6:00–6:30 bar starts at the 6a tick. Integer Y-axis
ticks still use a nice step. The detection count sits in the chart’s
upper-right corner. A “≥7.0 score” label is not shown; the hour chart
and recordings still use a score 7.0 or higher filter.
The calendar heatmap uses unfiltered daily counts, with first seen / peak /
still present or departed (days with more than 3 detections; departure is
hidden if anything was heard in the last 14 days; “first seen” if that falls
on the station’s first day, 2026-02-19), plus Today, this week, year-to-date,
and all-time totals. The calendar states that it is not score-filtered.
Recordings default to score 7.0 or higher, with most recent or highest
score sort, ten clips at a time, and Show more. Times are Eastern
(“Nov 11, 2026, 10:43 AM”). Clips are FLAC from BirdWeather. The page
fetches each clip and decodes it in the browser with a vendored copy of
libflacjs (MIT; based on the FLAC reference decoder, BSD) to a WAV blob
played in a normal audio element, so playback does not depend on the
browser’s FLAC support. If decoding fails, native FLAC playback is tried
when the browser reports support, otherwise a download link is offered.
Only one clip plays at a time, and a short loading state is shown. There
is no spectrogram and no worldwide map. See libflacjs.LICENSE.

LAYOUT
Sort options: Most detections (optional), Most recent (default), Name A-Z. ◀ and ▶ buttons beside the title date step back and forward by the selected Time Period
(Today is calendar days in Eastern Time; 24 hours, week, month and year are rolling windows).
The forward control is disabled on the live window, and the back control stops at the
station’s first detection (2026-02-19). All time hides the arrows. Changing Time Period
returns to the live window; auto-refresh runs only there. Past Today headings read
“Species heard that day”; past 24 hours / week / month / year read “in those 24 hours”
or “that week/month/year”. Week, month and year dates use a compact range.
Toolbar order is Time Period,
Sort, View, Search species. Both pages use Tweet Sheet's verified
light paper base color #f9f3e4 (not its texture or radial-gradient shading):
https://tweetsheet.app/assets/index-DisDh1UW.css
:root --paper; body background-color: var(--paper).

THEME REFINEMENT
Tweet Sheet's verified #f9f3e4 paper color now covers both pages' cards,
toolbars, fields, ordinary buttons, table/header and placeholder/empty areas
as well as page backgrounds. Functional green accents and photo content stay
unchanged. Search text and its placeholder are italic. Historical period controls are described below.

HISTORICAL PERIODS
The selector now includes week, month, year and all time. Week, month and year
are rolling exact 24-hour-day windows ending at request time, not previous
calendar weeks/months/years. All time covers the station's first detection
through request time (a safe early date is used until that timestamp is known).
Today remains Eastern midnight-to-now. The heading for all time is
“Species heard all time.”
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


ARRIVALS AND MISSING
Tabs under the title switch between Species (the main list), Arrivals and
Missing. Idea from Tweet Sheet (https://tweetsheet.app/arrivals), using the
same public BirdWeather topSpecies data; day boundaries are America/New_York.
Arrivals: This week (heard the past 7 days, fewer than 3 detections the 7
days before), This month (past 30 vs prior 30), This year (not in any of the
prior 3 calendar years) and Coming soon? (heard in the next 4 weeks of earlier
years, not yet this year). A species needs at least 3 detections to count as
heard. Missing: Vs last week and Vs last month (heard before, under 3
detections the past 7 days) and Vs previous years (at least 20 detections the
same week, +/-7 days, in any of the last 3 years). Comparisons that would
reach before the station's first detection (February 19, 2026) are skipped
and explained instead of queried. Each tab is one API request, cached for
10 minutes. Species links open the species page at the top; Back returns to
the same tab.
