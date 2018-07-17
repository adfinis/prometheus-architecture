# <Platform> Architecture

[![Build Status](https://travis-ci.org/adfinis-sygroup/prometheus-architecture.svg?branch=master)](https://travis-ci.org/adfinis-sygroup/prometheus-architecture)

This repository contains the source for the Adfinis SyGroup <Platform>
Architecture documentation.

The documentation is structured according to the [arc42](https://arc42.org/)
software architecture documentation template.

The architecture documentation in the repo get rendered into static HTML
pages by [hugo](https://gethugo.io). The resulting page is then deployed
to GitHub Pages through [travis](https://travis-ci.org/).

## Development

### Local Installation

After installing hugo as per [the installation docs](https://gohugo.io/getting-started/installing/)
you may run hugo to start a local development server on port 1313.

```bash
hugo server
```

You can now make changes to the markdown files in the `docs/` subdirectory and
hugo will watch the directory and reload your browser on each change.

### Docker Installation

If you do not wish to install hugo locally you may start the development server
in a docker container.

```bash
docker run --rm -ti -p 1313:1313 -v $(pwd):/src jojomi/hugo hugo server --bind 0.0.0.0
```

As with the local installation you can now connect to the development server
on port 1313 and the page will automatically get reloaded if you make changes
to the files in `docs/`.

## Deployment

The deployment of the final page to GitHub Pages is automated through travis.
Please look at [.travis.yml](./.travis.yml) for details on the CI/CD process.

## License

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

© We acknowledge that this document uses material from the arc 42
architecture template, <http://www.arc42.de>. Created by Dr. Peter
Hruschka & Dr. Gernot Starke.
