# Insta-web-scraper
# iscrape


A basic web scraper for Instagram using R. This package retrieves user and hashtag metrics from Instagram, such as the number of posts, followers, and following.

## Features
- **User Metrics:**
  - Number of posts
  - Number of followers
  - Number following

- **Hashtag Metrics:**
  - Number of posts

## Installation

Ensure you have R installed on your system. Then, install the required dependencies and iscrape using the following commands:

```R
install.packages(c("devtools", "dplyr", "httr", "stringr"), dep = TRUE)
devtools::install_github("royfrancis/iscrape")
```

## Usage

### User Page Metrics

To retrieve metrics for a user, use the username. Here's an example using the official "instagram" account:

```R
library(iscrape)

# Get user webpage
pu <- get_page_user("instagram")

# Get post count, follower count, and following count
get_count_post(pu)
get_count_follower(pu)
get_count_following(pu)
```

To retrieve multiple user metrics at once:

```R
get_page_info(c("instagram", "travelandleisure", "minimalism"))
```

### Hashtag Metrics

Retrieve the number of posts for a given hashtag:

```R
# Get hashtag webpage
ph <- get_page_hashtag("instagram")

# Get post count for the hashtag
get_count_hashtag(ph)
```

## Disclaimer

- Web scraping is discouraged by Instagram. Excessive scraping may result in your IP address being blocked.
- Using a VPN is recommended.
- This package was developed for personal use and relies on text pattern matching. Future changes to Instagram's page structure may cause the functions to break.
- The package is not actively maintained.

A basic web scraper for Instagram using R.

## Support

Feel free to fork or report issues if you encounter any problems
