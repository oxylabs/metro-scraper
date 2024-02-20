# Metro Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Metro Scraper](https://oxylabs.io/products/scraper-api/ecommerce/metro?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Metro website effortlessly. This brief guide showcases how Metro Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Metro results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Metro page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://fresh2go.metro.ca/individual-trays/deli-trays-platters.html'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/metro-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Strict//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-str ... </html>",
      "created_at": "2024-02-20 12:55:49",
      "updated_at": "2024-02-20 12:55:50",
      "page": 1,
      "url": "https://fresh2go.metro.ca/individual-trays/deli-trays-platters.html",
      "job_id": "7165690508843454465",
      "status_code": 200
    }
  ]
}
```
With our Metro Scraper, you can seamlessly harvest public data from any Metro web page. Garner essential timetable information, station details, or transit updates, to plan seamless journeys and stay ahead of transportation changes. If you need any help, reach out to our support team via live chat or send us an email at hello@oxylabs.io.