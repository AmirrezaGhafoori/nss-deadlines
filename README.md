# Networking, Systems & Security Conference Deadlines

**🌐 Live Site**: [https://amirrezaghafoori.github.io/nss-deadlines/](https://amirrezaghafoori.github.io/nss-deadlines/)

Countdown timers for academic conference deadlines targeted by the **Networks and Systems Security Lab (NSSL)**.

This project is forked from [Security and Privacy deadlines](https://github.com/sec-deadlines/sec-deadlines.github.io) project and customized for our lab's research focus areas.

## About This Project

This website tracks deadlines for **24 conferences** that are commonly targeted by researchers in the Networks and Systems Security Lab (NSSL). The conferences cover our main research areas:

- **Networking** - Top-tier networking conferences
- **Wireless** - Wireless and mobile systems conferences  
- **Systems** - Systems and distributed computing conferences
- **Security** - Security and privacy conferences
- **Top 4** - The most prestigious conferences in our field

## Conference Categories

Our conferences are organized into the following types:
- **NETWORKING** - Networking and communication protocols
- **WIRELESS** - Wireless, mobile, and IoT systems
- **SYSTEMS** - Operating systems, distributed systems, and computer architecture
- **SECURITY** - Security, privacy, and cryptography
- **TOP4** - The top-tier conferences (includes networking + security flagships)
- **CONF** - Conference venues (as opposed to workshops)

## Adding/Updating a Conference

Want to suggest a new conference or update existing information? We welcome contributions!

1. **Check the scope**: Ensure the conference aligns with NSSL's research areas (networking, wireless, systems, security)
2. **Update the data**: Modify `_data/conferences.yml` following the format below
3. **Submit a pull request**: Send us your changes for review

Please check if an entry for a prior year already exists and update it rather than creating a duplicate.

### Conference Entry Format

Example record:

```yaml
- name: INFOCOM
  description: IEEE International Conference on Computer Communications
  year: 2026
  link: https://infocom2026.ieee-infocom.org/call-papers
  deadline:
    - "2025-07-24 23:59"
    - "2025-07-31 23:59"
  comment: Abstract due a week before the full paper deadline. Page limit is 9 pages for main text, with 10 total pages including references and appendices.
  date: TBD
  place: TBD
  tags: [NETWORKING, CONF]
```

### Field Descriptions

| Field name    | Description                                                                             |
|---------------|-----------------------------------------------------------------------------------------|
| `name`\*      | Short conference name, without year                                                     |
| `year`\*      | Year the conference is happening                                                        |
| `description` | Description, or long name                                                               |
| `comment`     | Additional comments (e.g., page limits, special requirements)                          |
| `link`\*      | URL to the conference call for papers                                                   |
| `deadline`\*  | A list of deadlines in ISO format                                                      |
| `timezone`    | Timezone in [tz format][1]. Default is UTC-12 ([AoE][2])                              |
| `date`        | When the conference is happening                                                        |
| `place`       | Where the conference is happening                                                       |
| `tags`        | One or multiple [tags][3]: conference type and venue tags                              |

Fields marked with asterisk (\*) are required.

### Deadline Format

The *deadline* field should contain a list of deadlines in ISO format:

```yaml
deadline: ["2025-07-31 23:59"]  # Single deadline
```

```yaml
deadline:                       # Multiple deadlines
  - "2025-07-24 23:59"         # Abstract deadline
  - "2025-07-31 23:59"         # Paper deadline
```

All deadlines are automatically displayed in the viewer's local time.

*Note:* If the deadline hour is `{h}:00`, it will be automatically translated into `{h-1}:59:59` to avoid confusion when it happens to be midnight in local time.

### Timezone Codes

The timezone is specified in [tz format][1]. Here are some common codes:

| Common name                   | tz                                                                 |
|-------------------------------|--------------------------------------------------------------------|
| UTC                           | `Etc/UTC`                                                          |
| America Pacific Time          | `America/Los_Angeles`                                              |
| Pacific Standard Time (UTC-8) | `Etc/GMT+8` (Yes, the sign is inverted)                           |
| America Eastern Time          | `America/New_York`                                                 |
| Eastern Standard Time (UTC-5) | `Etc/GMT+5`                                                        |
| American Samoa Time (UTC-11)  | `Pacific/Samoa` or `Etc/GMT+11`                                    |

## Credits

- **Original project**: [sec-deadlines](https://github.com/sec-deadlines/sec-deadlines.github.io) by the security research community
- **Base inspiration**: [ai-deadlines](https://aideadlin.es) by @abshkdz
- **NSSL customization**: Adapted for Networks and Systems Security Lab research areas

## Contact

For questions about specific conferences or suggestions for additions, please:
1. Open an issue on this repository
2. Submit a pull request with your proposed changes
3. Contact the NSSL lab members

---

**Live site**: [https://amirrezaghafoori.github.io/nss-deadlines](https://amirrezaghafoori.github.io/nss-deadlines)

**NSSL Lab**: [https://nss.ece.vt.edu](https://nss.ece.vt.edu)

[1]: https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
[2]: https://www.timeanddate.com/time/zones/aoe
[3]: _data/types.yml