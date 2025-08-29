# eBay Discord Scraper Bot

## Overview
This project is a Discord bot that integrates with the **eBay Browse API**.  
It allows collectors and hobbyists to monitor new listings in real time and receive instant alerts directly in their Discord server.

## Features
- **Real-time listing alerts**: polls the eBay Browse API and posts new listings to Discord channels.
- **Filters**: supports maximum price, exclude keywords (e.g. exclude graded slabs), condition filtering, and more.
- **Smart graded detection**: automatically filters out PSA/BGS/CGC/SGC graded listings when requested.
- **Quota management**: built-in throttling and caching to avoid excessive API calls.
- **Discord commands**:
  - `/search add` – add a new search query with filters  
  - `/search list` – view all active searches  
  - `/search info` – view filters and settings for a search  
  - `/search test` – preview current listings without affecting state  
  - `/quota` – check API usage vs. daily quota  

## Why a Quota Increase is Needed
The default eBay Browse API quota of **5,000 calls/day** is quickly consumed when multiple users track multiple search queries.  
Even with optimizations (staggered polling, backoff, and caching), this limit prevents users from reliably receiving updates on new listings.  

We are requesting an increase to **20,000 calls/day** to support the current user base and ensure timely notifications.

## Responsible Usage
- Calls are **rate-limited** and staggered to prevent bursts.  
- Results are **cached** to avoid duplicate requests.  
- The bot only uses the **Browse API** and does not scrape eBay pages directly.  
- Intended solely for **legitimate buyer use cases** (collectors monitoring items).  

## Demo
This bot runs inside Discord. A test server can be provided if required.  
Example output of a new listing notification:

# Discord-Bot
Helps track ebay listings
