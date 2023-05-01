# Module 05 - Data Management Plans in practice

A data management plan (DMP), sometimes referred to as a data management and sharing plan, defines a framework for how researchers use and interact with data under our care. In this Module, we’ll look to our personas for examples of why DMPs are an essential research tool and provide some suggestions to springboard researchers looking to develop their first DMP. 

## The newbie tackling a new project

<p>
  <img src="https://github.com/GenomicsAotearoa/data-management-resources/blob/main/docs/figures/Taylor-profile.png?raw=true" alt="Profile image of Taylor Smith" style="float:left;height:120px;"> <a href="https://genomicsaotearoa.github.io/data-management-resources/personas/persona1/">Taylor</a> is a fresh-eyed PhD student excited to be working on a new project for a culturally significant species. No previous work has been done, so Taylor will need to develop a DMP from scratch. Taylor will work closely with their supervisor, <a href="https://genomicsaotearoa.github.io/data-management-resources/personas/persona3/">Professor Nepia</a>, who holds established relationships with Indigenous research partners with cultural connections to the focal species. To clearly communicate the terms under which the data will be generated, used, and accessed by all parties they need to establish a DMP for this project. 
</p>

<p>
  <img src="https://github.com/GenomicsAotearoa/data-management-resources/blob/main/docs/figures/Tehara-profile.png?raw=true" alt="Profile image of Professor Nepia" style="float:right;height:120px;"> To co-design a DMP that is fit-for-purpose, Professor Nepia leverages her previous experience to balance institutional responsibilities, research objectives, and priorities of Indigenous research partners. For instance, the university has a mandate for researchers to provide DMPs, the project will generate a large amount of data from hundreds of samples collected at various locations, and Indigenous research partners' desire to maintain kaitiakitanga. Through conversations between Taylor, Professor Nepia, Indigenous research partners, and representatives from a national wildlife department, Taylor has identified institutional commitments, research requirements, and Indigenous needs around the data. They have collated these in a table so they can clearly understand their obligations. 
  </p>

| What | When | Where| Who |
|--|--|--|--|
| Project: whole genome resequencing of a lizard species, many individuals sampled from across the species range sequenced to moderate depth, a reference genome sequenced and assembled  | Start date: ASAP | Processing & storage: Institutional computation and storage resources | Data custodian: Professor Nepia on behalf of Indigenous research partners during the research life cycle |
| Metadata: project title, funding organisation, project ID, species, sample IDs, geographic location, collection date, details of ethics permits, Indigenous affiliations, primary contact details | Project duration: 4 years | DMP in development | Different groups involved with data collection and generation: national wildlife department - long-term species monitoring, Taylor - sample collection with Indigenous community members, lab work, analysing data and preparing research outputs, sequencing facility  - producing raw DSI  |
| Data types: blood and/or tissue samples, digital sequence data, environmental data. Blood/tissue samples will be held on behalf of the Indigenous research partners at the university during the project. | DSI to be generated within the next 12 months | Agreement with local sequencing facility for data generation and secure transfer | Decision-making is in partnership - Indigenous research partners, key representatives of national wildlife department, with context for decisions provided by Taylor and Professor Nepia |
| File types to be generated: raw DSI (FASTQ files), genome assembly files, BAM alignment files, variant call files, spreadsheets, analysis results || Sampling notes in hard copy (field notebooks) with key metadata transcribed into spreadsheets housed in institutional cold storage | Potential for data reuse, but conditions for this yet to be determined |
| Data protection requirements and potential data reuse are being actively discussed by decision-makers | | | |
| DSI volume to be generated: on the order of terabytes. Keeping Darryl appraised of data storage needs will help the eResearch team allocate appropriate resources to the project. | | | |

Professor Nepia and Taylor recognise this will be an iterative and collaborative process, requiring regular engagement with the community so all parties are briefed regularly on progress, and to continue conversations to ensure the resulting DMP will serve the intended purpose while being responsive to change. With this information in hand, Taylor and Professor Nepia are now equipped to begin work on developing a DMP that satisfies these needs. 

## The experienced data manager

<p>
<img src="https://github.com/GenomicsAotearoa/data-management-resources/blob/main/docs/figures/Atsushi-profile.png?raw=true" alt="Profile image of Dr Atsushi Sato" style="float:left;height:100px;"> <a href="https://genomicsaotearoa.github.io/data-management-resources/personas/persona2/">Dr Sato</a> is an old hand when it comes to operating under established DMPs. Although he finds data management an onerous part of the research process, he recognises its importance, and has developed skills to help him adhere to DMPs in his daily workflows. He understands that as a middle-man for diverse data sets, it is important that he familiarises himself with access and usage requirements. 
  </p>
  
