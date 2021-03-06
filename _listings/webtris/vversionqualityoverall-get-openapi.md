---
swagger: "2.0"
x-collection-name: WebTRIS
x-complete: 0
info:
  title: WebTRIS Traffic Flow API Get Site OverallQuality
  version: 1.0.0
  description: Get site overallquality.
host: webtris.highwaysengland.co.uk
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v{version}/sites:
    get:
      summary: Get a list of sites
      description: Get a list of sites.
      operationId: Sites_Index
      x-api-path-slug: vversionsites-get
      parameters:
      - in: path
        name: version
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Sites
  /v{version}/sites/{site_Ids}:
    get:
      summary: Get selected sites
      description: Get selected sites.
      operationId: Sites_Index
      x-api-path-slug: vversionsitessite-ids-get
      parameters:
      - in: path
        name: site_Ids
        description: site id
      - in: path
        name: version
      responses:
        200:
          description: OK
      tags:
      - Selected
      - Sites
  /v{version}/quality/overall:
    get:
      summary: Get Site OverallQuality
      description: Get site overallquality.
      operationId: Quality_GetOverallDataQualityForSites
      x-api-path-slug: vversionqualityoverall-get
      parameters:
      - in: query
        name: end_date
        description: The end date of the report in the format ddmmyyyy (i
      - in: query
        name: sites
        description: Get site quality by site id delimited by ,
      - in: query
        name: start_date
        description: The start date of the report in the format ddmmyyyy (i
      - in: path
        name: version
      responses:
        200:
          description: OK
      tags:
      - Site
      - OverallQuality
  /v{version}/quality/daily:
    get:
      summary: Get Site DailyQuality
      description: Get site dailyquality.
      operationId: Quality_GetDailyDataQualityForSite
      x-api-path-slug: vversionqualitydaily-get
      parameters:
      - in: query
        name: end_date
        description: The end date of the report in the format ddmmyyyy (i
      - in: query
        name: siteId
      - in: query
        name: start_date
        description: The start date of the report in the format ddmmyyyy (i
      - in: path
        name: version
      responses:
        200:
          description: OK
      tags:
      - Site
      - DailyQuality
  /v{version}/sitetypes:
    get:
      summary: Return list of site types
      description: Return list of site types.
      operationId: SiteTypes_Index
      x-api-path-slug: vversionsitetypes-get
      parameters:
      - in: path
        name: version
      responses:
        200:
          description: OK
      tags:
      - Return
      - List
      - Of
      - Site
      - Types
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---