# Datasets for COVID-19 in Singapore and Malaysia
*Updates every 10 minutes*

![COVID-19 Singapore & Malaysia](./covid-sg.png)

This repository collects Singapore and Malaysia COVID-19 data from multiple data sources such as zaobao.sg and MOH. The updating frequency is *10 minutes*. New files for each day are created at 9 AM SGT. From April 7th, daily files are created at 1 AM SGT for more frequent checking of the status. From April 19th, daily files are created at 12 AM SGT because two days' press releases were updated after 12 AM SGT. From June 1, 2020, Zaobao stopped updating the data. Only Singapore MOH data will be updated.

## What is in this repository

Clearly, this repository provides information about Singapore and Malaysia COVID-19. However, we believe that the full tracking records of when and what information are available to general public is a more interesting piece of information. And thus, we tried to use `git` as a tool to show what has been changed in the press release files throughout the time line, when were these press release files became public available. By combining these information, we believe one can form a more complete picture about the reactions of government in this outbreak.

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

  From April 7th, Singapore MOH resumed posting case details. Meanwhile, case details for April 5th and 6th are also uploaded.

- `malay`: press release from MOH of Malaysia.
- `who`: situation reports from WHO.

<hr/>

We hope the world will back to normal as soon as possible.

Many thanks to NTU and UrbanDotSolution for providing the machine to host the updating scripts.

