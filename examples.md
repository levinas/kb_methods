
# Assembly method example 1

Key | Value
--- | ---
Narrative method | Simplified Assembly From Reads
Used in narrative | Genome assembly and annotation
Used in frozen narratives | 1
Short description | This method allows users to assemble reads into contig sets 
Service called directly by narrative | assembly
Service that implements the core function | assembly
Calling program in narrative | https://github.com/kbase/narrative/blob/master/src/notebook/ipython_profiles/profile_narrative/kbase_templates/static/kbase/js/widgets/function_output/kbaseAssembly.js#L361
Service URL | http://kbase.us/services/assembly
Service method API used by narrative | curl --data job_request_data -X POST user/:user/job/new
Input description | The input dictionary "job_request_data" contains one typed object and one parameter
Input typed object 1 | AssemblyInput
Description of input object 1 | Information about the genome to be assembled and the read files (names, location, paired-end/single-end libraries, etc)
Input parameter 1 | Assembly recipe
Description of input parameter 1 | A curated recipe to be selected from a drop down menu
Input parameter 1 is mandatory | No 
Allowed value for input parameter 1 | { "auto", "spades", "smart", "kiki" }
Default value for input parameter 1 | "auto"

 
# Annotation method example 1
 
Key | Value
--- | ---
Narrative method | Annotate Genome
Used in narrative | Microbes Annotation
Used in frozen narratives | 1, 2, 3
Short description | This method allows users to annotate a genome with structural and functional annotations.
Service called directly by narrative | fbaModelServices
Service that implements the core function | annotate_workspace_Genome
Calling program in narrative | https://github.com/kbase/narrative/blob/master/src/notebook/ipython_profiles/profile_narrative/kbase_templates/static/kbase/js/fbaModelServices.js#L575
Service URL | http://kbase.us/services/fba_model_services
Service method API used by narrative | Invocation/RPC: fbaModelServices.annotate_workspace_Genome()
Input description | The input contains a Genome typed object and no other parameter
Input typed object 1 | Genome
Description of input object 1 | Information about the genome
