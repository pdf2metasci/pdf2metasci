### People that could be interested

- Meta-Rep Task Force "LLMs in metasci"
- Julian Quandt (Wien): 
	- Bulk download PDFs
	- Convert PDF to markdown
	- select focal p-values
- StatCheck Team
- [Jamie Cummins](https://www.dig.psy.unibe.ch/ueber_uns/personen/dr_cummins_jamie/index_ger.html) (RegCheck)
- Peter Hilpert
- Daniel Lakens + Lisa DeBruine: https://scienceverse.github.io/papercheck/
- René Bekkers: Research Transparency Check
- Johannes Breuer: Bibliometrie-Leute
- Matthew Vowels Matthew.vowels@unil.ch
- Andrea Hildebrandt

### Ressources:

- https://github.com/BERD-NFDI/turning-pdfs-into-research-data.io/tree/e52796ed0800105ded224ec691ddaf0c415f128d


### Steps

1. Identify actors (i.e., developers that work(ed) on solutions)
2. Create common platform: Github org
	1. Find a catchy name. pdf2metasci?
	2. README-Datei anlegen (mit der Pipeline + Tasks)
3. Identify existing open source software projects
4. Pipeline
	1. Construct a prototypical pipeline
	2. Split the pipeline in distinct tasks
		1. Search for paper dois (e.g., all papers from a journal): OpenAlex
		2. Bulk download OA and non-OA papers
		3. Convert PDF to markdown
		4. Extract key information from the paper text (with LLMs, regexp, ...): This is the most diverse step, as it depends on the research question
		5. Collect/Link trainingssets (hand-coded PDFs)
			1. Hilmar Brohmer: Coded dissertations for open science practices
	3. Collect existing tools for each task
		1. Do little benchmarking experiments: Which tool solves which task best? (Check computing time, quality of output, robustness)
	4. Create working groups to standardize the input/output interfaces between each task
	5. Publish exemplary combined pipelines (e.g., in different programing languages)
	6. Find consensus on one pipeline and start scraping OA papers; build up database (maybe a random selection of psych papers as a start?); 
5. Outlook / advanced projects:
	1. Have a "SETI@home" client: Let others contribute computing power to increase the database of scraped papers
		1. to be solved: 
			1. Where to store the database of parsed PDFs? How much storage space do we need? 
				1. Snapshot Torrents + incremental deltas on Github? (i.e., workers push scraped files to a Github folder. As soon as it reaches a certain size, we zip it and seed it as a new torrent file. Torrent files would )
			2. How to ensure data integrity (e.g., the markdown could be altered before upload)
	2. Think about psych-specific embedding models (cf. BioBERT)
6. Type of collaboration:
	1. Low key - *very* few synchronous meetings
	2. What is the benefit of contributing? Save time on your own pipeline, be more efficient
	3. Citations? Make the project citable (CFF file), ask users to cite. The main coordinator is first author.


### Next steps:

1. Create Github org: pdf2metasci
2. README-Datei anlegen (mit der Pipeline + Tasks)
3. Leute anschreiben --> Guter Pitch (Was sind die Vorteile?), als member in die org einladen.
4. Zoom-Treffen: Kennenlernen, jeder stellt ganz kurz seine Pipeline vor; Einigung auf die Task-Kategorien; Hausaufgabe: Jeder verlinkt seine Lösung an der richtigen Stelle.
5. Sobald die Grundstruktur steht: Breit bewerben um weitere Collaborators zu finden.

### Snippets for introduction:

- How to contribute: We expect that all steps of the tech stack will change - some slower (e.g. PDF conversion) some faster (e.g., LLM models). Therefore we will timestamp all benchmarks and recommendations.
- Goals:
	- Overarching goal: Do you want to convert scientific PDFs into data that can be used for meta-scientific research? We openly share our resources. Thereby we reduce research waste and increase efficiency by not re-inventing the wheel in common data processing pipelines.
	- Collect existing resources
	- Curate the best approaches
	- Benchmark
	- Demo pipelines for re-use
	- Connect the community, with breakout groups for defined, manageable tasks (e.g., specific benchmark studies)
