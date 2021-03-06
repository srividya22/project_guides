# KBase External Data Source Details

This document should be used for describing each KBase external data source in the following ways:

- How the external data source is being used in KBase, and any references to existing documentation and source code in the KBase GitHub project that describes this in more detail.
- What the license policy is of the data.
- What version or versions (if more than one copy of the data is used) are being used.
- A link or links to where the data can be accessed.
- A link or links to the documentation for this data.

---

## Data Sources

### ModelSEED

#### How ModelSEED is used in KBase

ModelSEED was the basis for the biochemistry database and the metabolic model reconstruction services in KBase. The KBase biochemistry database was initially based on a reformatted load of the entire ModelSEED biochemistry database. The KBase database has subsequently undergone additional curation and manual addition of reactions from other data sources, namely published manuscripts and published metabolic models.  

#### License for ModelSEED data

All data specific to ModelSEED is released under the ModelSEED Public License:
https://github.com/ModelSEED/ModelSEED/blob/master/LICENSE.TXT

However, some data in the ModelSEED is derived from other sources (e.g., KEGG), and that data carries its own potential licensing restrictions.

#### Versions of ModelSEED utilized

KBase loaded the 2012 version of the ModelSEED database.

#### Links to where ModelSEED can be accessed

http://seed-viewer.theseed.org/seedviewer.cgi?page=ModelView

---

### Kyoto Encyclopedia for Genes and Genomes (KEGG)

#### How KEGG is used in KBase

KEGG served as one data source for ModelSEED biochemistry database (see above), which forms the basis for all biochemistry in KBase. This biochemistry data is loaded into tables in the KBase central store and serves as the foundational data for all metabolic modeling services. The ModelSEED used raw ligand data reformatted from KEGG FTP dumps, adjusted for charge/pH, and loaded into our own database structures and formats. Overall, KBase includes the following specific data from KEGG:

- Molecular data from compounds found uniquely in KEGG including formula, chemical structure, and aliases
- Aliases and KEGG IDs from compounds found in multiple databases
- Stoichiometry and aliases for reactions found uniquely in KEGG
- Aliases and KEGG IDs for reactions found in multiple databases
- Coordinates for compounds and reactions from KEGG metabolic diagrams
- KEGG pathway organization for reactions found in KEGG

#### License for KEGG data

KEGG data was utilized for the ModelSEED project under the free academic license. No KEGG formatted data is directly accessible via KBase.

#### Versions of KEGG utilized

Release 62.0, April 1, 2012

#### Links to where KEGG can be accessed

http://www.genome.jp/kegg/

---

### IntAct

#### How IntAct is used in KBase

IntAct is one of our primary source for the protein-protein interaction in our central store.  

#### License for IntAct data
Creative Commons Attribution License 
http://www.ebi.ac.uk/intact/developer_resources

#### Links to where IntAct can be accessed

http://www.ebi.ac.uk/intact/

---

### Gene Expression Omnibus (GEO)
http://www.ncbi.nlm.nih.gov/geo/

#### How GEO is used in KBase
GEO is the primary source of public expression data.  This is what is used to populate the public KBase Expression data.  This is done by the Expression service.

#### License for GEO
http://www.ncbi.nlm.nih.gov/geo/info/disclaimer.html

"Copyright Status
Unless otherwise stated, documents and files on NCBI Web servers may be freely downloaded and reproduced. However, some material on this site, such as abstracts, may be copyright protected under the U.S. and foreign copyright laws. For such material, the submitting authors or publishers retain all rights for reproduction or redistribution. Permission to reproduce these documents may be required. All persons reproducing, redistributing, or making commercial use of this information are expected to adhere to the terms and conditions asserted by the copyright holder."

---

### Obofoundry - The Open Biological and Biomedical Ontologies
Top level collection of ontologies that are used in KBase. 

#### License for Obofoundry 
http://wiki.obofoundry.org/wiki/index.php/FP_001_open
Creative Commons CC-BY license version 4.0 or later.

#### Link to where obofoundry can be accessed

http://www.obofoundry.org/

---

#### Gene Ontologies : GO terms
Molecular function/Cellular components/Biological process ontologies - Associated with Features.
http://geneontology.org/

license - http://geneontology.org/page/use-and-license

#### Plant Ontologies : PO terms
Tissue and development ontologies - Associated with Expression Samples, GWAS.
http://www.plantontology.org/

