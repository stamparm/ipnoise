# IPnoise

Daily archive of the [IPnoise](https://ipnoise.sekuripy.hr/) blacklist.

IPnoise is a free IP blacklist built from a distributed network of interactive
honeypot sensors — hosts running no legitimate service, advertised nowhere, so
every connection reaching them is hostile by construction. The sensors answer,
emulating real services well enough to record what each source actually came to
do: credential attacks, exploit and malware-delivery attempts, CMS and
admin-panel enumeration, SSH brute force. An address is listed after repeated
hostile activity within a short sliding window. Captured payloads are never
published.

## Files

`daily/YYYY-MM-DD.txt` — the addresses active on that day (UTC), captured just
after the day ends. Plain text, one IPv4 or IPv6 address per line, `#` comments
in the header.

```
curl -fsSL https://raw.githubusercontent.com/stamparm/ipnoise/master/daily/2026-09-07.txt | grep -v '^#'
```

## Live feed

This repository is an archive. For current data use the feed itself, which also
offers wider freshness windows:

| File | Contents |
|------|----------|
| [1d.txt](https://ipnoise.sekuripy.hr/1d.txt) | active in the last day (what is archived here) |
| [7d.txt](https://ipnoise.sekuripy.hr/7d.txt) | active in the last 7 days |
| [14d.txt](https://ipnoise.sekuripy.hr/14d.txt) | active in the last 14 days |
| [30d.txt](https://ipnoise.sekuripy.hr/30d.txt) | active in the last 30 days |

A shorter window means less chance of blocking an address that has since been
reassigned; a longer one casts a wider net.

## License

Free for any use.
