# COVID-19-SG

Singapore and Malaysia COVID-19 data from multiple data sources such as zaobao.sg and MOH. This repository updates *every 10 minutes* if new data is available. New files for each day are created at 9 AM SGT.


## Description

- `cases`: information about each case. The content is maintained in a partial append-only manner, which means each file contains all information available at the date specified by file name. If one only the latest file is need, then the last file contains all information needed.
- `case_tags`: metatags for tag cases, The content also maintained in a partial append-only manner in order to align with cases file.
- `event`: important action taken by Singapore government. The content also maintained in a partial append-only manner in order to align with cases file.
- `groups`: meta information to group cases. The content also maintained in a partial append-only manner in order to align with cases file.
- `journeys`: records of activities and status of each case. The content is updated daily if status of the case is changed.
- `overview`: overview of cases in that day.
- `tracing`: numbers of how many suspect cases, suspect cases, close contacts and their status. The content also maintained in a partial append-only manner.
- `moh`: press releases from MOH. Three formats are offered:
  1. json format: raw MOH press release.
  2. html format: content extracted from json file.
  3. plain text format: actual content of the press release encoded in UTF-8.

  From March 18th, Singapore MOH posts case details in a separate pdf. They are downloaded and renamed to `date_original name`.
  From April 5th, Singapore MOH does not post case details any more. Instead a situation report is provided. These reports are downloaded and placed in `moh` folder as well.
- `malay`: press release from MOH of Malaysia.
- `who`: situation reports from WHO.