license - http://www.plantontology.org/node/279 is licensed under a Creative Commons Attribution 4.0 International License. 

#### Plant Environmental Ontologies : EO terms
Environmental ontologies for plants - Associated with Expression Samples, GWAS.
http://wiki.plantontology.org/index.php/Plant_Environment_Ontology_Wiki

license - http://crop.cgrb.oregonstate.edu/node/1 is licensed under a Creative Commons Attribution 3.0 United States License.

#### Environmental Ontologies : ENVO terms
Environment Ontologies - Currently no expression data is associated with this, but it has the capability to do so.
http://environmentontology.org/

license - http://environmentontology.org/home/about-envo

"We hope that the community will adopt EnvO and benefit from its potential to promote standardised data integration and access. As an open project, we welcome your use of and participation in this project. Please contact us should you like to learn more!"

---

### Plant Metabolic Network

#### How Plant Metabolic Network is used in KBase

Plant Metabolic Network includes all of the plant metabolic pathway databases including AraCyc, PlantCyc, BarleyCyc, BrachypodiumCyc, ChlamyCyc, CornCyc, GrapeCyc, MossCyc, OryzaCyc, PapayaCyc, PoplarCyc, SelaginellaCyc, SetariaCyc, SorghumBicolorCyc, SoyCyc, SwitchgrassCyc.  

#### License for Plant Metabolic Network data
http://plantcyc.org/downloads/license_agreement.faces
This license is freely available to everyone, including commercial users

#### Links to where Plant Metabolic Network data can be accessed

http://plantcyc.org/downloads/data_downloads.faces

---

### Plant Reactome

#### How Plant Reactome is used in KBase

Plant Reactome is plant pathway database which hosts plant metabolic and regulatory pathways. Plant Reactome pathways are constructed by manual curation of pathways and reactions reported in the published literature or derived by orthology-based computational projections from curated pathways in the MetaCyc, Plant Metabolic Network, and Human Reactome databases. Pathways, reactions and gene entries in Plant Reactome are cross-referenced to many bioinformatics databases such as UniProt, ChEBI, PubChem, PubMed, Gramene and Plant Ensembl genomes and the Gene Ontology (GO).

#### License for Plant Reactome
http://plantreactome.gramene.org/copyright.html
Creative Commons Attribution 3.0 United States License.

#### Links to where Plant Reactome data can be accessed

http://plants.reactome.org/about.html

---

### UniProtKB

#### How UniProtKB is used in KBase

The UniProt Knowledgebase (UniProtKB) provides functional information on proteins, with accurate, consistent and rich annotation. It has two sections - Swiss-Prot and TrEMBL. UniProtKB/Swiss-Prot is a high quality manually annotated and non-redundant protein sequence database, which brings together experimental results, computed features and scientific conclusions. UniProtKB/TrEMBL contains high quality computationally analyzed records that are enriched with automatic annotation and classification. These UniProtKB/TrEMBL unreviewed entries are kept separated from the UniProtKB/Swiss-Prot manually reviewed entries so that the high quality data of the latter is not diluted in any way. 

#### License for UniProtKB
http://www.uniprot.org/help/license
Creative Commons Attribution-NoDerivs License

#### Links to where UniProtKB can be accessed

http://www.uniprot.org/downloads

---

### Ensembl Plants/Gramene

#### How Ensembl Plants/Gramene is used in KBase

Ensembl Plants is a joint project of EBI and Gramene. KBase uses Ensembl Plants/Gramene as a resource for plant genomes, ontology, pathway, interpro, and gene trees. 

#### License for Ensembl Plants
The terms of use of Ensembl data and code are summarised on the following page: http://www.ensembl.org/info/about/legal/index.html.  
The EMBL-EBI terms of use also apply: http://www.ebi.ac.uk/about/terms-of-use.
Gramene terms of use is here: http://www.gramene.org/node/225
Ensembl and Gramene do not place any license restrictions on the data that they produce although they do retain copyright. Their code is explicitly licensed using the Apache v2.0 license.  As noted, their databases may contain information that is subject to third-party constraints of various kinds and users of the Ensembl data and software are solely responsible for determining what these constraints are and complying with them.


#### Links to where Ensembl Plants/Gramene can be accessed

Ensembl Plants: http://plants.ensembl.org/index.html
Gramene: http://gramene.org/

---

### Phytozome

#### How Phytozome is used in KBase

