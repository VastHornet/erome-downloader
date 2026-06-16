[Erome Downloader](https://apify.com/vnx0/erome-downloader?fpr=data)

# Erome Downloader & Scraper

A fast, highly efficient **Erome downloader and scraper** designed to extract and bulk-download videos, images, and albums from erome.com. Perfect for media archivers, data extraction, and automation workflows. This powerful software simplifies the entire process of downloading content from Erome, whether it's a single album, a batch of albums, a specific user profile, or search results.

Features include raw media extraction, bulk gallery downloading, bypasses for HTTP 403 blocks (using built-in residential proxies and authentic headers), and fully structured metadata exports.

## Features

- **⚡️ Bulk Album Downloader:** Download images and high-quality videos directly from Erome albums.
- **👤 Profile Scraper:** Extract and download all albums and posts natively found on any creator's profile page.
- **🔍 Search Automation:** Scrape Erome search results and seamlessly extract their subsequent albums automatically.
- **🚀 Fast & Reliable:** Built with advanced networking to prevent 403 Forbidden blockers, timeouts, and IP blocks seamlessly.
- **🛡️ Proxy Support:** Fully integrates with high-quality proxies to maintain high scraping success rates securely.
- **📊 Structured Data Extraction:** Retrieves album tags, titles, dates, uploaders, and individual media URLs in a structured format for easy database storage or further API usage.

## Why use this Erome Downloader?

This tool acts as a premier **gallery-downloader and data-extraction tool**. Standard Python scrapers or standalone scripts can drop connections, get banned by 410 headers, or struggle with concurrency. Our software utilizes a robust infrastructure for flawless, concurrent data extraction, automatically dealing with headers, retries, and proxies.

You can dynamically toggle the media download capability if you only want the metadata, or you can seamlessly archive the raw `.mp4` and `.jpg` files directly to your storage seamlessly.

## Input Configuration

The scraper accepts input via a sleek interface or a generic data payload.

| Field | Type | Description |
| --- | --- | --- |
| `url` | String | A single Erome album URL to scrape and download. |
| `urls` | Array | A list of Erome album URLs for bulk downloading. |
| `username` | String | A specific Erome profile username to extract all posts/albums from. |
| `query` | String | A search keyword to scrape Erome albums. |
| `download_media` | Boolean | True to physically download all `mp4`/`jpg` files to storage, False to only export the metadata. Default: `false`. |
| `proxyConfiguration` | Object | Proxy settings to prevent IP bans and secure the traffic flow. |

### Input Example

```
{
  "url": "https://www.erome.com/a/U3CyGACn",
  "download_media": true
}
```

## Output Example

Upon completion, you will find your structured data export containing all necessary metadata. If `download_media` was checked, the actual media files will be saved in structured storage.

```
{
  "input": {
    "url": "https://www.erome.com/a/U3CyGACn",
    "download_media": true
  },
  "success": true,
  "data": {
    "type": "album",
    "album_id": "U3CyGACn",
    "title": "Asian wild babe sloppy blowjob",
    "user": "PINKPARK",
    "tags": ["amateur", "creampie", "asian"],
    "count": 6,
    "date": "2026-04-06T13:53:18.000Z",
    "media": [
      {
        "num": 1,
        "url": "https://s94.erome.com/.../file.jpg",
        "filename": "nqKmbvAz",
        "extension": "jpg"
      },
      {
        "num": 2,
        "url": "https://v94.erome.com/.../file.mp4",
        "filename": "Z64ancVH_720p",
        "extension": "mp4"
      }
    ],
    "download_stats": {
      "totalMedia": 6,
      "downloadedMedia": 6
    }
  }
}
```

## Usage Limits & Disclaimer

Please respect Erome.com's Terms of Service and bandwidth capabilities. We strongly advise utilizing reliable residential proxies inside your configuration to decrease the likelihood of getting banned and to ensure a healthy and stable automated flow for all your web-scraping endeavors.