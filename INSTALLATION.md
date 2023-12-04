# INSTALLATION

## Local environment
- For the local development/testing environment, at least one AS server instance is required. It is not strictly required to have more than one instance of the AS server.
- A proxy web server may be useful for JS development, by defining a proxy to the source directories. Depending on the AS server, the proxy may be configured on it (please refer to the documentation of the server for informations on how to do so).
- Download the subprojects in a shared folder.
  - Create a `ivyLocalRepos/` folder at the same level as the subprojects for the lcoal compilation of the libraries.
  - To achieve the maximum reusability of the Ivy caching system, create a `ivycache/` folder at the same level as the subprojects and configure the `<project>/buildfiles/ivyconf.xml` file to refer to such folder.
- Compile the projects in the following order (so as to correctly configure the dependencies):
  - `siaccommon`
  - `siaccoritf`
  - `siacintegitf`
  - `siaccommonser`
  - `siaccommonapp`
  - `siacrepitf`
  - `siacbilitf`
  - The following may be compiled in any order:
    - `siccorser`
    - `siacbilser`
  - The following may be compiled in any order:
    - `siaccruapp`
    - `siacboapp`
    - `siacrepapp` (must configure the configuration parameter to refer to the report templates in the `siacreport` project)
    - `siacfinapp`
    - `siacbilapp`
- Configure the DBMS via the scripts in the `siacbdimpl` project.
- Deploy the `siacwebres` on an accessible web server.
- To test the backend resources, there are at least three ways:
  - deploy the backend project and use a SOAP client to access the resources.
  - deploy the backend project and execute a JUnit test on the frontend project to access the backend resource.
  - execute a JUnit test on the backend project (preferred way).
- Please be aware that the deployment of the projects may take a considerable amount of time due to metadata resolution.

## Production environment
For the production environment, the same configuration for the local environment may be used. We strongly suggest against using an exact replica of such configuration due to the load on the server.

- A load balancer should be configured with the "sticky session" configuration to acto as a reverse proxy to the AS instances.
  - The load balancer may also be used for the static resources access.
- Keep the DMBS and AS machine separated. The added overhead of the TCP connection between two distinct machines is far overshadowed by the load distribution.
- It is recommended to protect the URLs by preponing a WAF to the DMZ.
