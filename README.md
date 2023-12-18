# Xing Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Xing Scraper](https://oxylabs.io/products/scraper-api/web/xing?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Xing website effortlessly. This brief guide explains how an Xing Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Xing results by providing your own URLs to our service. We can return the HTML for any Xing page you like.

#### Python code example

The example below illustrates how you can get HTML of Xing page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.xing.com/jobs/search?benefit=1.795d28'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/xing-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html lang=\"de\" class=\"light\">\n  <head>\n    <link rel=\"prefetch\" href=\"/assets/jobs- ... </html>",
      "created_at": "2023-12-18 10:42:32",
      "updated_at": "2023-12-18 10:42:35",
      "page": 1,
      "url": "https://www.xing.com/jobs/search?benefit=1.795d28",
      "job_id": "7142464145147876353",
      "status_code": 200
    }
  ]
}
```
With our Xing Scraper, you can seamlessly extract public data from any Xing profile. Collect necessary professional details, such as job history, skills or endorsements, to understand the job market and gain competitive advantage. If you need assistance or have any questions, our support team is available through live chat or you can email us at hello@oxylabs.io.