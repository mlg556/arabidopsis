README for ATH_GO annotation and GOSLIM file.

The ATH_GO document is a tab-delimited file containing GO annotations for
Arabidopsis genes annotated by TAIR, UNIPROT and the GO Consortium, IntAct and TIGR with terms from the Gene OntologyConsortium controlled vocabularies (see www.geneontology.org). This
file includes an updated set of literature based annotations and
electronic annotations based upon matches to INTERPRO domains. Ontologies and
annotations can also be searched/browsed at: 

http://arabidopsis.org/servlets/Search?action=new_search&type=keyword

You can search this file by locus name on line at: 
 
http://arabidopsis.org/tools/bulk/go/index.jsp

This file is updated on a monthly basis.

Please cite this paper when using TAIR's GO annotations in your research:

Berardini, TZ, Mundodi, S, Reiser, R, Huala, E, Garcia-Hernandez, M,
Zhang, P, Mueller, LM, Yoon, J, Doyle, A, Lander, G, Moseyko, N, Yoo,
D, Xu, I, Zoeckler, B, Montoya, M, Miller, N, Weems, D, and Rhee, SY
(2004) Functional annotation of the Arabidopsis genome using
controlled vocabularies. Plant Physiol. 135(2):1-11.

Column headers :explanation

1. locus name: standard AGI convention name

2. TAIR accession:the unique identifier for an object in the TAIR database- 
the object type is the prefix, followed by a unique accession number(e.g. gene:12345).  

3. object name : the name of the object (gene, protein, locus) being annotated.

4. relationship type: the relationship between the annotated object and the GO term

5. GO term: the actual string of letters corresponding to the GO ID

6. GO ID: the unique identifier for a GO term.  

7. TAIR Keyword ID: the unique identifier for a keyword in the TAIR database.

8.  Aspect: F=molecular function, C=cellular component, P=biological 13process. 

9. GOslim term: high level GO term helps in functional categorization.

10. Evidence code: three letter code for evidence types (see: http://www.geneontology.org/GO.evidence.html).

11. Evidence description: the analysis that was done to support the annotation

12. Evidence with: supporting evidence for IGI, IPI, IC, IEA and ISS annotations

13. Reference: Either a TAIR accession for a reference (reference table: reference_id) or reference from PubMed (e.g. PMID:1234).  

14. Annotator: TAIR, TIGR, GOC (GO Consortium), UniProt, IntAct or a TAIR community member

15. Date annotated: date the annotation was made.


Reference explanations:

You can link to the TAIR detail pages for the references using the following base URL:

http://www.arabidopsis.org/servlets/TairObject?accession=Publication:xxxxxx
http://www.arabidopsis.org/servlets/TairObject?accession=Communication:xxxxxx
http://www.arabidopsis.org/servlets/TairObject?accession=AnalysisReference:xxxxxxx

1. publication or PMID:
For literature based annotations the associated reference is given for either 
PubMed (PMID) or TAIR (publication:reference_id).

2. For electronic annotations (IEA evidence code) the Analysis References refer to either 

a. a TargetP run on the latest version of the Arabidopsis genome annotation
b. an INTERPROScan run + INTERPRO2GO mapping run on the latest version of the Arabidopsis genome annotation
c. annotations made during the creation of the AraCyc database using Pathologic Software.  A hand-edited file of enzyme names, based on TIGR annotations, was used as the input parameter and the output was manually curated.

_______________________________________________________________________________

----------
DATA REUSE POLICY: From the Terms of Use, full text available here: http://www.arabidopsis.org/doc/about/tair_terms_of_use/417

"Upon your agreement to utilize the Service on the terms described herein, you may extract, download, and make copies of limited excerpts of the information contained in the Service as necessary for your academic and non-profit use. You may create works based on the data and freely redistribute those works. You may not otherwise copy, replicate, share, redistribute, or facilitate access to substantial subsets of the Data or Materials or the Service or in any form, for example, the files in the Subscriber_Data_Releases folder, without written permission from Phoenix Bioinformatics. Files in the Public_Data_Releases folder are made available to the public under the CC-BY 4.0 license (https://creativecommons.org/licenses/by/4.0/).
...
By using the Service, you agree to provide attribution to TAIR. To attribute the use of the Data to TAIR, you must cite at least one TAIR publication in the way specified at http://www.arabidopsis.org/about/citingtair.jsp or in a substantially similar manner. You must also supply the URL of these Terms of Use: http://www.arabidopsis.org/doc/about/tair_terms_of_use/417. "
-----------------









