## --- Day 7: Internet Protocol Version 7 ---

While snooping around the local network of EBHQ, you compile a list of [IP addresses](https://en.wikipedia.org/wiki/IP__address) (they're IPv7, of course; [IPv6](https://en.wikipedia.org/wiki/IPv6) is much too limited). You'd like to figure out which IPs support __TLS__ (transport-layer snooping).

An IP supports TLS if it has an Autonomous Bridge Bypass Annotation, or __ABBA__. An ABBA is any four-character sequence which consists of a pair of two different characters followed by the reverse of that pair, such as `xyyx` or `abba`. However, the IP also must not have an ABBA within any hypernet sequences, which are contained by __square brackets__.

For example:

- `abba[mnop]qrst` supports TLS (`abba` outside square brackets).
- `abcd[bddb]xyyx` does __not__ support TLS (`bddb` is within square brackets, even though `xyyx` is outside square brackets).
- `aaaa[qwer]tyui` does __not__ support TLS (`aaaa` is invalid; the interior characters must be different).
- `ioxxoj[asdfgh]zxcvbn` supports TLS (`oxxo` is outside square brackets, even though it's within a larger string).

__How many IPs__ in your puzzle input support TLS?

