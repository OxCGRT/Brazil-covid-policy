# Codebook for the Brazil Subnational Coding - Oxford Covid-19 Government Response Tracker

***Brazil Subnational Codebook version 1.0 <br/>01 May 2020***

This document is codebook for the coding of subnational units drawing on the Oxford Covid-19 Government Response Tracker ([GitHub repo](https://github.com/OxCGRT/covid-policy-tracker), [university website](https://www.bsg.ox.ac.uk/covidtracker)).

For Brazilian subnational units, we coded nine OxCGRT indicators organised into two groups:
- [C - containment and closure policies](#containment-and-closure-policies)
- [H - health system policies](#health-system-policies)

All nine indicators are recorded on an ordinal scale that represents the level of strictness of the policy. Eight of the indicators (C1-C7 and H1) also have a flag for whether they are targeted to a specific geographical region (flag=0) or whether they are a "general" policy that is applied across the whole state or city (flag=1).

### Containment and closure policies

| ID | Name | Description | Measurement | Coding |
| --- | --- | --- | --- | --- |
| C1 | `C1_School closing` | Record closings of schools and universities | Ordinal scale | 0 - no measures <br/>1 - recommend closing <br/>2 - require closing (only some levels or categories, eg just high school, or just public schools) <br/>3 - require closing all levels <br/>Blank - no data |
| | `C1_Flag` | | Binary flag for geographic scope | 0 - targeted <br/>1- general <br/>Blank - no data |
| C2 | `C2_Workplace closing` | Record closings of workplaces | Ordinal scale | 0 - no measures <br/>1 - recommend closing (or recommend work from home) <br/>2 - require closing (or work from home) for some sectors or categories of workers <br/>3 - require closing (or work from home) for all-but-essential workplaces (eg grocery stores, doctors) <br/>Blank - no data |
| | `C2_Flag` | | Binary flag for geographic scope | 0 - targeted <br/>1- general <br/>Blank - no data |
| C3 | `C3_Cancel public events` | Record cancelling public events | Ordinal scale | 0 - no measures <br/>1 - recommend cancelling <br/>2 - require cancelling <br/>Blank - no data |
| | `C3_Flag` | | Binary flag for geographic scope | 0 - targeted <br/>1- general <br/>Blank - no data |
| C4 | `C4_Restrictions on gatherings` | Record limits on private gatherings | Ordinal scale | 0 - no restrictions <br/>1 - restrictions on very large gatherings (the limit is above 1000 people) <br/>2 - restrictions on gatherings between 101-1000 people <br/>3 - restrictions on gatherings between 11-100 people <br/>4 - restrictions on gatherings of 10 people or less <br/>Blank - no data |
| | `C4_Flag` | | Binary flag for geographic scope | 0 - targeted <br/>1- general <br/>Blank - no data |
| C5 | `C5_Close public transport` | Record closing of public transport (including intercity transport)| Ordinal scale | 0 - no measures <br/>1 - recommend closing (or significantly reduce volume/route/means of transport available) <br/>2 - require closing (or prohibit most citizens from using it) <br/>Blank - no data |
| | `C5_Flag` | | Binary flag for geographic scope | 0 - targeted <br/>1- general <br/>Blank - no data |
| C6 | `C6_Stay at home requirements` | Record orders to "shelter-in-place" and otherwise confine to the home | Ordinal scale | 0 - no measures <br/>1 - recommend not leaving house <br/>2 - require not leaving house with exceptions for daily exercise, grocery shopping, and 'essential' trips <br/>3 - require not leaving house with minimal exceptions (eg allowed to leave once a week, or only one person can leave at a time, etc) <br/>Blank - no data |
| | `C6_Flag` | | Binary flag for geographic scope | 0 - targeted <br/>1- general <br/>Blank - no data |
| C7 | `C7_Restrictions on internal movement` | Record restrictions on internal movement between cities/regions <br/><br/>Note: this records city or state closure of internal borders preventing people from entering/exiting it | Ordinal scale | 0 - no measures <br/>1 - recommend not to travel between regions/cities <br/>2 - internal movement restrictions in place <br/>Blank - no data |
| | `C7_Flag` | | Binary flag for geographic scope | 0 - targeted <br/>1- general <br/>Blank - no data |
| C8 | `C8_International travel controls` | Record restrictions on international travel <br/><br/>Note: subnational units often don't have authority to ban international arrivals or close borders | Ordinal scale | 0 - no restrictions <br/>1 - screening arrivals <br/>2 - quarantine arrivals from some or all countries <br/>3 - ban arrivals from some countries <br/>4 - ban on all countries or total border closure <br/>Blank - no data |

### Health system policies

| ID | Name | Description | Measurement | Coding |
| --- | --- | --- | --- | --- |
| H1 | `H1_Public information campaigns` | Record presence of public info campaigns | Ordinal scale | 0 - no Covid-19 public information campaign <br/>1 - public officials urging caution about Covid-19 <br/>2- coordinated public information campaign (eg across traditional and social media) <br/>Blank - no data |
| | `H1_Flag` | | Binary flag for geographic scope |  0 - targeted <br/>1- general <br/>Blank - no data |

