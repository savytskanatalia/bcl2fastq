# bcl2fastq
bcl2fastq by Illumina
Elaborate manual with information on manual installation w/o Docker and more options for conversion can be found here:

https://support.illumina.com/content/dam/illumina-support/documents/documentation/software_documentation/bcl2fastq/bcl2fastq_letterbooklet_15038058brpmi.pdf

https://support.illumina.com/content/dam/illumina-support/documents/documentation/software_documentation/bcl2fastq/bcl2fastq2_guide_15051736_v2.pdf

# To install:
```
docker build - < Dockerfile -t bcltofastq
```
# To run:
```
docker run -it -u USER_N -v /directory_of_choice:/data  bcltofastq
```
# Before file conversion navigate to directory, containing RunInfo.xml
```
cd /run_directory_of_your_choice # Should contain RunInfo.xml
```

# To convert BCL files WITHOUT demultiplexing them:
```

bcl2fastq --input-dir /yourdirectory/blabla/Data/Intensities/BaseCalls --output-dir /yourdirectory
```

# As an output you will receive *.fastq.gz files, named after subfolders in basecalls folder of the input directory (e.g. flowcell names, lane numbers,...)


