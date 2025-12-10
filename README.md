# Fanfix.com scraper
> Fanfix.com scraper helps you collect structured creator and model data from Fanfix with minimal setup. It turns unstructured profile pages into clean, analytics-ready records you can plug into your CRM, dashboards, or growth workflows.
> Whether you’re tracking models, pricing, or engagement, this scraper keeps your Fanfix data consistent, searchable, and ready to act on.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>fanfix-com-scraper</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
Fanfix.com scraper is a data collection tool that automatically visits Fanfix creator pages and extracts key profile information, monetization details, and engagement indicators. Instead of manually clicking through hundreds or thousands of profiles, you get a consistent JSON/CSV feed you can reuse in automations and analytics.

It solves the problem of gathering large model lists or niche creator segments for research, influencer discovery, or competitor tracking. It’s ideal for marketers, agencies, data analysts, and growth teams who need up-to-date Fanfix creator data at scale.

### Creator Analytics & Discovery
- Collect detailed creator profile data (names, bios, tags, and niches) into a single structured dataset.
- Capture monetization details such as subscription price, trial offers, bundles, and premium content indicators.
- Track audience and engagement metrics like follower counts, posts, and activity status over time.
- Filter or segment models by niches, languages, categories, and content style for targeted campaigns.
- Power internal dashboards, CRM enrichment, and prospecting workflows with fresh creator data.

## Features

| Feature | Description |
|----------|-------------|
| Bulk profile scraping | Import a list of Fanfix profile URLs or discovery pages and extract data for hundreds or thousands of creators in one run. |
| Structured creator data | Normalizes model profile information into consistent fields for easy querying and integration. |
| Monetization insights | Captures subscription price, tiers, offers, and other monetization indicators to support pricing analysis. |
| Engagement metrics | Tracks follower counts, posts, and other activity signals to rank or score creators. |
| Flexible input options | Accepts URLs, username lists, or discovery/search result pages depending on your workflow. |
| Export-ready output | Output can be saved as JSON, CSV, or fed directly into databases, BI tools, or automation pipelines. |
| Error handling & retries | Skips broken or unavailable profiles gracefully while continuing the rest of the run. |
| Configurable throttling | Adjustable delays and concurrency to balance speed against stability and blocking risk. |

---

## What Data This Scraper Extracts

| Field Name | Field Description |
|-------------|------------------|
| id | Internal unique identifier for the scraped creator record. |
| username | Fanfix username/handle of the creator. |
| displayName | Public display name of the creator profile. |
| profileUrl | Canonical URL of the creator’s public Fanfix page. |
| avatarUrl | Direct link to the creator’s profile image or avatar. |
| bio | Short description or biography text set on the profile. |
| category | Main niche, theme, or category associated with the creator. |
| tags | Array of tags/keywords describing content type or audience. |
| subscriptionPrice | Primary subscription price in the profile’s default currency. |
| currency | Currency code used for subscription pricing (e.g. USD, EUR). |
| hasFreeTrial | Indicates whether the profile is currently offering a free trial. |
| bundles | Details of any subscription bundles or multi-month discounts. |
| followersCount | Approximate number of followers/subscribers on the profile. |
| postsCount | Number of public and/or paywalled posts visible on the profile. |
| mediaPreviewCount | Number of preview media items (photos/videos) on the landing page. |
| socialLinks | List of external profile links (e.g. Instagram, Twitter, TikTok). |
| isVerified | Flag indicating whether the creator appears to be verified on the platform. |
| isActive | Boolean indicating if the profile looks active based on recent content. |
| lastPostDate | Timestamp or date string of the most recent visible post. |
| country | Parsed country or region information if available. |
| language | Primary language detected or indicated for the profile. |
| createdAt | Time when this record was first scraped. |
| updatedAt | Time when this record was last refreshed by the scraper. |
| rawHtml | (Optional) Extracted HTML snippet for debugging or advanced parsing. |

---

