Classic multi-page architecture has a few benefits:

### Better empty-cache performance: 

your site can render faster. As web browsers become more privacy-focused and users spread their browsing across multiple web-capable devices, empty-caches visits are increasingly common. Faster sites make more money. Read WPO Stats. Search engines use site performance as a search ranking signal, which makes good performance crucial.

### Inclusive and robust by default: 

You are in full control the minimum requirements necessary to visit your site. You needn’t put any undue burden on the capabilities of the web browser of your visitors. You needn’t place your site behind a “Best Viewed In” browser-compatibility warning. If they can view HTML, they can view your site.

### Energy-efficiency: 

Lighter pages result in safer long sessions that are more energy efficient and won’t drain your visitors’ laptop or mobile device batteries.

### Privacy-focused: 

* working without client-JavaScript allows visitors full control over their viewing experience. 
* This allows you to create sites that work best in the harsh real world environment of browser extensions, content and ad-blockers; even working with those rare folks that browse with JavaScript disabled.

### Searchable by default: 

A simpler architecture for server rendered content makes it straightforward for search engines to find you.
Better defaults for accessibility-focused page navigations, preserving scroll position, forward/back button support, etc.

Single Page Application frameworks have pivoted away from client-side rendering to server-rendering and we welcome this improvement. However, the large starting size of client JavaScript bundles customary to SPA persist: Remix (228 kB), Next.js (248 kB), Gatsby (210 kB), and Nuxt (191 kB) source. Notably, these large bundle sizes are only the minimum for a Hello World project and will only grow as your project grows (and as the frameworks grow over time, too).

You can’t JavaScript your way out of an excess-JavaScript problem. These large JavaScript bundles are costly to site performance.

Single Page Application advocates argue these large, costly bundles enable performance gains for future navigations, seamless media playback during transition, and fancy transition animations. While we can debate (and even agree on some of) those points (recognizing also that they will fade into irrelevance as the web platform progresses), take a moment to consider whether or not this trade-off should be made for you as a default.