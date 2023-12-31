API Setup and installation
===========================

Requirements
--------------

An Ensembl API checkout including:

- [ensembl-genomio](https://github.com/Ensembl/ensembl-genomio)  (export /src/perl and /src/python into PERL5LIB and PYTHONPATH respectively)
- [ensembl-hive](https://github.com/Ensembl/ensembl-hive)
- [ensembl-production](https://github.com/Ensembl/ensembl-production)
- [ensembl-analysis](https://github.com/Ensembl/ensembl-analysis/tree/dev/hive_master) (on dev/hive_master branch)
- [ensembl-taxonomy](https://github.com/Ensembl/ensembl-taxonomy)
- [ensembl-orm](https://github.com/Ensembl/ensembl-orm)

Software
--------------

- Python 3.8+
- Bioperl 1.6.9+

Python Modules
--------------
- bcbio-gff
- biopython
- jsonschema
- mysql-connector-python
- requests
- python-redmine


## Installation
--------------
### Directly from GitHub:
```
git clone https://github.com/Ensembl/ensembl-genomio
git clone https://github.com/Ensembl/ensembl-analysis -b dev/hive_master
git clone https://github.com/Ensembl/ensembl-production
git clone https://github.com/Ensembl/ensembl-hive
git clone https://github.com/Ensembl/ensembl-taxonomy
git clone https://github.com/Ensembl/ensembl-orm
```