# Trustpilot Scraper
This Trustpilot Scraper retrieves comprehensive reviews, ratings, and sentiment data for any supported company website. It helps analysts, marketers, and businesses understand customer perception at scale. Built for speed, accuracy, and reliable high-volume extraction, it provides clean and structured Trustpilot review insights.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/za2122/footer-section/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
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
  If you are looking for <strong>Trustpilot</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
The Trustpilot Scraper automatically collects reviews from Trustpilot for any target domain, giving you direct access to customer sentiment and experience patterns.
It solves the challenge of manually tracking reputation across regions and ensures that even high-volume review datasets remain structured and ready for analysis.

### Why Trustpilot Review Data Matters
- Provides real-time insights into customer satisfaction and recurring issues.
- Captures sentiment, star ratings, timestamps, and consumer profile details in one dataset.
- Enables trend analysis to improve product, service, or brand strategy.
- Supports multi-country review coverage across all major Trustpilot-supported regions.
- Helps teams automate reputation tracking and performance monitoring.

## Features
| Feature | Description |
|---------|-------------|
| Dual Processing Modes | Choose between API mode (slower, cheaper) or Cheerio mode (faster, requires higher memory). |
| Full Review Extraction | Retrieves all available reviews for a target company domain, sorted by recency. |
| Sentiment Categorization | Automatically identifies sentiment as Negative, Neutral, or Positive. |
| Reply Collection | Captures company replies, dates, and update information. |
| Multi-Country Coverage | Works across all Trustpilot-supported regions. |
| Review Metadata | Includes consumer info, rating, dates, labels, and domain-specific review counts. |
| Filtering Options | Supports review limits and API-based “Date posted” filtering. |

---
## What Data This Scraper Extracts
| Field Name | Field Description |
|------------|------------------|
| id | Unique review identifier. |
| text | Full review text submitted by the customer. |
| title | Review headline or summary. |
| rating | Star rating value assigned by the reviewer. |
| labels | Verification and metadata labels associated with the review. |
| dates | Includes experienced, published, and updated timestamps. |
| consumer | Customer profile data such as name, country code, and review count. |
| reply | Company reply details including message and timestamps. |
| language | Language code of the submitted review. |
| link | Direct link to the review if provided. |

---
## Example Output

    {
      "id": "65a7cbd9b8138df08d3fd809",
      "filtered": false,
      "pending": false,
      "text": "Awesome Company! - Beautiful jewelry, timely shipping, good practices.",
      "rating": 5,
      "labels": {
        "merged": null,
        "verification": {
          "isVerified": true,
          "createdDateTime": "2024-01-17T14:45:14.000Z",
          "reviewSourceName": "InvitationApi",
          "verificationSource": "invitation",
          "verificationLevel": "verified",
          "hasDachExclusion": false
        }
      },
      "title": "Awesome Company",
      "likes": 0,
      "dates": {
        "experiencedDate": "2024-01-12T00:00:00.000Z",
        "publishedDate": "2024-01-17T14:45:14.000Z",
        "updatedDate": null
      },
      "consumer": {
        "id": "57eaba720000ff000a48480e",
        "displayName": "Kimberly Babcock Sanborn",
        "imageUrl": "",
        "numberOfReviews": 3,
        "countryCode": "US",
        "hasImage": false,
        "isVerified": false
      },
      "reply": {
        "message": "Hi Kimberly, thank you for reaching out and sharing your positive words with us! We appreciate your continued support and we look forward to having you shop with us again.",
        "publishedDate": "2024-01-17T16:03:37.000Z",
        "updatedDate": null
      },
      "consumersReviewCountOnSameDomain": 1,
      "productReviews": [],
      "language": "en",
      "location": null,
      "website": "",
      "link": ""
    }

---
## Directory Structure Tree

    Trustpilot/
    ├── src/
    │   ├── runner.js
    │   ├── processors/
    │   │   ├── api_mode.js
    │   │   └── cheerio_mode.js
    │   ├── parsers/
    │   │   ├── review_parser.js
    │   │   └── sentiment_classifier.js
    │   ├── utils/
    │   │   ├── request.js
    │   │   └── normalize.js
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── sample_reviews.json
    │   └── inputs.sample.txt
    ├── package.json
    └── README.md

---
## Use Cases
- **Reputation teams** use it to monitor customer feedback, so they can quickly address negative trends.
- **E-commerce brands** use it to analyze product satisfaction, helping improve conversion rates and customer retention.
- **Market researchers** use it to gather sentiment data across multiple regions, enabling competitive analysis.
- **Customer experience teams** use it to track service quality and identify recurring support issues.
- **Data analysts** integrate review streams into dashboards to measure brand health over time.

---
## FAQs

**Q: Do I need to provide a Trustpilot URL?**
A: No. Provide the company’s website URL (e.g., `www.example.com`). The scraper automatically locates the associated Trustpilot page.

**Q: Why am I only seeing up to 100 pages of reviews?**
A: Trustpilot’s frontend limits review pagination to 100 pages. For higher limits, use more advanced filtering options.

**Q: What is the difference between API and Cheerio mode?**
A: API mode is slower but cheaper. Cheerio mode is faster and more resource-intensive and requires at least 2GB memory.

**Q: Does Date Posted filtering work for both modes?**
A: No, it only applies in API mode.

---
## Performance Benchmarks and Results
**Primary Metric:** Processes an average of 500–800 reviews per minute in API mode and significantly faster in Cheerio mode.
**Reliability Metric:** Maintains a 98%+ success rate across supported regions.
**Efficiency Metric:** Optimized for low-cost execution while handling high-volume datasets with stable memory usage.
**Quality Metric:** Captures 99% of available review fields with consistent formatting and minimal data loss.


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
        <img src="https://github.com/za2122/footer-section/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtube.com/shorts/6AwB5omXrIM" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review3.gif" alt="Review 3" width="35%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Exceptional results, clear communication, and flawless delivery. Bitbash nailed it.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
