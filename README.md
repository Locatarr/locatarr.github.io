# Locatarr

<p>
 <a href="https://github.com/Locatarr/locatarr.github.io/issues"><img alt="contributions welcome" src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat" /></a>
</p>

Locating *Arr services and aggregating them into a single list.
Feel free to open a [PR](https://github.com/Locatarr/locatarr.github.io/pulls) with apps that aren't listed!

## Contributing

There are 2 json files in root of the repository ([`arr-services.json`](arr-services.json) and [`other-helpful-apps.json`](other-helpful-apps.json)) which contain the data for the tables that are shown on [locatarr.github.io](https://locatarr.github.io).
In order to add or modify the tables on the website, simply fork the repository, update the appropriate json file, and open a new PR into the `master` branch.
Order doesn't matter in the JSON file as the applications are sorted by name before being inserted into the website.

## How the system works

This repository utilizes GitHub Actions & Jekyll to build a fully rendered, static webpage to be hosted on GitHub Pages.

In order to generate markdown from the JSON files located in the repo, a [custom GitHub action](https://github.com/Locatarr/markdown-table-generator) reads in each JSON file and emits a markdown table generated from the contents.
The tables are then inserted into a template file which contains all of the static portions of the final website output.

Once the final markdown file is constructed, the [actions/jekyll-build-pages](https://github.com/actions/jekyll-build-pages) utilizes Jekyll to generate a Pages-compatible website which is then uploaded to the Pages environment.

## License

The Locatarr website is licensed under the Apache 2.0 License.

See [the LICENSE file](LICENSE) for details.

## Misc

**See Also:** [What Happened to rustyshackleford36/locatarr](https://github.com/Locatarr/locatarr.github.io/discussions/3)
