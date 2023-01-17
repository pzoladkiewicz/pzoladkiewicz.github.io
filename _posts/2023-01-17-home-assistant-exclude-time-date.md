---
title: Exclude Time & Date (ISO)
date: 2023-01-17 12:36
categories: [home-assistant]
tags: [tips]
---

# Q: How to exclude Time \& Date from the Logbook?

We can exclude entities from the [logbook](https://home-assistant.io/components/logbook/) or better exlude them from the [recorder](https://www.home-assistant.io/integrations/recorder/), so your database won't be spamed with them.

All you need is add configuration variables to **configuration.yaml**

```yaml
recorder:
  #db_url: !secret your_db  -- if you got other than standard
  exclude:
    entities:
      - sensor.date_time_iso
```