# Carrefour Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Carrefour Scraper](https://oxylabs.io/products/scraper-api/ecommerce/carrefour?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Carrefour website effortlessly. This brief guide showcases how Carrefour Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Carrefour results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Carrefour page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.carrefour.fr/edito/bouton-anti-inflation'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/carrefour-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": " ... </html>",
      "created_at": "2024-02-20 12:48:34",
      "updated_at": "2024-02-20 12:48:51",
      "page": 1,
      "url": "https://www.carrefour.fr/edito/bouton-anti-inflation",
      "job_id": "7165688685470453761",
      "status_code": 613
    }
  ]
}
```
With our Carrefour Scraper, you can seamlessly gather specific data from any Carrefour web page. Assemble the necessary details about product inventory, cost comparison, customer feedback or product specifications to study market trends and outpace your rivals. If you need any clarification, reach out to our support crew using the live chat feature or by sending an email to us at hello@oxylabs.io.