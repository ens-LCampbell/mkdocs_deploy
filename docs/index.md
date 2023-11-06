# [Ensembl-genomio](https://github.com/Ensembl/ensembl-genomio)

A repository dedicated to pipelines used to turn basic genomic data into formatted 
Ensembl core databases. Also allow users to dump core databases into various formats.

File formats handled : FastA, gff3, JSON (*following BRC4 specifications*).

Check out the :doc:`usage` section for further information of requirements to
run ensembl-genomio pipelines.

Ehive pipelines
-------------------------------------------
1. __Genome loader__: Creates an Ensembl core database from a set of flat files.
2. __Genome dumper__: Dumps flat files from an Ensembl core database.

Contents
--------
Check out ref:`installation <install>` section for further information on how 
to install the project.

1. [Usage](usage.md)
2. [Install](install.md)
3. [License](license.md)

## Project layout
    ensembl/
	├── brc4
	│   └── runnable
	│       ├── compare_fasta.py
	│       ├── compare_report.py
	│       ├── core_server.py
	│       ├── download_genbank.py
	│       ├── dump_stable_ids.py
	│       ├── extract_from_gb.py
	│       ├── fill_metadata.py
	│       ├── gff3_specifier.py
	│       ├── integrity.py
	│       ├── json_schema_factory.py
	│       ├── load_sequence_data.py
	│       ├── manifest.py
	│       ├── manifest_stats.py
	│       ├── prepare_genome.py
	│       ├── read_json.py
	│       ├── say_accession.py
	│       └── seqregion_parser.py
	└── io
	    └── genomio
	        ├── assembly
	        │   └── get_assembly_data.py
	        ├── db_factory.py
	        ├── events
	        │   └── format_events.py
	        ├── events_dumper.py
	        ├── events_loader.py
	        ├── fastaprep
	        │   └── process_fasta.py
	        ├── genbank
	        │   ├── extract_from_genbank.py
	        │   └── get_genbank.py
	        ├── genome_metadata
	        │   ├── compare_genome_stats.py
	        │   ├── dump_genome_metadata.py
	        │   └── dump_genome_stats.py
	        ├── gff3
	        │   ├── functional_annotation.py
	        │   └── process_gff3.py
	        ├── integrity.py
	        ├── manifest_maker.py
	        ├── manifest_stats.py
	        ├── metadata
	        │   ├── prepare_genome.py
	        │   ├── prepare_seq_region.py
	        │   └── update_genome_metadata.py
	        ├── schemas
	        │   ├── json_schema_factory.py
	        │   └── json_schema_validator.py
	        ├── seq_region_dumper.py
	        └── utils
	            ├── archive_utils.py
	            └── json_utils.py


## Project Module Overview

<!-- <Placeholder> -->

## Acknowledgements

I want to thank my house plants for providing me with
a negligible amount of oxygen each day. Also, I want
to thank the sun for providing more than half of their
nourishment free of charge.

Indices and tables
==================
<TO DO>

# MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

