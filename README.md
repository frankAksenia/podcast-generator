# Podcast Generator

Automatically generate and publish a podcast RSS feed from your repository using GitHub Actions.

## Features

* Generates a valid podcast RSS feed
* Runs automatically with GitHub Actions
* Simple Python-based implementation
* No external services required
* Easy to customize for any podcast

## Installation

Add this action to your workflow:

```yaml
name: Generate Podcast Feed

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v5

      - uses: actions/setup-python@v5
        with:
          python-version: "3.10"

      - name: Generate feed
        run: python feed.py
```

## Repository Structure

```text
.
├── .github/
│   └── workflows/
│       └── podcast.yml
├── feed.py
└── README.md
```

## Usage

1. Fork or clone this repository.
2. Configure your podcast metadata in the feed generator.
3. Commit and push changes.
4. GitHub Actions will generate and update the RSS feed automatically.

## Example Output

The generated RSS feed can be submitted to podcast directories such as:

* Apple Podcasts
* Spotify for Creators
* Pocket Casts
* Overcast
* Amazon Music

## Customization

You can modify:

* Podcast title
* Description
* Author information
* Episode metadata
* Artwork URL
* Feed URL
* Categories

## Requirements

* Python 3.10+
* GitHub Actions enabled
* Repository write permissions for workflow commits

## Contributing

Issues and pull requests are welcome.

## License

MIT License.
