
# Test Results

Python version used: 3.14.10  
Operating system: Windows 11  
Date: 28 October 2026

| # | Input | Expected result | Actual result | Pass/Fail |
|---|-------|-----------------|---------------|-----------|
| 1 | https://www.example.com/login | No listed warning signs | No listed warning signs | PASS |
| 2 | http://192.0.2.10/account | IP address + HTTP | IP address + HTTP | PASS |
| 3 | http://example.com@sample.invalid/login | @ symbol + HTTP | @ symbol + HTTP | PASS |
| 4 | https://a.b.c.d.e.example.invalid/path | Many hostname segments | Many hostname segments | PASS |
| 5 | https://xn--example.invalid/ | Punycode-style hostname | Punycode-style hostname | PASS |

## Notes

I learned how Python can identify common phishing URL warning signs without opening a website.

I was surprised that the @ symbol can make a URL misleading, because the actual hostname may be different from the domain appearing before it.

I also learned that having no warning signs does not guarantee a URL is safe.
