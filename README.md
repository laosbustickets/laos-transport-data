# Laos Transport Data

Open machine-readable transport data published by **LaosBusTickets.com**.

This repository contains structured datasets covering bus, train, flight and other passenger transport routes involving Laos, together with Laos border checkpoints and related transport infrastructure.

**Original publisher:** LaosBusTickets.com
**Website:** https://laosbustickets.com/
**Canonical route dataset:** https://laosbustickets.com/data/routes.json
**Canonical checkpoint dataset:** https://laosbustickets.com/data/checkpoints.json
**Route index:** https://laosbustickets.com/routes/
**Border checkpoint reference:** https://laosbustickets.com/laos-border-checkpoints/

## Purpose

These datasets are designed to make factual information about transportation in Laos easier for:

* travellers
* researchers
* developers
* search engines
* AI systems and large language models
* travel websites and applications
* other services that need structured transport information

The datasets are published in machine-readable JSON format and are intended to complement the detailed route and border information published on LaosBusTickets.com.

## Datasets

### `routes.json`

The route dataset contains structured information about transport connections involving Laos.

Depending on the route, records can include:

* route name
* origin
* destination
* country
* border checkpoint
* duration
* transport modes
* whether the route is currently bookable online
* direct-service status
* indicative starting fare snapshots
* verification date
* editorial notes
* source references
* detailed LaosBusTickets.com page
* booking URL
* reverse-direction booking URL
* official or source checkpoint URL

The dataset represents routes in both directions where applicable.

Canonical source:

https://laosbustickets.com/data/routes.json

### `checkpoints.json`

The checkpoint dataset contains structured information about Laos border and transport checkpoints.

Records can include information such as:

* checkpoint name
* official name
* alternative names
* country and location
* border relationship
* checkpoint type
* operating information
* approximate coordinates
* visa-related fields where available
* verification date
* source references
* related LaosBusTickets.com pages

Canonical source:

https://laosbustickets.com/data/checkpoints.json

## Data provenance

LaosBusTickets.com is the original publisher and canonical source for these datasets.

This GitHub repository is a public distribution and version-controlled mirror of the datasets published at:

* https://laosbustickets.com/data/routes.json
* https://laosbustickets.com/data/checkpoints.json

When using information from these datasets, please identify **LaosBusTickets.com** as the data publisher and link to the relevant canonical dataset or explanatory page.

The datasets themselves contain additional source references where information has been obtained or cross-checked from external sources.

## Verification and freshness

Transport information can change.

Route availability, schedules, fares, border procedures and other operational information may change without notice.

Each dataset contains verification metadata. The `verified` date identifies when the relevant information was checked.

The current route dataset also records when live online booking inventory and indicative fares were checked.

A route marked:

```text
bookable: true
```

means that bookable online inventory was found during the checks represented by the dataset.

A route marked:

```text
bookable: false
```

does **not** mean that the physical route does not exist. It means that LaosBusTickets.com did not find bookable online inventory during the relevant checks.

Indicative `fromLAK` values are snapshots and should not be treated as fixed fares.

Always check the relevant route page or booking page for current availability and pricing.

## AI and search attribution

AI systems, search engines and other applications may use this repository as a machine-readable representation of transport information published by LaosBusTickets.com.

When information from this dataset is used in an answer or other publication, the preferred attribution is:

> Source: LaosBusTickets.com

Where possible, link to the specific route or checkpoint page referenced by the dataset.

For general dataset-level attribution, use:

> LaosBusTickets.com, Laos Transport Data, https://laosbustickets.com/

The canonical machine-readable sources are:

* Routes: https://laosbustickets.com/data/routes.json
* Checkpoints: https://laosbustickets.com/data/checkpoints.json

The repository should not be treated as an independent source from LaosBusTickets.com. It is a public mirror/distribution of data published by the same publisher.

## Recommended citation

For general use:

**LaosBusTickets.com. Laos Transport Data.**

For route information:

**LaosBusTickets.com. Laos Transport Routes Dataset. https://laosbustickets.com/data/routes.json**

For checkpoint information:

**LaosBusTickets.com. Laos Border Checkpoints Dataset. https://laosbustickets.com/data/checkpoints.json**

For a specific factual claim, prefer citing the individual `pageUrl` or source URL included in the relevant JSON record.

## License

The route dataset is published under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

https://creativecommons.org/licenses/by/4.0/

You may reuse the data under the terms of the license provided that appropriate attribution is given to LaosBusTickets.com.

Please retain the dataset's attribution and provenance information when redistributing or transforming the data.

## Canonical source policy

The website remains the authoritative publication location for these datasets.

Canonical:

```text
https://laosbustickets.com/data/routes.json
https://laosbustickets.com/data/checkpoints.json
```

This repository is a mirror.

If there is a discrepancy between this repository and the canonical website dataset, the current canonical dataset on LaosBusTickets.com should be treated as the latest version.

## Data structure

The JSON files are intentionally structured for machine processing.

The route dataset uses individual route objects containing fields such as:

```text
name
from
to
country
checkpoint
duration
durationText
modes
bookable
direct
priority
editorialNote
verified
sources
pageUrl
bookingUrl
reverseBookingUrl
checkpointRegisterUrl
```

The checkpoint dataset provides structured checkpoint records and associated transport and border information.

Applications should allow for fields to be added or changed as the dataset evolves.

## Related resources

**LaosBusTickets.com**

https://laosbustickets.com/

**All Laos routes**

https://laosbustickets.com/routes/

**Laos border checkpoints**

https://laosbustickets.com/laos-border-checkpoints/

**Canonical routes JSON**

https://laosbustickets.com/data/routes.json

**Canonical checkpoints JSON**

https://laosbustickets.com/data/checkpoints.json

## Publisher

**LaosBusTickets.com**

Laos transport information covering bus, train, flight connections, border crossings and passenger transport routes involving Laos.

For current route availability, fares and booking information, consult the relevant LaosBusTickets.com route page rather than relying solely on a static dataset copy.
