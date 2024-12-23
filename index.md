PhotonIQ Performance Proxy (P3): improving Core Web Vitals for over 25% boost in conversion rates

Speed performance for web pages is no longer a luxury; it’s a necessity, as research shows that even a one-second delay can significantly drop user satisfaction and conversion rates. According to Google, bounce rates (the probability of a user leaving a website) skyrocket as load times increase: a 1-3 second delay raises abandonment by 32%, a 1-5 second delay spikes it by 90%, and anything beyond 10 seconds? That sends bounce rates up by 123%.

But what exactly causes these delays? Numerous factors can contribute to delayed page load latency. From server issues and network congestion to large file sizes and inefficient code, each element plays a role in how quickly a webpage renders. Understanding these challenges is crucial for anyone looking to enhance their web performance. Even as web technologies evolve to tackle these challenges, some users still experience frustrating page loading delays.

Today, we’re introducing a game-changer in the race for speed: PhotonIQ Performance Proxy (P3).  P3 is a suite of AI-driven services designed to find the best ways to optimize your website and reduce page load latency without compromising the user experience. It analyzes your webpage and applies real-time optimizations that improve core web vitals, delivering a fully optimized version that loads almost instantly on the browser.
In this blog, we’ll highlight P3's major features and explore how it can transform your website’s performance. Many of our customers have experienced up to a 25% boost in conversion rates due to the Core Web Vitals improvements powered by the P3 engine.
The browser page loading journey
Before exploring deeper into P3, let’s take a step back to understand the browser process for loading your website. Whenever a user visits your website, 
The browser requests the site’s server to fetch the core HTML document. 
The CDN routes the request to the nearest geographical server, analyzing real-time network conditions, geographic proximity, and server load to deliver the HTML document with minimal latency and optimized performance.
The server responds with this document, and the browser quickly begins reading it. It encounters links to essential assets—stylesheets, JavaScript files, images, and fonts—that bring the page to life. For each external resource, the browser makes additional requests to pull them individually. 

Caching plays a vital role in this process. When a user visits your site, the browser stores certain elements and assets in a temporary cache. Assets stored in the browser's cache can be loaded instantly to reduce load time. 

With all these assets in place, the browser begins to build the Document Object Model (DOM), a structured layout of the page’s content that ultimately appears on the screen. 

But this process isn’t just a one-time deal; it repeats with each new page the user navigates to, meaning every click triggers a fresh set of requests and responses to pull in any uncached content.

While this cycle may be efficient, some users still experience delays, especially on sites with multiple pages or complex content. Each time users move from one page to another, like browsing a product catalog or news section, they wait for each page to load. Imagine if these pages were already optimized in the browser background. This means the content is ready to be served when users click, giving them a smooth, uninterrupted experience.
Beyond the regular: Why is P3 the game changer?
Several services have evolved over the years, offering various levels of prefetching and pre-rendering to boost page load times and enhance the overall user experience on the web. These approaches tackle different layers of the internet stack, from boosting network connection speeds to preloading webpages closer to end-users.
P3 goes beyond prefetching and background pre-rendering. It leverages advanced AI technologies to analyze your webpage and determine specific optimization techniques to reduce its complexity without compromising appearance or functionality.  These optimizations may include converting image formats and embedding external CSS and JavaScript directly into the HTML document, which reduces the number of external resource requests.  As a result, P3 produces a fully optimized version of the page, loaded into the CDN cache and ready to serve instantly when users navigate to it. Here are some key features that distinguish P3 from other web optimization services.
Intelligent prefetching and pre-rendering based on user behavior or URL visibility
P3 uses AI to optimize specified pages in your origin and predict the pages users will likely navigate to. Using advanced algorithms, P3 prefetches and pre-renders pages that match your defined URL patterns. At the same time, it analyzes user behavior to anticipate additional pages they may visit, prefetching and optimizing them in the background. This combined approach minimizes wait times, providing users a fast and streamlined experience at every step.

Additionally, P3 saves significant computational resources and costs by pre-rendering only the URLs visible to the user as they scroll through the website rather than pre-rendering every link on the page. For example, on a checkout page, when a user scrolls to where the payment button is visible, only the payment page is pre-rendered. This approach reduces the number of requests and conserves resources.
Browser compatibility
A key advantage of P3 is its broad browser compatibility. While other similar services are limited to specific Chromium browsers, P3 works seamlessly across all browsers. If a feature like pre-rendering isn’t supported or if a page has a registered service worker, P3 defaults to native prefetching and pre-rendering to maintain a consistent experience for users across different browsers.
Precision control for page optimization
The prefetch optimization in P3 gives you granular control over which pages are optimized in your origin. You can specify individual URLs or use regex patterns to group pages with similar structures, making it easy to target specific areas of your site. P3 also allows you to serve prefetched HTML from the cache for matching URLs, ensuring that your most-visited pages are always ready to load instantly. It can also prefetch sub-resources for the first matching URL, keeping the process efficient and reducing unnecessary resource loading. [we may need to explain this last sentence more]
Deep prefetch for dynamic sub-resources 
Some websites rely on dynamic resources and assets not included in the HTML document for the page to load correctly. P3 uses the “deep prefetch” to retrieve and execute these resources within the pre-rendered page.
Now that we’ve covered what sets P3 apart from other services, let’s dive into the technical details of how P3 operates.
 
How P3 works
Policies
The foundation of P3’s approach lies in Policies. Policies are used to group pages and apply optimization rules to them. With Policies, you can define URL patterns of pages to be optimized, set the target region for content delivery, specify device types for tailored optimizations, and choose the level of optimization needed. You can also pass custom headers to the optimized content, ensuring precise control over how and where your content is delivered. Visit the official documentation to create a new Policy.
Optimizations
When users access a webpage, their request passes through the Content Delivery Network (CDN). If CDN is configured with P3, it directs the request to the P3 gateway. At this stage, the HTML ReWriter checks the memory cache for optimization rules matching the URL pattern. If applicable rules are found, they’re instantly applied, and the optimized page is returned to the user.
If there are no optimization rules in memory for that URL, the HTML ReWriter forwards the request to the P3 Controller. The Controller then checks for any configured policies that match the URL. If no policies are found, the request returns without P3 optimizations, pulling content directly from the origin back to the user.
However, if a policy does match, it triggers a new optimization job. This process involves three key phases:
Analyzer: P3’s AI-based engine actively learns the content of your web pages, training itself to find a combination of optimization rules that can be applied to your website. By assessing different combinations of optimization rules, it determines the best possible rules to boost your core web vitals. These optimizations can include bundling CSS and JS, inline CSS and JS, and optimizations for slow networks. For a complete list of optimizations, see the official P3 guide.
If your webpage is updated, P3 trains itself again on the new content to determine the updated optimizations required for it.
Validator: The Validator verifies these rules using computer vision to ensure that the optimizations don’t disrupt the page’s appearance, considering different device resolutions. Finally, it performs functional validation to ensure the optimizations don’t interfere with the page’s functionality.



	




Performance Proxy Metrics (PPM)
The Performance Proxy Metrics (PPM) service is a scheduled job that measures the performance of  Core Web Vitals for your website, such as First Contentful Paint (FCP) and Largest Contentful Paint (LCP). You can view these metrics and manage PPM jobs directly in the Performance Proxy dashboard. For more details, refer to the Manage Performance Proxy Metrics Job guide.


Conclusion
By setting a new benchmark for speed and resource efficiency, P3 is reshaping how users experience your website. It’s currently managed by the Macrometa team and to get started—reach out to our Sales team and discover what optimized performance can mean for your business!

For an in-depth guide to using P3, refer to the official documentation.
