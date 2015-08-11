---
layout: post
title: Job hunting with Twitter
published: true
---

While I'm not job hunting at the moment, I was reminded the other day of a project I undertook when I was an unemployed student in Southampton: a Twitter feed for lazy jobhunters.

## The basic idea

The great thing about Twitter is the immediacy of updates and the flexibility of the platform. For many, Twitter has replaced RSS as the way of keeping up with news, as well as obviously the personal status updates.

The bad thing about job hunting online is the proliferation of sites advertising vacancies, also the sorting the wheat from the chaff aspect.

So what about combining the two? Why not make a Twitter bot that regularly posts a semi-curated feed of the latest jobs, drawing in adverts from a variety of sites and localised to your specific area?

## Technical challenges

Last time I did this it was honestly very straightforward. Most sites supplied properly formatted feeds for any given search query and it was a very quick job to run them through Twitterfeed, apply a few filters and start posting.

Unfortunately with the death of Google Reader there's little call for these feeds and in fact Gumtree et al have attempted to make it impossible to use their content in this way.

The logical thing to do is scrape but then you risk posting the same "featured content" again and again rather than showing a decent range of adverts.

## Solutions...and further investigations

Currently what I'm doing is taking a custom search from Gumtree, scraping it with Feed43, organising it into RSS using regular expressions, parsing that feed into tweets using Twitterfeed and links shortened by bit.ly and then posting the content.

The quick guide I read on regular expressions enabled me to identify the features of the promoted adverts and just ignore them completely. Gumtree only shows up to 20 results per page but for a feed refreshed half-hourly posting up to five times each refresh, this is in the region of enough content to keep the page fresh but few enough to avoid bombarding people.

Twitterfeed provides filters which I'm in the process of developing to get rid of spammy ads and bullshit people should be avoiding like Home Fundraising etc.

The next step is to implement the same sort of thing for Universal Jobmatch and Indeed - I will report back on the unexpected challenges that may arise...
