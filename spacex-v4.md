## SpaceX API V4 Docs
[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/ed4ed700dcc55b2c1f1c)


## Base URL
`https://api.spacexdata.com/v4`

## Authentication

Authentication via api key is required for all destructive routes. This includes all `create`, `update`, and `delete` routes.

Authenticate by passing the header `spacex-key` with your api key. Protected routes return `401` without a valid key.

## Pagination + Custom Queries

All `/query` routes support pagination, custom queries, and other output controls.
See the [pagination + query](queries.md) guide for more details and examples.

## Popular queries
```pip install jq```

valuation
```bash
curl --location --request GET 'https://api.spacexdata.com/v4/company' | jq '.valuation'
```
launches
```bash
curl --location --request GET 'https://api.spacexdata.com/v4/launches' | jq
```
rockets
```bash
curl --location --request GET 'https://api.spacexdata.com/v4/rockets' | jq
```

### Capsules - [Schema](capsules/schema.md)

Detailed info for serialized dragon capsules

* [Get all capsules](capsules/all.md) : `GET /capsules`
* [Get one capsule](capsules/one.md) : `GET /capsules/:id`
* [Query capsules](capsules/query.md) : `POST /capsules/query`
* 🔒 [Create a capsule](capsules/create.md) : `POST /capsules`
* 🔒 [Update a capsule](capsules/update.md) : `PATCH /capsules/:id`
* 🔒 [Delete a capsule](capsules/delete.md) : `DELETE /capsules/:id`

### Company Info - [Schema](company/schema.md)

Detailed info about SpaceX as a company

* [Get company info](company/all.md) : `GET /company`
* 🔒 [Update company info](comapny/update.md) : `PATCH /company/:id`

### Cores - [Schema](cores/schema.md)

Detailed info for serialized first stage cores

* [Get all cores](cores/all.md) : `GET /cores`
* [Get one core](cores/one.md) : `GET /cores/:id`
* [Query cores](cores/query.md) : `POST /cores/query`
* 🔒 [Create a core](cores/create.md) : `POST /cores`
* 🔒 [Update a core](cores/update.md) : `PATCH /cores/:id`
* 🔒 [Delete a core](cores/delete.md) : `DELETE /cores/:id`

### Crew - [Schema](crew/schema.md)

Detailed info on dragon crew members

* [Get all crew members](crew/all.md) : `GET /crew`
* [Get one crew member](crew/one.md) : `GET /crew/:id`
* [Query crew members](crew/query.md) : `POST /crew/query`
* 🔒 [Create a crew member](crew/create.md) : `POST /crew`
* 🔒 [Update a crew member](crew/update.md) : `PATCH /crew/:id`
* 🔒 [Delete a crew member](crew/delete.md) : `DELETE /crew/:id`

### Dragons - [Schema](dragons/schema.md)

Detailed info about dragon capsule versions

* [Get all dragons](dragons/all.md) : `GET /dragons`
* [Get one dragon](dragons/one.md) : `GET /dragons/:id`
* [Query dragons](dragons/query.md) : `POST /dragons/query`
* 🔒 [Create a dragon](dragons/create.md) : `POST /dragons`
* 🔒 [Update a dragon](dragons/update.md) : `PATCH /dragons/:id`
* 🔒 [Delete a dragon](dragons/delete.md) : `DELETE /dragons/:id`

### Landpads - [Schema](landpads/schema.md)

Detailed info about landing pads and ships

* [Get all landpads](landpads/all.md) : `GET /landpads`
* [Get one landpad](landpads/one.md) : `GET /landpads/:id`
* [Query landpads](landpads/query.md) : `POST /landpads/query`
* 🔒 [Create a landpad](landpads/create.md) : `POST /landpads`
* 🔒 [Update a landpad](landpads/update.md) : `PATCH /landpads/:id`
* 🔒 [Delete a landpad](landpads/delete.md) : `DELETE /landpads/:id`

### Launches - [Schema](launches/schema.md)

Detailed info about launches

* [Get past launches](launches/past.md) : `GET /launches/past`
* [Get upcoming launches](launches/upcoming.md) : `GET /launches/upcoming`
* [Get latest launch](launches/latest.md) : `GET /launches/latest`
* [Get next launch](launches/next.md) : `GET /launches/next`
* [Get all launches](launches/all.md) : `GET /launches`
* [Get one launch](launches/one.md) : `GET /launches/:id`
* [Query launches](launches/query.md) : `POST /launches/query`
* 🔒 [Create a launch](launches/create.md) : `POST /launches`
* 🔒 [Update a launch](launches/update.md) : `PATCH /launches/:id`
* 🔒 [Delete a launch](launches/delete.md) : `DELETE /launches/:id`

