
<!-- README.md is generated from README.Rmd. Please edit that file -->

<!-- -->

<!-- FILL OUT OPTIONS !!! -->

<!-- -->

<!-- -->

<!-- -->

# ‘CalDav’ Requests

**Status**

<a href="https://travis-ci.org/petermeissner/caldav"><img src="https://api.travis-ci.org/petermeissner/caldav.svg?branch=master"><a/>
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/petermeissner/caldav?branch=master&svg=true)](https://ci.appveyor.com/project/petermeissner/caldav)
<a href="https://codecov.io/gh/petermeissner/caldav"><img src="https://codecov.io/gh/petermeissner/caldav/branch/master/graph/badge.svg" alt="Codecov" /></a>
<a href="https://cran.r-project.org/package=caldav">
<img src="http://www.r-pkg.org/badges/version/caldav"> </a>
<img src="http://cranlogs.r-pkg.org/badges/grand-total/caldav">
<img src="http://cranlogs.r-pkg.org/badges/caldav">

*lines of R code:* 45, *lines of test code:* 0

**Version**

0.1.0 ( 2020-09-12 12:52:02 )

**Description**

A simple package for making ‘CalDav’ requests to retrieve calendar
information from servers.

**License**

MIT + file LICENSE <br>Peter Meissner \[aut, cre\]

**Citation**

``` r
citation("caldav")
```

``` r
Meissner P (2020). caldav: 'CalDav' Requests. R package version 0.1.0.
```

**BibTex for citing**

``` r
toBibtex(citation("caldav"))
```

    @Manual{,
      title = {caldav: 'CalDav' Requests},
      author = {Peter Meissner},
      year = {2020},
      note = {R package version 0.1.0},
    }

**Installation**

Stable version from CRAN:

``` r
install.packages("caldav")
```

<!-- Latest development version from Github: -->

<!-- ```{r, eval=FALSE} -->

<!-- devtools::install_github("user_name/repo_name") -->

<!-- ``` -->

**Usage**

*starting up …*

    library("caldav")

``` r
cal_data <- 
  caldav_get_all_simple_auth(
    url = "https://nextcloud03.webo.cloud/remote.php/dav/calendars/usah_nameahh/personal/",
    user = "usah_nameahh",
    password =  "*********"
  )

cat(cal_data$calendar[1])
## BEGIN:VCALENDAR
## CALSCALE:GREGORIAN
## VERSION:2.0
## PRODID:-//IDN nextcloud.com//Calendar app 2.0.3//EN
## BEGIN:VEVENT
## CREATED:20200904T111126Z
## DTSTAMP:20200907T200537Z
## LAST-MODIFIED:20200907T200537Z
## SEQUENCE:3
## UID:8d9e7fb1-ea44-4986-80bb-ab009924c27e
## DTSTART;TZID=Europe/Berlin:20200904T140026
## DTEND;TZID=Europe/Berlin:20200904T150026
## SUMMARY:Whatever
## RRULE:FREQ=WEEKLY;BYDAY=FR,WE
## END:VEVENT
## BEGIN:VTIMEZONE
## TZID:Europe/Berlin
## BEGIN:DAYLIGHT
## TZOFFSETFROM:+0100
## TZOFFSETTO:+0200
## TZNAME:CEST
## DTSTART:19700329T020000
## RRULE:FREQ=YEARLY;BYMONTH=3;BYDAY=-1SU
## END:DAYLIGHT
## BEGIN:STANDARD
## TZOFFSETFROM:+0200
## TZOFFSETTO:+0100
## TZNAME:CET
## DTSTART:19701025T030000
## RRULE:FREQ=YEARLY;BYMONTH=10;BYDAY=-1SU
## END:STANDARD
## END:VTIMEZONE
## END:VCALENDAR  
```