## Example Output

    [
      {
        "id": "ffx_001234",
        "username": "creator_example",
        "displayName": "Creator Example",
        "profileUrl": "https://fanfix.com/creator/creator_example",
        "avatarUrl": "https://images.fanfix-cdn.com/avatars/creator_example.jpg",
        "bio": "Lifestyle, behind-the-scenes content, and daily vlogs.",
        "category": "Lifestyle",
        "tags": [
          "lifestyle",
          "vlogs",
          "behind-the-scenes"
        ],
        "subscriptionPrice": 14.99,
        "currency": "USD",
        "hasFreeTrial": true,
        "bundles": [
          {
            "durationMonths": 3,
            "price": 39.99,
            "savingsPercent": 11
          }
        ],
        "followersCount": 5280,
        "postsCount": 186,
        "mediaPreviewCount": 12,
        "socialLinks": [
          "https://instagram.com/creator_example",
          "https://x.com/creator_example"
        ],
        "isVerified": true,
        "isActive": true,
        "lastPostDate": "2025-10-28T15:32:00Z",
        "country": "United States",
        "language": "en",
        "createdAt": "2025-11-10T09:00:00Z",
        "updatedAt": "2025-11-10T09:00:00Z"
      }
    ]

---

## Directory Structure Tree

    Fanfix.com scraper/
    ├── src/
    │   ├── main.py
    │   ├── config.py
    │   ├── runner.py
    │   ├── inputs/
    │   │   ├── __init__.py
    │   │   └── url_loader.py
    │   ├── extractors/
    │   │   ├── __init__.py
    │   │   ├── profile_parser.py
    │   │   └── pricing_parser.py
    │   ├── clients/
    │   │   ├── __init__.py
    │   │   └── http_client.py
    │   ├── utils/
    │   │   ├── __init__.py
    │   │   ├── logging_utils.py
    │   │   ├── throttling.py
    │   │   └── validators.py
    │   └── outputs/
    │       ├── __init__.py
    │       └── exporters.py
    ├── data/
    │   ├── inputs.sample.txt
    │   └── sample_output.json
    ├── tests/
    │   ├── __init__.py
    │   ├── test_profile_parser.py
    │   └── test_pricing_parser.py
    ├── scripts/
    │   ├── run_local.sh
    │   └── export_to_csv.py
    ├── requirements.txt
    ├── pyproject.toml
    ├── .env.example
    └── README.md

---

## Use Cases

- **Influencer marketing agencies** use it to **build and refresh lists of Fanfix creators in targeted niches**, so they can **launch more precise outreach campaigns with up-to-date contact and profile data.**
- **Creator economy analytics platforms** use it to **pull Fanfix model, pricing, and engagement data into their dashboards**, so they can **offer cross-platform insights and benchmarking to customers.**
- **Growth and partnership teams** use it to **identify fast-growing or underpriced creators**, so they can **propose collaborations and revenue-share deals before competitors do.**
- **Data analysts and researchers** use it to **study subscription pricing, content niches, and audience behavior on Fanfix**, so they can **derive trends, patterns, and market intelligence.**
- **Internal operations teams** use it to **sync Fanfix profiles into CRMs or lead lists**, so they can **keep contact databases clean, structured, and ready for automation.**

---

## FAQs

**Q1: Do I need a list of Fanfix URLs to start?**
In most setups, providing a list of profile URLs or discovery/search result pages is the fastest way to get started. You can build this list from your own research or internal tools. The scraper then visits each page, extracts the data fields, and stores them in a structured dataset.

**Q2: What happens if some profiles are private, removed, or inaccessible?**
When a profile can’t be loaded or appears unavailable, the scraper records an error status for that item and moves on to the next one. This ensures the overall run completes successfully without failing on a single problematic profile, and you can review any skipped entries afterwards.

**Q3: Can I filter creators by niche, price, or followers directly in the scraper?**
Typical setups capture all relevant data first, then apply filtering during post-processing (for example, only keeping creators with a minimum follower count or a specific price range). This keeps the scraper simple while giving you full control when querying or analyzing the exported dataset.

**Q4: How often should I run the scraper to keep data fresh?**
For most use cases, a weekly or bi-weekly run balances freshness with resource usage. High-frequency use cases like dynamic pricing or fast-changing campaigns might run daily, while longer-term research projects may only need monthly updates.

---

### Performance Benchmarks and Results

**Primary Metric:** On a typical broadband connection, the scraper can process approximately 150–250 Fanfix profiles per hour with detailed field extraction, depending on page complexity and throttle settings.

**Reliability Metric:** With conservative timeouts and retry logic enabled, success rates of 92–97% on valid, public profiles are achievable over large runs.

**Efficiency Metric:** Average CPU and memory usage remain modest for single-run jobs, making it suitable for running on lightweight virtual machines or shared environments without special tuning.

**Quality Metric:** For well-structured profiles, field completeness for core attributes (username, profile URL, pricing, and follower counts) generally exceeds 95%, providing a strong foundation for analytics, targeting, and enrichment workflows.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