### Launchpads - [Schema](launchpads/schema.md)

Detailed info about launchpads

* [Get all launchpads](launchpads/all.md) : `GET /launchpads`
* [Get one launchpad](launchpads/one.md) : `GET /launchpads/:id`
* [Query launchpads](launchpads/query.md) : `POST /launchpads/query`
* 🔒 [Create a launchpad](launchpads/create.md) : `POST /launchpads`
* 🔒 [Update a launchpad](launchpads/update.md) : `PATCH /launchpads/:id`
* 🔒 [Delete a launchpad](launchpads/delete.md) : `DELETE /launchpads/:id`

### Payloads - [Schema](payloads/schema.md)

Detailed info about launch payloads

* [Get all payloads](payloads/all.md) : `GET /payloads`
* [Get one payload](payloads/one.md) : `GET /payloads/:id`
* [Query payloads](payloads/query.md) : `POST /payloads/query`
* 🔒 [Create a payload](payloads/create.md) : `POST /payloads`
* 🔒 [Update a payload](payloads/update.md) : `PATCH /payloads/:id`
* 🔒 [Delete a payload](payloads/delete.md) : `DELETE /payloads/:id`

### Fairings - [Schema](fairings/schema.md)

Detailed info on SpaceX fairings

* [Get all fairings](fairings/all.md) : `GET /fairings`
* [Get one fairing](fairings/one.md) : `GET /fairings/:id`
* [Query fairings](fairings/query.md) : `POST /fairings/query`
* 🔒 [Create a fairing](fairings/create.md) : `POST /fairings`
* 🔒 [Update a fairing](fairings/update.md) : `PATCH /fairings/:id`
* 🔒 [Delete a fairing](fairings/delete.md) : `DELETE /fairings/:id`

### Roadster info - [Schema](roadster/schema.md)

Detailed info about Elon's Tesla roadster's current position

* [Get roadster info](roadster/get.md) : `GET /roadster`
* [Query roadster info](roadster/query.md) : `POST /roadster/query`
* 🔒 [Update roadster info](roadster/update.md) : `PATCH /roadster/:id`

### Rockets - [Schema](rockets/schema.md)

Detailed info about rocket versions

* [Get all rockets](rockets/all.md) : `GET /rockets`
* [Get one rocket](rockets/one.md) : `GET /rockets/:id`
* [Query rockets](rockets/query.md) : `POST /rockets/query`
* 🔒 [Create a rocket](rockets/create.md) : `POST /rockets`
* 🔒 [Update a rocket](rockets/update.md) : `PATCH /rockets/:id`
* 🔒 [Delete a rocket](rockets/delete.md) : `DELETE /rockets/:id`

### Ships - [Schema](ships/schema.md)

Detailed info about ships in the SpaceX fleet

* [Get all ships](ships/all.md) : `GET /ships`
* [Get one ship](ships/one.md) : `GET /ships/:id`
* [Query ships](ships/query.md) : `POST /ships/query`
* 🔒 [Create a ship](ships/create.md) : `POST /ships`
* 🔒 [Update a ship](ships/update.md) : `PATCH /ships/:id`
* 🔒 [Delete a ship](ships/delete.md) : `DELETE /ships/:id`

### Starlink - [Schema](starlink/schema.md)

Detailed info about Starlink satellites and orbits

Includes raw orbit data from [Space Track](https://www.space-track.org/auth/login), updated hourly.

Space Track data adheres to the standard for [Orbit Data Messages](https://public.ccsds.org/pubs/502x0b2c1.pdf)

* [Get all Starlink sats](starlink/all.md) : `GET /starlink`
* [Get one Starlink sat](starlink/one.md) : `GET /starlink/:id`
* [Query Starlink sats](starlink/query.md) : `POST /starlink/query`
* 🔒 [Create a Starlink sat](starlink/create.md) : `POST /starlink`
* 🔒 [Update a Starlink sat](starlink/update.md) : `PATCH /starlink/:id`
* 🔒 [Delete a Starlink sat](starlink/delete.md) : `DELETE /starlink/:id`

### History - [Schema](history/schema.md)

Detailed info on SpaceX historical events

* [Get all historical events](history/all.md) : `GET /history`
* [Get one historical event](history/one.md) : `GET /history/:id`
* [Query historical events](history/query.md) : `POST /history/query`
* 🔒 [Create a historical event](history/create.md) : `POST /history`
* 🔒 [Update a historical event](history/update.md) : `PATCH /history/:id`
* 🔒 [Delete a historical event](history/delete.md) : `DELETE /history/:id`