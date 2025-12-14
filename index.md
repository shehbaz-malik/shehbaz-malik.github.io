---
layout: default
---

## Overview

Versatile Full-Stack developer with expertise in PHP frameworks, WordPress (custom themes & plugins), React.js, Vue.js, and RESTful/GraphQL API integration. Proven experience in building scalable B2B and eCommerce solutions for a variety of businesses. Focused on clean code, performance, and seamless user experiences.

&nbsp;

## Work Experience

> ### 1. Upwork
> Full-Stack Developer | Nov 2025 - Present
>
> `Freelancer` - Full-time
> * * *
> ### 2. NewRich Network (Canada)
> Full-Stack Developer | Mar 2022 - Aug 2025
>
> `Remote` - Full-time
> ##### Responsibilities
> * Maintained multiple projects, including CRM systems, Payment Gateway APIs,
WordPress sites (including e-commerce and membership platforms).
> * Managed various sales funnels and upsells to enhance business revenue.
>
> ##### Stacks
> * PHP, Laravel, WordPress (custom themes, plugins), VueJS, ReactJS, API’s
including Chatgpt, Stripe, NMI, Konnektive CRM, Drip, ActiveCampaign, Zapier
Automations, and Custom Checkout.
>
> * * *
> ### 3. Wabel B2B (France)
> Full-Stack Developer | Nov 2020 - May 2021
>
> `Remote` - Full-time
> ##### Responsibilities
> * Responsible for maintaining the B2B platform, which supports nearly 100,000
monthly active users.
> * Implemented a meeting scheduling feature using the Zoom API and WebSockets
for real-time communication between customers and businesses.
> * Integrated OAuth synchronization with Google and Outlook Calendar APIs.
>
> ##### Stacks
> * PHP, Mouf, GraphQL, RabbitMQ, Docker, AngularJS, Unit Tests, API’s.
>
> * * *
> ### 4. Phoenix Technologies (Pakistan)
> Full-Stack Developer | Nov 2017 - Oct 2020
>
> `Onsite` - Full-time
> ##### Responsibilities
> * Maintaining multiple projects, including an organization's ERP, CRM, Payment
Gateway APIs, and WordPress sites.
>
> ##### Stacks
> * PHP, Laravel, WordPress
>

&nbsp;

## Projects

- needl.co
  - PREVIEW: <a href="https://app.needl.co" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: PHP, Mouf, GraphQL, RabbitMQ, Docker, AngularJS, Unit Tests and API’s.
  - ***
- newrich.com
  - PREVIEW: <a href="https://newrich.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: PHP, Laravel, ReactJS, API’s.
  - ***
- newrichapps.com
  - PREVIEW: <a href="https://newrichapps.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins, Custom Checkout with upsells flow and User Dashboard.
  - ***
- zebricks.com
  - PREVIEW: <a href="https://www.zebricks.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: HubSpot, Custom Modules & Theme.
  - ***
- childrensbookmaker.net
  - PREVIEW: <a href="https://app.childrensbookmaker.net" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: Laravel, OpenAI, AI Story Generation, Illustration generation using OpenAI and User Dashboard.
  - ***
- apba.org.pk
  - PREVIEW: <a href="https://apba.org.pk" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: Laravel, Organization CRM, Business Management, Custom Invoicing and Messer Management.
  - ***
- gemmo.ai
  - PREVIEW: <a href="https://gemmo.ai" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***
- risso.ai
  - PREVIEW: <a href="https://risso.ai" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***
- vintagerep.com
  - PREVIEW: <a href="https://vintagerep.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***
- mrjunkbgoneseattle.com
  - PREVIEW: <a href="https://mrjunkbgoneseattle.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins and GHL Crm Integration.
  - ***
- hexafit.nl
  - PREVIEW: <a href="https://hexafit.nl" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***
- interrexglobal.com
  - PREVIEW: <a href="https://interrexglobal.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***
- cleads.ai
  - PREVIEW: <a href="https://cleads.ai" target="_blank" rel="noopener noreferrer" data-proofer-ignore>Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***
- 99junkremoval.com
  - PREVIEW: <a href="https://99junkremoval.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***
- thomas-dentistry.com
  - PREVIEW: <a href="https://thomas-dentistry.com" target="_blank" rel="noopener noreferrer">Live site</a>
  - STACKS: WordPress, Custom Theme & Plugins.
  - ***

<!-- &nbsp;

## Web Scrapping With PlayWright
Example for clean code

```js
// Bot function to scrap the actual page content
async function scrapeCompanies(page, url) {
  let allCompanies = [];
  let pageNum = 1;

  console.log(`🔗 Navigating to: ${url}`);
  await page.goto(url, {waitUntil: "domcontentloaded", timeout: 0});
  
  try {
    while (true) {
      console.log(`📄 Scraping page ${pageNum}...`);
      
      const companiesOnPage = await scraper(page);
      console.log(`✅ Found ${companiesOnPage.length} companies on page ${pageNum}`);
      allCompanies.push(...companiesOnPage);
      
      await humanLikeMouse(page);

      // --- Pagination check ---
      const prevUrl = page.url();

      const nextBtn = await page.$("#pagination-next");
      if (!nextBtn) {
        console.log("🚦 No more pages. Stopping...");
        break;
      }

      await humanLikeScroll(page);

      console.log("➡️ waiting before click...");
      await delay(2000, 4000);
      console.log("➡️ Clicking next button...");

      await page.click("#pagination-next", {timeout: 0});

      await page.waitForURL(newUrl => newUrl !== prevUrl, {
        waitUntil: "domcontentloaded",
        timeout: 0
      });

      await maybeHumanTypeQuoiQui(page);

      pageNum++;
    }

    return allCompanies;
  } catch (err) {
    console.error("❌ Error scraping companies:", err.message);
    return allCompanies;
  }
}
``` -->
&nbsp;

## Scrapping Bots

![Scrape Result](./assets/images/bot_scrapper.png)

* * *