In Dr Sato’s case, leveraging datasets with different data management requirements is not uncommon. He relies on collaborators to provide a well-defined DMP alongside the data. He is tasked with the role of identifying the practical intersection between technical aspects such as data storage and computing needs, and governance as determined by existing DMPs. While Taylor and Professor Nepia are concerned with development of a DMP, Dr Sato has to adhere to DMPs that have been defined by collaborators. 

In his role, Dr Sato generates large quantities of intermediate analysis files, and typically hands off data to other collaborators once analysis is complete. He is less concerned with long-term storage requirements, and more with the here-and-now of these data sets. Similarly to Taylor, he has created a table of his data management concerns and considerations.

| Who | What | When | Where | Why | How |
|--|--|--|--|--|--|
| Project: Climate change impacts on adaptation of fisheries stocks | Secure data transfer required, with restricted data access | Data generated at external institutions iteratively over past 5 years | Very comprehensive metadata supplied by collaborators | Computationally intensive so requires national HPC infrastructure | Some data being reused for purposes other than that initially determined |
| Collaborators leading the project are acting as data custodians and decision-makers for data management | | Atsushi intends to complete work on this project within the next 6 months | DMP provided by collaborators - but this lacks information on whether some key files are available for reuse | | Supplied data and outputs to be deleted following delivery of results as per DMP |
| Data supplied is BAM/CRAM alignment and variant call files including thousands of samples along with climate data, on the order of terabytes | |  | Analysed data to be returned to collaborators, supplied data to be deleted on completion | | Accessed on the national compute infrastructure via Atsushi's private project directory |

Among these concerns, he observes a shortfall in one of these existing DMPs, that lacks guidance for the potential reuse of key intermediate files. While this small oversight is not the end of the world, he will need to discuss this with his collaborators, who may need to revise this DMP. 

## The foundation of a DMP

By having done the background thinking and having discussions around data management for a proposed project you will be well prepared to develop a DMP. Some examples of what may be covered in a DMP include: 

* Data types
* Data formats and standards
* Data roles and responsibilities
* Data dissemination
* Data sharing & access
* Archiving & persistence

While some funding bodies or institutes may designate specific templates, these are likely to cover fairly similar aspects and can be readily adapted to suit. Considering the [5Ws (+H)](https://github.com/GenomicsAotearoa/data-management-resources/blob/main/docs/figures/5Ws-eResearch-support-staff-draft-v2.png?raw=true) for your project should help you to populate any template.


## Resources for developing a Data Management Plan

DMPs are widely used across the research, science, and innovation sector. As such, there is no need to reinvent the wheel - leverage the wide array of available resources to help you get started! 

### Online data management resources 

The [Digital Curation Centre](https://www.dcc.ac.uk/guidance/how-guides/develop-data-plan) provides useful guides and advice to help you get started.

[MANTRA](https://mantra.ed.ac.uk/) is a free, online non-assessed course with guidelines to help you understand and reflect on how to manage the digital data you collect throughout your research. It has been crafted for the use of post-graduate students, emerging researchers, and information professionals. It is freely available on the web for anyone to explore on their own. 

### Online resources for developing Data Management Plans

* Use a checklist to see if you need to create a DMP: https://www.dcc.ac.uk/guidance/how-guides

* Check out [10 simple rules for creating a good DMP](https://datamanagement.hms.harvard.edu/plan-design/data-management-plans) for useful guidelines on what to include in DMPs. 

* To create your own DMP, you can try out the Digital Curation Centre's [Data Management Plan Tool](https://dmponline.dcc.ac.uk/), or the [Data Stewardship Wizard](https://ds-wizard.org/), which is used Horizon Europe and other international funding bodies, and which incorporates version control.

### Other ways to learn about Data Management Plans

* Attend a course on Data Management at your local institute.

* Reach out to your institute's Data Librarian, Data Stewards, or Research Data Management teams for expert assistance and support.

*[DMP]: Data Management Plan
*[DSI]: Digital sequence information
*[HPC]: High performance computing
*[kaitiakitanga]: (te reo Māori) guardianship, protection  
