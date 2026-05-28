[update-readmes]   Mode: rewrite — migrating to template structure...
# fess-crawler

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/fess-crawler)

<!-- AI:start:what-it-does -->
_Description pending._
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
_Architecture documentation pending._
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/fess-crawler.git
cd fess-crawler
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration


### XML Configuration

Fess Crawler uses XML-based configuration with LastaFlute DI. Place configuration files in your classpath:

```xml
<!-- crawler.xml -->
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE components PUBLIC "-//DBFLUTE//DTD LastaDi 1.0//EN"
    "http://dbflute.org/meta/lastadi10.dtd">
<components namespace="fessCrawler">
    <component name="crawler" class="org.codelibs.fess.crawler.Crawler" instance="prototype"/>
    <component name="httpClient" class="org.codelibs.fess.crawler.client.http.HcHttpClient" instance="singleton"/>
    <component name="fileTransformer" class="org.codelibs.fess.crawler.transformer.impl.FileTransformer" instance="singleton"/>
</components>
```

### Crawler Context Configuration

```java
// Set maximum number of URLs to crawl
crawler.crawlerContext.setMaxAccessCount(1000);

// Set number of crawler threads
crawler.crawlerContext.setNumOfThread(10);

// Set maximum crawl depth
crawler.crawlerContext.setMaxDepth(3);

// Set request interval (politeness)
crawler.crawlerContext.setDefaultIntervalTime(1000); // 1 second
```

### URL Filtering

```java
// Include patterns
crawler.urlFilter.addInclude("https://example.com/.*");
crawler.urlFilter.addInclude(".*\\.pdf$");

// Exclude patterns  
crawler.urlFilter.addExclude(".*\\.js$");
crawler.urlFilter.addExclude(".*login.*");
```

## CI

<!-- AI:start:ci -->
_CI documentation pending._
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/fess-crawler`](https://github.com/Interested-Deving-1896/fess-crawler) and mirrored through:

```
Interested-Deving-1896/fess-crawler  ──►  OpenOS-Project-OSP/fess-crawler  ──►  OpenOS-Project-Ecosystem-OOC/fess-crawler
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
_Contributors pending._
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[Apache-2.0](https://github.com/Interested-Deving-1896/fess-crawler/blob/master/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
