# Frontend Performance

_by Osama Kashif_

This document covers standards and guides around frontend performance. Definitions, summaries, measurements, and other relevant sections will be marked as provided.

## Frontend Performance Standards

### Overview/summary of indicators and their ideal values

| Indicator                       | Ideal value    |
| ------------------------------- | -------------- |
| Time to First Byte (TTFB)       | <= 0.8 seconds |
| Largest Contentful Paint (LCP)  | <= 2.5 seconds |
| Cumulative Layout Shift (CLS)   | <= 0.1         |
| Interaction to Next Paint (INP) | <= 0.2 seconds |
| Total Blocking Time (TBT)       | <= 0.2 seconds |

### Indicator definitions

- "Time to First Byte (TTFB) is an indicator of server efficiency." It is the time taken to receive the first byte of data from the server.
- "Largest Contentful Paint (LCP) is a stable Core Web Vital metric for measuring perceived load speed. It marks the point in the page load timeline when the page's main content has likely loaded. A fast LCP helps reassure the user that the page is useful." Essentially, it is a measure for when the main part of the page is loaded making it useful.
- Cumulative Layout Shift (CLS) "measures all the layout's small and large 'jumps' during the page load phase. You want to keep this score as close to 0 as possible, as a score of 0 indicates that the layout did not change at all. CLS measures the instability of content." This is when there are any sudden shifts within your UI, e.g. an instant pop up where there was a button that you just clicked, or the button shifts down due to a dialogue appearing.
- Interaction to Next Paint (INP) "measures the time it takes for the browser to render the next frame after user interaction, such as a click, scroll, or typing." This is a measure of how quickly something changes in the UI once the user interacts with an interact-able aspect/element.
- Total Blocking Time (TBT) "measures the time a user is blocked from doing interactions at the critical page load time and is a metric that you want to get close to as 0 as possible." "A score of 0 indicates that the user is not blocked, whereas a score of, let’s say, 1000 indicates that the user was blocked for an accumulated time of 1 second."

### Ideal values for indicators

- "Ideally, the TTFB should be under 200 milliseconds for a server in close proximity to the user." "As a rough guide, most sites should strive to have TTFB of 0.8 seconds or less."
- "To provide a good user experience, sites should strive to have LCP of 2.5 seconds or less."
- "To provide a good user experience, a site must have a CLS score of 0.1 or less."
- "Google suggests sites should strive to have an INP of 200 milliseconds or less."
- "To provide a good user experience, sites should have a TBT of less than 200 milliseconds when tested on average mobile hardware."

## Frontend Performance Improving Guidelines

- Minify CSS and JavaScript.
- Reduce image sizes to be relevant to screen sizes (as opposed to unnecessarily large/in depth ones).
- Minimise the number of HTTP requests to avoid latency.
- Remove duplicate JavaScript and CSS.
  - The Coverage panel in Chrome DevTools can help you find unused JavaScript and CSS code.
- For large datasets on the server side, can consider gzip compression.
- Limit the number of fonts. A lot of fonts can slow down page load significantly.
- Use Lighthouse on Chrome to measure performance.

## Tools for checking performance

Chrome devtools are good to use. A number of tools in general include:

- Chrome devtools: [Lighthouse](https://developer.chrome.com/docs/lighthouse) tab
- Chrome devtools: [Network](https://developer.chrome.com/docs/devtools/network) tab
- Web Vitals JavaScript Library (added by default in React apps)
- [Web page test](https://www.webpagetest.org/)

## References

1. [23 front-end performance engineering rules for web apps](https://techbeacon.com/app-dev-testing/23-front-end-performance-rules-web-applications)
2. [Frontend Performance Checklist](https://crystallize.com/learn/best-practices/frontend-performance/checklist)
3. [Frontend Performance Measuring, KPIs, and Monitoring](https://crystallize.com/blog/frontend-performance-measuring-and-kpis)
4. [Time to First Byte (TTFB)](https://crystallize.com/learn/best-practices/frontend-performance/other-web-vitals/time-to-first-byte-ttfb)
5. [Time to First Byte (TTFB)](https://web.dev/articles/ttfb#what-is-a-good-ttfb-score)
6. [Largest Contentful Paint (LCP)](https://web.dev/articles/lcp)
7. [Cumulative Layout Shift (CLS)](https://web.dev/articles/cls)
8. [Interaction to Next Paint (INP)](https://crystallize.com/learn/best-practices/frontend-performance/core-web-vitals/interaction-to-next-paint-inp)
9. [Total Blocking Time (TBT)](https://web.dev/articles/tbt)
