# Website

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator, and [DocuNotion](https://github.com/AbstractSDK/docu-notion). The link to the importer can be found [here](https://www.notion.so/abstract-money/Docusaurus-Importer-1c946a0cd0c3807ca596f215527f26c3?pvs=4). Instructions for adding documents to this repository through Notion are documented there.

**Important Note:** DocuNotion will delete all markdown documents in the `docs` directory that are not coming from Notion. If you want to write a markdown document, make sure that you use the MDX extension. All of the docs are located in the `./docs` folder. Images should be co-located with the docs themselves.

### Installation

```
$ pnpm
```

### Local Development

```
$ pnpm start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```
$ pnpm build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

We are using GitHub Pages, and the workflows for GitHub Pages will automatically deploy the site once your PRs are merged.

### Pulling from Notion

```
$ pnpm pull-notion
```

This command will pull the latest changes from the Notion database for the docs and commit them to this repository. Please note that you will need to have defined the `DOCU_NOTION_INTEGRATION_TOKEN` and the `DOCU_NOTION_ROOT_PAGE`.

## Term
