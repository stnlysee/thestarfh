The StarFH Google Search Console indexing fix

What was added/fixed:
1. Added .htaccess redirect rules for Apache/cPanel hosting.
2. Added _redirects for Netlify hosting.
3. Added vercel.json for Vercel hosting.
4. Updated robots.txt to clearly allow crawling and point to the sitemap.
5. Updated sitemap.xml with lastmod/changefreq for the canonical homepage.
6. Existing canonical tag in index.html is already correct:
   https://www.the-starfh.com/

Important:
Use only the redirect file that your hosting supports.
- cPanel/Apache: use .htaccess
- Netlify: use _redirects
- Vercel: use vercel.json

After uploading:
1. Visit these URLs in a browser:
   http://the-starfh.com/
   http://www.the-starfh.com/
   https://the-starfh.com/
   https://www.the-starfh.com/index.html

   They should all redirect to:
   https://www.the-starfh.com/

2. In Google Search Console:
   - Open URL Inspection
   - Inspect https://www.the-starfh.com/
   - Click Test Live URL
   - Click Request Indexing
   - Go to Sitemaps and resubmit:
     https://www.the-starfh.com/sitemap.xml

Notes about the GSC messages:
- Page with redirect is usually okay if it is the non-preferred URL redirecting to the preferred URL.
- Alternate page with proper canonical tag is usually okay if Google recognises the preferred canonical page.
- Crawled currently not indexed means Google crawled the URL but has not chosen to index it yet. This often improves after the canonical homepage is clear, the sitemap is resubmitted, and the site has stronger unique text/content.
