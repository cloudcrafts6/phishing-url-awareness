# Test Results

Python version used: 3.\_14\_   |   Operating system: \_\_Windows\_\_\_\_\_\_   |   Date: \_\_\_28-10-2026\_\_\_\_\_

|#|Input|Expected result|Actual result|Pass/Fail|
|-|-|-|-|-|
|1|https://www.example.com/login|No listed warning signs|No listed warning signs found. This does NOT prove safety.|PASS|
|2|http://192.0.2.10/account|IP address + HTTP|Uses an IP address instead of a familiar domain. Uses HTTP.|PASS|
|3|http://example.com@sample.invalid/login|@ symbol + HTTP|Contains an @ symbol; inspect carefully. Uses HTTP.|PASS|
|4|https://a.b.c.d.e.example.invalid/path|Many hostname segments|Contains many hostname segments/subdomains.|PASS|
|5|https://xn--example.invalid/|Punycode-style hostname|Contains a punycode-style hostname.|PASS|

## Notes

I learned that a URL can be split into scheme, hostname and path, and that the hostname is the most important part to read.
It surprised me that a link with no warning signs can still be dangerous, so this tool only gives clues, not proof.

