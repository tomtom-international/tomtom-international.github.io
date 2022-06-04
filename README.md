# tomtom-international.github.io


Showcase site for hand-picked open-source projects by TomTom based on the excellent showcase site built by Spotify. It is built using Jekyll & GitHub Actions with a node.js script to fetch data from the GitHub GraphQL API adding it to a static YAML file in the repository.


## Development

**Install Jekyll & bundler gems**

```
gem install jekyll bundler
```

**Install yarn**

```
npm install --global yarn
```

**Install dependencies** inside of the project folder

```
yarn & bundle install
```

**Build & serve**

```
bundle exec jekyll serve
```

**(Optional) Test & update data**

[Create a personal GitHub Access Token](https://github.com/settings/tokens) to fetch & update the repository data locally. As the data is updated automatically using GitHub Actions `_data/projects_generated.yaml` should not be added to Git.

```
GH_TOKEN=YOUR_TOKEN node ./scripts/nightly.js
```

## Adding a project to the showcase website
You can add a project by adding it in the `projects.yaml` file.
Find the section for a specific coding language and add the following line to
the `projects:` section: `- url: <link of github repository`

Below is an example for a configuration of the Kotlin section:

```

- config:
    id: kotlin
    name: Kotlin
  projects:
    - url: https://github.com/tomtom-international/kotlin-tools

```

If there is no section available for your programming language you can add a new `- config:` section using a unique id and name. You can use the example above as a template.

---

This project adheres to the [Open Code of Conduct][code-of-conduct]. By participating, you are expected to honor this code.

[code-of-conduct]: https://github.com/tomtom-international/.github/blob/main/code-of-conduct.md
