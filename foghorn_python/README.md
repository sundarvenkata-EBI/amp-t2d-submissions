VCF compression tool 
====================

### What is This?
This python tool converts vcf file into cVCF format as used by the AMP-T2D knowledge portals genetic analysis interactive tool (GAIT)

### Prerequisites
This package depends on the following packages (e.g. on RedHat 7):
```commandline
python-wheel python2-pip
```

To install all the other Python dependencies with virtualenv:
```commandline
git clone https://github.com/EBIvariation/amp-t2d-submissions
cd amp-t2d-submissions/foghorn_python
virtualenv -p python2.7 venv
source venv/bin/activate
pip install -r requirements.txt
deactivate
```

### Using the scripts
To use, stream a vcf to the tool with with an outfile flag and compression type
```commandline
zcat inVCF.vcf.gz | python foghorn_python.py -o outfile -GT[DS]
```

The GT flag implements the genotype compression algorithm 

The DS flag implements the gene dosage compression algorithm
