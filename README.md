## Microsoft Open Source Code of Conduct
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

Learn how to contribute at [Contribute to Dynamics 365 guidance content](https://learn.microsoft.com/en-us/dynamics365/get-started/contribute#dynamics-365-guidance-content) (for external contributors).  

## Local docs authoring and build

This repo is built with **DocFX** using the configuration in `guidance/docfx.json` and Open Publishing metadata in `.openpublishing.publish.config.json`.

### Required tools

- .NET SDK (for installing/running DocFX)
- DocFX CLI (`docfx`)

Install DocFX locally:

```bash
dotnet tool install --global docfx
```

### Build docs locally

From the repo root:

```bash
docfx guidance/docfx.json
```

The generated site is written to:

`guidance/dynamics365guidance`

### Edit and rebuild workflow

1. Edit Markdown files under `guidance/`.
2. Rebuild:

   ```bash
   docfx guidance/docfx.json
   ```

3. Preview the built output locally:

   ```bash
   docfx serve guidance/dynamics365guidance
   ```

> [!NOTE]
> This repo references shared content from dependent repositories in Open Publishing. A local standalone build may show warnings about missing includes unless those dependencies are also available.
