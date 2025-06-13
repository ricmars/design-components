# design-components

List of components available for Pega Platform Design Time

## index.json Schema

The `index.json` file contains information about available packages, their versions, and associated resources.

```json
{
  "packages": [
    // Array of package definitions
    {
      "package": "package-name", // Name of the package (e.g., "blueprint-import")
      "versions": [
        // Array of available versions for this package
        {
          "platformVersion": "xx.x.x" /* Compatibility with Pega Platform version (e.g., "23.1.0" or "23.1") - Could be a comma separated list like "8.8,23.1,...*/,
          "latestVersion": "x.x.x", // Latest version of this package (e.g., "1.0.1")
          "updateDate": "YYYY-MM-DD", // Date when package was last updated
          "binaries": [
            // Array of downloadable binary files - You should have at least one entry in the array
            {
              "name": "binary-name", // Name of the binary ("MAIN" is required - you can include other types of binaries) */
              "url": "binary-url" // URL to download the binary file
            }
          ],
          "documentation": [
            // Array of documentation resources
            {
              "name": "doc-name" /* Name of the documentation ("README" is required for documentation - you can include other types of documentations) */,
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
