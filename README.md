# Project Title
CONTABILIA

Contabilit&agrave; per i grandi enti pubblici

# Project Description
This is a multi-module project handling the accounting for the Public Administration.

The modules are as follow:
- libraries (please note that the order reflects the interdependencies):
  - [siaccommon]( https://github.com/unica-open/siaccommon ): common and transversal dependencies for the various subproject
  - [siaccoritf]( https://github.com/unica-open/siaccoritf ): service interfaces for the CORE functionalities
  - [siaccommonser]( https://github.com/unica-open/siaccommonser ): common and transversal dependencies for the SERVICE subprojects
  - [siaccommonapp]( https://github.com/unica-open/siaccommonapp ): common and transversal dependencies for the WEBAPP subprojects
  - [siacintegitf]( https://github.com/unica-open/siacintegitf ): service interfaces for the INTEGRATION functionalities
  - [siacrepitf]( https://github.com/unica-open/siacrepitf ): service interfaces for the REPORT ENGINE functionalities
  - [siacbilitf]( https://github.com/unica-open/siacbilitf ): service interfaces for the ACCOUNTING (BILancio) functionalities
- backend services:
  - [siaccorser]( https://github.com/unica-open/siaccorser ): service implementation for the CORE functionalities
  - [siacbilser]( https://github.com/unica-open/siacbilser ): service implementation for the ACCOUNTING (BILancio) functionalities
- frontend services:
  - [siaccruapp]( https://github.com/unica-open/siaccruapp ): webapp for the DASHBOARD (CRUSCOTTO) functionalities
  - [siacbilapp]( https://github.com/unica-open/siacbilapp ): webapp for the ACCOUNTING (BILANCIO) functionalities
  - [siacfinapp]( https://github.com/unica-open/siacfinapp ): webapp for the FINANCING functionalities
  - [siacboapp]( https://github.com/unica-open/siacboapp ): webapp for the BACKOFFICE functionalities
  - [siacrepapp]( https://github.com/unica-open/siacrepapp ): webapp for the REPORT ENGINE functionalities
- transversal:
  - [siacbatch]( https://github.com/unica-open/siacbatch ): CLI/batch projects to be invoked by a scheduler
  - [siacreport]( https://github.com/unica-open/siacreport ): reporting template for the report engine
  - [siacdbimpl]( https://github.com/unica-open/siacdbimpl ): database implementation, with all the required scripts
  - [siacetlbo]( https://github.com/unica-open/siacetlbo ): backoffice for the ETL (Extract, Transform, Load) functionalities
  - [siacetlmigr]( https://github.com/unica-open/siacetlmigr ): migration via ETL (Extract, Transform, Load) functionalities
  - [siacwebres]( https://github.com/unica-open/siacwebres ): static web resources for the webapps
  - [siacscripts]( https://github.com/unica-open/siacscripts ): CLI scripts for automation and executions

# Configurations
For the configuration of each single module, please refer to the
README.md file which is present in each module.

# Getting Started
Please refer to the Prerequisites section to gather the requested configuration prior to configure the project.

Please refer to the Installing section for specifications about the installation process.

# Prerequisites
- The Java projects are written in UTF-8 and are compatible with Java 1.6.0_41
- (Compilation only) The `JAVA_HOME` environment variable is required to point to the Java 1.6.0_41 JDK home folder
- The Java runtime used is 1.8.0_73
- Apache Ant for the building process
- Apache Ivy for dependencies management
- All the libraries listed in the BOM.csv must be accessible to compile the project. the libraries are published at [http://repart.csi.it](http://repart.csi.it), but are also included in the `lib/` folder for simplicity
- A "JEE 6 full profile"-compatible Application Server (tested on JBoss EAP 6.4.0)
- The correct version for the DBMS (tested on PostgreSQL 9.6)

# Installing
Please refer to the [INSTALLATION.md](./INSTALLATION.md) file for the steps
required for the installation

# Contributing
Please read [CONTRIBUTING.md](./CONTRIBUTING.md) for details on our code of conduct,
and the process for submitting pull requests to us.

# Versioning
We partially use Semantic Versioning for versioning. (http://semver.org) \
A major version increment in SemVer standard corresponds to a non-compatible upgrade of the project;
yet a non-compatible upgrade to the project not necessarily corresponds to a major version increment.

# Authors
See the list of contributors who participated in this project in file [AUTHORS.txt](./AUTHORS.txt).

# Copyrights
See the list of copyrighters in this project in file Copyrights.txt
“&copy; Copyright CSI Piemonte – 2020”.

# License
SPDX-License-Identifier: EUPL-1.2-or-later\
See the [**"EUPL v1_2 IT-LICENSE.txt"**](./EUPL%20v1_2%20IT-LICENSE.txt)
and [**"EUPL v1_2 EN-LICENSE.txt"**](./EUPL%20v1_2%20EN-LICENSE.txt) files for details
