### KNOWN ISSUES:

* The overhead incurred by the agent is too high for high-load production
  apps.
* The method used to make instrumentation pervasive touches a lot of the
  core of Node.js and is both slow and potentially fragile.
* The agent works only with Node.js 0.6 and newer.
* The agent uses memory very inefficiently.
* Transaction traces do not correctly set up the parent-child call
  relationships necessary for meaningful transaction traces.
* Server-side configuration is unavailable until support is added within
	the core New Relic application.

### TO DO:

* Additional third-party instrumentation:
    1. Redis
    2. PostgreSQL
    3. CouchDB
    4. mikael/request
* Proxy support.
* Better tests for existing instrumentation.
* Replace callstack-based shim with domains.
* Lots more testing of what the data looks like in RPM.
* Publish a build of the agent via NPM.
* Refine how transaction traces gather and report time used.
* Instrumentation for HTTPS connections.
* Simpler instrumentation for web services using the core HTTP module.