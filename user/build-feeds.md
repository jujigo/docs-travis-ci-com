---
title: Atom Build Feeds
layout: en

---

One way to get updates on your builds is an Atom feed.

You can read it in your favorite RSS reader, or programmatically consume it
with scripts.

## Atom Feeds

Every repository on Travis CI has its own Atom feed, which includes all builds that were run on it, with both pull requests and normal commits.

The feeds are fetched directly from our API at `https://api.travis-ci.org`.

The canonical URL for a repository's builds is:

```
https://api.travis-ci.org/repos/travis-ci/travis-ci/builds
```

This URL returns a JSON representation by default, but you can get the Atom feed by adding the `.atom` suffix:

```
https://api.travis-ci.org/repos/travis-ci/travis-ci/builds.atom
```

## Private Repositories

For private repositories, you need a token to subscribe to
the feed. The API endpoint is different too: `https://api.travis-ci.com`

1. The token is the same as is used to fetch a build status image, which can be
   found on the repository page. See the related
   [documentation](/user/cc-menu/#using-the-cc-feed-with-repositories)
   for more details on how to access the token.

2. Once you have the token, append it as the `token` parameter to the URL:

   ```
   https://api.travis-ci.com/repos/travis-ci/billing/builds.atom?token=<token>
   ```
