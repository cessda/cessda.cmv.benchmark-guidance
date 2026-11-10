# CESSDA Benchmark Guidance

See <https://docs.tech.cessda.eu/platform/documentation_tooling.html> for detailed documentation on how to use this repository,
as well as descriptions on what the files in this repository do.

## Technical Implementation

The documentation is written in markdown files and compiled to html using [Jekyll](https://jekyllrb.com)
with the [CESSDA theme](https://rubygems.org/gems/jekyll-cessda-docs) based on the
[Just the docs](https://github.com/pmarsceill/just-the-docs) theme.

## Getting started

Requires Ruby 3.1 or later (the CI image uses 3.1.1) and [Bundler](https://bundler.io/).
The Ruby that ships with macOS is too old; [install a current one](https://jekyllrb.com/docs/installation/),
for example with Homebrew (`brew install ruby`).

```shell
git clone https://github.com/cessda/cessda.cmv.benchmark-guidance.git
cd cessda.cmv.benchmark-guidance
gem install jekyll bundler
bundle install
```

Build the site into the `_site/` directory:

```shell
bundle exec jekyll build
```

Or serve it with automatic rebuilds, then open <http://localhost:4000>:

```shell
bundle exec jekyll serve
```

Sass deprecation warnings from the theme during the build are expected and can be ignored.

To run the same checks as CI:

```shell
bundle exec rake lint
bundle exec jekyll build
bundle exec rake htmlproofer
```

## Development

The documentation is written using Markdown files with Jekyll headers.
Coding follows the [Google Style Guide for Markdown](https://google.github.io/styleguide/docguide/style.html),
including ATX style headers and a maximal line lengths of 140 characters.

Style Guide compliance is checked with [markdownlint](https://github.com/markdownlint/markdownlint) by running

```shell
bundle exec rake lint
```

## Navigation

The home page is *index.md*

Create child and grandchild pages as required, to organise the document into sections and sub-sections.

Search for the word `TODO` to see places where the name of your Product should be inserted.

Use *document-navigation-structure.md* to keep track of the navigation structure.
