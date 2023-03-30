# Module 07 - The what, why, and how of metadata management

## What is metadata?

Metadata in its broadest form is 'the data about the data'. Metadata provides the spatio-temporal context for digital sequence information, and may be vital for interpreting and contextualising results. For biodiversity genomics data (a.k.a. digital sequence information; DSI), the core metadata is defined by community standards such as the [Genomics Standards Consortium](https://www.gensc.org/index.html) and [Biodiversity Information Standards](https://www.tdwg.org/), including the MIGS and [MIxS](https://genomicsstandardsconsortium.github.io/mixs/) specifications. 

<figure>
  <center><img src="https://github.com/GenomicsAotearoa/data-management-resources/blob/main/docs/figures/5Ws+H-Metadata.png?raw=true" alt="The Data Lifecycle" style="width:65%" class="center"></center>
  <figcaption>
    An overview of the minimum metadata for genomic data.
  </figcaption>
</figure>

For processed data, metadata will also include information such as what software, software versions, and parameters were used. Additional metadata may include associated keywords, downstream publications, funding sources, and data access and licensing details. To get an idea of metadata beyond the minimum, check out the [Darwin Core terms](https://dwc.tdwg.org/list/) for an extensive list. 

## Why should we be collecting and managing metadata?

Metadata should be recorded and managed alongside DSI to ensure that results produced using these data can be placed into the appropriate context. Collation and stewardship of metadata is also essential to ensure that data meet the requirements of the FAIR Principles, and so facilitating the traceability and future use of data. Not only that, but metadata describing the spatiotemporal context for data enables the connection of DSI to Indigenous communities, facilitating benefit-sharing into the future as described by the [CARE Principles for Indigenous Data Sovereignty](https://www.gida-global.org/care).

## How can we best manage metadata?

At its core, metadata collation and stewardship all come down to the need for thorough and consistent record-taking and record-keeping throughout the lifespan of a project - from sample collection through to dissemination of results. Starting early will save you from headaches down the track! 

Portals such as the Genomic Observatories MetaDatabase ([GEOME](https://geome-db.org/)) and the Collaborative Open Plant Omics ([COPO](https://copo-project.readthedocs.io/en/latest/copo-about.html)) allow users to generate template to populate with metadata associated with DSI. By using existing templates, users can ensure that metadata is recorded in ways that are consistent with biodiversity genomics community standards.

Tools such as version control, software containers, and workflow management systems can be extremely helpful in tracking metadata during data processing and analysis. These tools can be particularly useful when shared across the research group, along with guidelines for directory structure and file naming conventions, ensuring time-wide consistency.

## Further reading

* Crandall, E. D. et al. (2023). Importance of timely metadata curation to the global surveillance of genetic diversity. Conservation Biology, 00(e14061). https://doi.org/10.1111/cobi.14061
* Field, D., et al. (2008). The minimum information about a genome sequence (MIGS) specification. Nature Biotechnology, 26(5), Article 5. https://doi.org/10.1038/nbt1360
* Yilmaz, et al. (2011). Minimum information about a marker gene sequence (MIMARKS) and minimum information about any (x) sequence (MIxS) specifications. Nature Biotechnology, 29(5), Article 5. https://doi.org/10.1038/nbt.1823


*[MIGS]: Minimum Information about a Genome Sequence
*[MIxS]: Minimum Information about any (X) Sequence
*[DSI]: Digital Sequence Information
*[FAIR Principles]: FAIR Guiding Principles for scientific data management and stewardship, aiming to improve the Findability, Accessibility, Interoperability, and Reuse of data.
*[CARE Principles]: CARE Principles for Indigenous Data Governance, that aim to ensure that Indigenous Data is managed in such a way as to maintain Collective Benefit, Authority to Control, Responsibility, and Ethics. 
