# design-components

List of components available for Pega Platform Design Time.

To view the list of components: [https://ricmars.github.io/design-components/](https://ricmars.github.io/design-components/)

For API access, use : [https://ricmars.github.io/design-components/index.json](https://ricmars.github.io/design-components/index.json)

## index.json Schema

The [index.json](https://ricmars.github.io/design-components/index.json) file contains information about available packages, their versions, and associated resources.

```json
{
  "packages": [
    // Array of package definitions
    {
      "package": "package-name", // Name of the package (e.g., "blueprint-import")
      "versions": [
        // Array of available versions for this package
        {
          /* Compatibility with Pega Platform version (e.g., "23.1.0" or "23.1") - Could be a comma separated list like "8.8,23.1,...*/
          "platformVersion": "xx.x.x",
          "latestVersion": "x.x.x", // Latest version of this package (e.g., "1.0.1")
          "updateDate": "YYYY-MM-DD", // Date when package was last updated
          "binaries": [
            // Array of downloadable binary files - You should have at least one entry in the array
            {
              // Name of the binary ("MAIN" is required - you can include other types of binaries) */
              "name": "binary-name",
              "url": "binary-url" // URL to download the binary file
            }
          ],
          "documentation": [
            // Array of documentation resources
            {
              /* Name of the documentation ("README" is required for documentation - you can include other types of documentations) */
              "name": "doc-name",
              "url": "doc-url" /* URL to access the documentation - could be from this repo or from a different domain */
            }
          ]
        }
      ]
    }
  ]
}
```

Each package can have multiple versions supporting different Pega Platform releases, with their respective binaries and documentation links.
