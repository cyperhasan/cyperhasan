Appendix A: Developer URL canonicalization test
cases
These example inputs and expected outputs illustrate the desired developer URL to canonicalized domain transformation.
Test handling of a typical .com domain
https://www.example.com/test example.com
https://m.example.com/test example.com
https://example.com/test example.com
https://subdomain.example.com/test subdomain.example.com
https://another.subdomain.example.com/test subdomain.example.com
https://subdomain.www.example.com/test example.com
Test handing of two-level public suffix
https://www.example.co.uk/test example.co.uk
https://m.example.co.uk/test example.co.uk
https://example.co.uk/test example.co.uk
https://subdomain.example.co.uk/test subdomain.example.co.uk
https://another.subdomain.example.co.uk/test subdomain.example.co.uk
IAB Tech Lab
https://iabtechlab.com/ads-txt

https://subdomain.www.example.co.uk/test example.co.uk
Test handling of a newer country public suffix registerable namespace
https://www.example.uk/test example.uk
https://m.example.uk/test example.uk
https://example.uk/test example.uk
https://subdomain.example.uk/test subdomain.example.uk
https://another.subdomain.example.uk/test subdomain.example.uk
https://subdomain.www.example.uk/test example.uk
Appendix B: Developer URL to app-ads.txt file URL
test cases
These example inputs and expected outputs illustrate the proper translation from developer URL to app-ads.txt path.
Test baseline developer URL
This test illustrates baseline URL normalization without any subdomain.
● Developer URL: https://example.com/test
● Verifier will crawl: https://example.com/app-ads.txt
Test developer URL with ignored www. subdomain
This test illustrates the normalization of the common “www” subdomain.
● Developer URL: https://www.example.com/test
IAB Tech Lab
https://iabtechlab.com/ads-txt

● Verifier will crawl: https://example.com/app-ads.txt
● Confirm that crawler DOES NOT crawl: https://www.example.com/app-ads.txt
Test “m.” developer URL with ignored m. subdomain
This test illustrates the normalization of the common “m” subdomain.
● Developer URL: https://m.example.com/test
● Verifier will crawl: https://example.com/app-ads.txt
● Confirm that crawler DOES NOT crawl: https://m.example.com/app-ads.txt
Test developer URL with subdomain
This test illustrates how the subdomain will be used for locating an app-ads.txt file.
● Developer URL: https://subdomain.example.com/test
● Verifier will first crawl: https://subdomain.example.com/app-ads.txt
● If no file found, verifier will then crawl: https://example.com/app-ads.txt
Test developer URL with multiple subdomains
This test illustrates how only the first subdomain will be used for locating an app-ads.txt file.
● Developer URL: https://another.subdomain.example.com/test
● Verifier will first crawl: https://subdomain.example.com/app-ads.txt
● If no file found, verifier will then crawl: https://example.com/app-ads.txt
Test developer URL with subdomain on a multipart public suffix
This test illustrates how only the first subdomain will be used for locating an app-ads.txt file for a URL with a multipart public suffix.
● Developer URL: https://another.subdomain.example.co.uk/test
● Verifier will first crawl: https://subdomain.example.co.uk/app-ads.txt
● If no file found, verifier will then crawl: https://example.co.uk/app-ads.txt
