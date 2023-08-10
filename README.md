# preservica-opex-complex-asset-example

This repo contains a sample OPEX package for ingesting into Preservica. The package creates 2 Structural Objects within Preservica and a single Information Object within the second SO. The Information Object has 2 child Content Objects, a `docx` and a `json` file. The Information Object is ingested as an unzipped PAX package.

```
SO: Folder A
    SO: Folder B
        IO: My Asset
            Representation Preservation
                CO: <filename>.docx
                    Generation
                        Bitstream
                CO: original_metadata.json
                    Generation
                        Bitstream
```

This example has been made to prove that OPEX ingests support abstracting file and folder names from the physical hierarchy when ingesting from systems such as S3 that do not encrypt object keys. When ingested the file and folder names are retrieved from the accompanying XIP and OPEX files to rebuild the physical hierarchy in Preservica.
