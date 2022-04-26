# AS numbers to organization names

This repository contains the asn2org script. It produces a CSV file
translating AS numbers to organization names. It uses [PeeringDB][]
and various IRR databases to do the conversion.

There are various other sources for this information:

- [Potaroo](https://bgp.potaroo.net/cidr/autnums.html)
- [RIPE](http://ftp.ripe.net/ripe/asnames/asn.txt)
- [Maximnd ASN database](https://dev.maxmind.com/geoip/docs/databases/asn?lang=en#csv-database)

The goal of this script is to improve the quality of such information
and avoid names such as `COGENT-174` or `AS-SSI`. The script gives
priority to PeeringDB as it is curated, then uses information from
IRR. When using the IRR database, the organization name is used.

This script uses the following sources (first match is preferred):

- [PeeringDB][]
- AFRINIC, APNIC, ARIN, LACNIC and RIPE IRR databases
- [DB-IP IP to ASN][] database (mostly because ARIN information is not complete)

Use `--help` to get help on how to use the script. You can also
download the [generated CSV file][].

[PeeringDB]: https://www.peeringdb.com/
[DB-IP IP to ASN]: https://db-ip.com/db/download/ip-to-asn-lite
[generated CSV file]: https://vincentbernat.github.io/asn2org/asns.csv
