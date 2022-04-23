# AS numbers to organization names

This repository contains the asn2org script. It produces a CSV file
translating AS numbers to organization names. It uses [PeeringDB][]
and various IRR databases to do the conversion.

There are various other sources for this information:

- [Potaroo](https://bgp.potaroo.net/cidr/autnums.html)
- [RIPE](http://ftp.ripe.net/ripe/asnames/asn.txt)

The goal of this script is to improve the quality of such information
and avoid names such as `COGENT-174` or `AS-SSI`. The script gives
priority to PeeringDB as it is curated, then uses information from
IRR. When using the IRR database, the organization name is used.

Use `--help` to get help on how to use the script.

[PeeringDB]: https://www.peeringdb.com/
