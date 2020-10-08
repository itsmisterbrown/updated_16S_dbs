# updated 16S databases for marker gene taxonomic assignment

This is a modified version of the [Silva trainset 138 (Version 2)](https://zenodo.org/record/3986799#.X2GWbWdKh24), which was constructed from the version 138 release of the [Silva Small Subunit rRNA database](https://www.arb-silva.de/documentation/release-138/)

All databases are formatted for compatibility with the [DADA2 workflow](https://benjjneb.github.io/dada2/tutorial.html)

### Note:
Performing the standard _assignTaxonomy()/addSpecies()_ workflow with _silva_nr99_v138_train_set_BPB_091820_updated.fa.gz__ and _silva_species_assignment_v138_BPB_091820.fa.gz__ 
__does not__ produce identical results to _assignTaxonomy()_ with _silva_nr99_v138_wSpecies_train_set_BPB_091820_updated.fa.gz_ and, unfortunately, both seem to provide annotations that the other does not.
It is unknown why this is the case, s my recommendation would be to try both and see which yields better results for your dataset. Obviously, one advantage of the annotating solely with _silva_nr99_v138_wSpecies_train_set_BPB_091820_updated.fa_ is that it saves oen computational step.

Modifications to the default version of this database include the addition of several key vaginal bacteria that have remained out of most 16S databases.
Taxa added are documented below ([Genbank accession](https://www.ncbi.nlm.nih.gov/genbank/) numbers are listed in parentheses):

## Bacterial vaginosis–associated bacteria (BVAB):

_BVAB1_ (AY724739); Annotated as _Lachnocurva vaginae_  
_E.coli_ coordinates: __113:1004__   

* Citations: [Fredericks et al. 2005 NEJM](https://www.nejm.org/doi/full/10.1056/NEJMoa043802), 
[Holm et al. 2020 Front. Cell. Infect. Microbiol.](https://www.frontiersin.org/articles/10.3389/fcimb.2020.00117/full)
 


_BVAB2_ (AY724740); Annotated as _Saccharofermentans BVAB2_  
_E.coli_ coordinates: __101:1006__  

* Citations: [Fredericks et al. 2005 NEJM](https://www.nejm.org/doi/full/10.1056/NEJMoa043802)  


_BVAB3_ (AY724741); Annotated as _Mageeibacillus indolicus_  
_E.coli_ coordinates: __101:1010__  
* Citations: [Fredericks et al. 2005 NEJM](https://www.nejm.org/doi/full/10.1056/NEJMoa043802),
[Austin et al. 2014 Anaerobe](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4385425/)  

## Others
_Sneathia/Leptotrichia amnionii_ (AY724742); Annotated as _Sneathia amnii_  
_E.coli_ coordinates: __101:1009__  
* Citations: [Fredericks et al. 2005 NEJM](https://www.nejm.org/doi/full/10.1056/NEJMoa043802), 
[Harwich et al. 2012 BMC Genomics](https://bmcgenomics.biomedcentral.com/articles/10.1186/1471-2164-13-S8-S4)

_Eggerthella species Type 1_ (AY738656); Annotated as _Eggerthella T1_  
_E.coli_ coordinates: __95:1000__  
* Citations: [Fredericks et al. 2005 NEJM](https://www.nejm.org/doi/full/10.1056/NEJMoa043802), 
[McClelland et al. 2018 Lancet ID](https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(18)30058-6/fulltext)

_TM7-H1 isolate E1_ (CP026537); Annotated as _TM7-H1 E1_  
_E.coli_ coordinates: __8:1540__  
* Citations: [Fettweis et al. 2019 Nature Medicine](https://www.nature.com/articles/s41591-019-0450-2) 

## Relative performance

The image below was generated from datasets of stools from 149 South African infants (Fecal; V6 region; HiSeq 2500) and vaginal swabs from 564 adult African women (Vaginal; V3-4 regions; MiSeq). The Silva database used was Version 132, but this version (138) should perform even better.

![alt text](https://github.com/itsmisterbrown/updated_16S_dbs/blob/master/RDP_v_Silva.png "RDP v Silva")