Phytozome is the public portal to JGI's plant genome data and analysis. Currently KBase uses Phytozome as an additional resource for released plant genomes which are not available at Ensembl Plants/Gramene. Phytozome will also be used to provide diversity, expression data and many other data types to KBase in future. 

#### License for Phytozome
Phytozome does not license or distribute any code associated with Phytozome. Phytozome is ©2006-2015 University of California Regents. All rights reserved. 

Download policy is given on this link: http://genome.jgi.doe.gov/pages/dynamicOrganismDownload.jsf?organism=PhytozomeV10
"Some of the data available on this portal are pre-publication data and may contain errors. The goal of our policy is that early release should enable the progress of science. By accessing these data, you agree not to publish any articles containing analyses of genes or genomic data on a whole genome or chromosome scale prior to publication by JGI and its collaborators of its comprehensive genome analysis. These restrictions will be lifted on the publication of the whole genome description or as specified on the information for each organism. During this waiting period, the data will be available for any kind of publication that does not compete directly with planned publications (e.g. reserved analyses) of the JGI and collaborators. A principal collaborator or "champion," listed in the organsim's Info page and is the point of contact and arbiter regarding publication plans. Scientists are strongly encouraged to contact the principal collaborator and JGI about their intentions and any potential collaboration. Each directory within this portal has a file describing the release policy of that data. People who access data are expected to adhere to those policies."

#### Links to where Phytozome can be accessed
http://phytozome.jgi.doe.gov/pz/portal.html

---

### Pfam

#### How Pfam is used in KBase

Pfam is used by the Gene Families service to search for domains in
genomes.

#### License for Pfam data
Pfam is freely available under the Creative Commons Zero ("CC0") licence.
http://pfam.xfam.org/about

#### Links to where Pfam can be accessed

http://pfam.xfam.org/

---

### TIGRFAMs

#### How TIGRFAMs is used in KBase

TIGRFAMs is used by the Gene Families service to search for domains in
genomes.

#### License for TIGRFAMs data

Copyright 1995-2014 The J. Craig Venter Institute. All rights
reserved.

This data is provided "AS IS". The J. Craig Venter Institute
makes no Representation or warranty, express or
implied, including without limitation any warranties of
merchantability or fitness for a particular purpose, associated
with the receipt or use of this data.

This database is free; you can redistribute it and/or modify it under
the terms of the GNU Library General Public License as published by
the Free Software Foundation; either version 2 of the License, or (at
your option) any later version.

In summary, you are free to redistribute *verbatim* copies of TIGRFAMs
or any TIGRFAMs files in any way you like, so long as your copy
of TIGRFAMs retains our copyright notice and the GNU license. You may also
make *modified* copies of TIGRFAMs and distribute them, but your derivative
database must be freely distributed under the GNU LGPL. Proprietary
modification of the TIGRFAMs database is prohibited, except by a separate
formal licensing agreement from the J. Craig Venter Institute.

ftp://ftp.jcvi.org/pub/data/TIGRFAMs/COPYRIGHT

#### Links to where TIGRFAMs can be accessed

http://www.jcvi.org/cgi-bin/tigrfams/index.cgi

---

### CDD

#### How CDD is used in KBase

CDD is used by the Gene Families service to search for domains in
genomes.  In addition to the NCBI-curated CDD domain models, we also
search against CDD libraries for SMART (Simple Modular Architecture
Research Tool) and for COGs (clusters of orthologous groups).

#### License for CDD data

Databases of molecular data on the NCBI Web site include such examples
as nucleotide sequences (GenBank), protein sequences, macromolecular
structures, molecular variation, gene expression, and mapping
data. They are designed to provide and encourage access within the
scientific community to sources of current and comprehensive
information. Therefore, NCBI itself places no restrictions on the use
or distribution of the data contained therein. Nor do we accept data
when the submitter has requested restrictions on reuse or
redistribution. However, some submitters of the original data (or the
country of origin of such data) may claim patent, copyright, or other
intellectual property rights in all or a portion of the data (that has
been submitted). NCBI is not in a position to assess the validity of
such claims and since there is no transfer or rights from submitters
to NCBI, NCBI has no rights to transfer to a third party. Therefore,
NCBI cannot provide comment or unrestricted permission concerning the
use, copying, or distribution of the information contained in the
molecular databases.

http://www.ncbi.nlm.nih.gov/About/disclaimer.html

#### Links to where CDD can be accessed

http://www.ncbi.nlm.nih.gov/Structure/cdd/cdd.shtml

---
