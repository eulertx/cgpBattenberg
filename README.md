cgpBattenberg
=============

An installation helper, perl wrapper and the R program Battenberg which detects subclonality and copy number in matched NGS data.

| Master | Dev |
|---|---|
| [![Build Status](https://travis-ci.org/cancerit/cgpBattenberg.svg?branch=master)](https://travis-ci.org/cancerit/cgpBattenberg) | [![Build Status](https://travis-ci.org/cancerit/cgpBattenberg.svg?branch=dev)](https://travis-ci.org/cancerit/cgpBattenberg) |

## Battenberg R code
The Battenberg R code is developed and maintained in a separate repository [here](https://github.com/Wedge-Oxford/battenberg) and this is where any questions or issues specific to the R code should be directed.

## Installation

The battenberg R files are installed automatically from the Battenberg GitHub repository found [here](https://github.com/Wedge-Oxford/battenberg). The linked version is currently [`v2.2.5`](https://github.com/Wedge-Oxford/battenberg/releases/tag/v2.2.5).

Please install the following before attempting to run ``setup.sh <install_to_folder> [X/lib/perl:Y/lib/perl]``

1. [PCAP-core v2.1.3+](https://github.com/cancerit/PCAP-core/releases)
2. [alleleCount v3.0.1+](https://github.com/cancerit/alleleCount/releases)
3. [cgpVcf v2.0.1+](https://github.com/cancerit/cgpVcf/releases)

All of the items listed here use the same install method.

### Prerequisites

* Impute2 executables can be found [here](https://mathgen.stats.ox.ac.uk/impute/impute_v2.html)
  * Any impute related data for download
* BWA Mapped, indexed, duplicate marked/removed bam files, for both a matched normal and tumour sample
* Reference.fasta and index
* A file containing a list of contigs in the reference .fai to ignore

Some required data files are not included in the distribution but a script is included to generate these for you:

* Directory containing the 1000 genomes allele and loci data:
  * Generated using the included script ``download_generate_bberg_ref_files.pl``
* Impute info file ``impute_info.txt``
  * Generated using the included script ``download_generate_bberg_ref_files.pl``
* Prob loci file probloci.txt
  * Included: ``files/probloci.txt.gz``

Additionally, the wgs_gc_correction_1000g files need to be downloaded. These can be obtained from the Battenberg R code site [here](https://github.com/Wedge-Oxford/battenberg#required-reference-files).

## Program Run Instructions

For the most up to date usage instructions for the wrapper code please see the command line help:

    battenberg.pl -h

Please check the [wiki](https://github.com/cancerit/cgpBattenberg/wiki) for common problems before raising any issues.

----

LICENCE
=======
Copyright (c) 2014-2017 Genome Research Ltd.

Author: Cancer Genome Project cgpit@sanger.ac.uk

This file is part of cgpBattenberg.

cgpBattenberg is free software: you can redistribute it and/or modify it under
the terms of the GNU Affero General Public License as published by the Free
Software Foundation; either version 3 of the License, or (at your option) any
later version.

This program is distributed in the hope that it will be useful, but WITHOUT
ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more
details.

You should have received a copy of the GNU Affero General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.

1. The usage of a range of years within a copyright statement contained within
this distribution should be interpreted as being equivalent to a list of years
including the first and last year specified and all consecutive years between
them. For example, a copyright statement that reads 'Copyright (c) 2005, 2007-
2009, 2011-2012' should be interpreted as being identical to a statement that
reads 'Copyright (c) 2005, 2007, 2008, 2009, 2011, 2012' and a copyright
statement that reads "Copyright (c) 2005-2012' should be interpreted as being
identical to a statement that reads 'Copyright (c) 2005, 2006, 2007, 2008,
2009, 2010, 2011, 2012'."
