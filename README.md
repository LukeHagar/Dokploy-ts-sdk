# dokploy

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *dokploy* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=dokploy&utm_campaign=typescript"><img src="https://www.speakeasy.com/assets/badges/built-by-speakeasy.svg" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/lukehagar/lukehagar). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

Dokploy API: Endpoints for dokploy

More information about the API can be found at http://app.dokploy.com/api/settings.getOpenApiDocument
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [dokploy](#dokploy)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

> [!TIP]
> To finish publishing your SDK to npm and others you must [run your first generation action](https://www.speakeasy.com/docs/github-setup#step-by-step-guide).


The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add <UNSET>
```

### PNPM

```bash
pnpm add <UNSET>
```

### Bun

```bash
bun add <UNSET>
```

### Yarn

```bash
yarn add <UNSET>
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { Dokploy } from "dokploy";

const dokploy = new Dokploy({
  authorization: process.env["DOKPLOY_AUTHORIZATION"] ?? "",
});

async function run() {
  const result = await dokploy.admin.getOne();

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name            | Type | Scheme      | Environment Variable    |
| --------------- | ---- | ----------- | ----------------------- |
| `authorization` | http | HTTP Bearer | `DOKPLOY_AUTHORIZATION` |

To authenticate with the API the `authorization` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { Dokploy } from "dokploy";

const dokploy = new Dokploy({
  authorization: process.env["DOKPLOY_AUTHORIZATION"] ?? "",
});

async function run() {
  const result = await dokploy.admin.getOne();

  console.log(result);
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [admin](docs/sdks/admin/README.md)

* [getOne](docs/sdks/admin/README.md#getone)
* [createUserInvitation](docs/sdks/admin/README.md#createuserinvitation)
* [removeUser](docs/sdks/admin/README.md#removeuser)
* [getUserByToken](docs/sdks/admin/README.md#getuserbytoken)
* [assignPermissions](docs/sdks/admin/README.md#assignpermissions)

### [application](docs/sdks/application/README.md)

* [create](docs/sdks/application/README.md#create)
* [getOne](docs/sdks/application/README.md#getone)
* [reload](docs/sdks/application/README.md#reload)
* [delete](docs/sdks/application/README.md#delete)
* [stop](docs/sdks/application/README.md#stop)
* [start](docs/sdks/application/README.md#start)
* [redeploy](docs/sdks/application/README.md#redeploy)
* [saveEnvironment](docs/sdks/application/README.md#saveenvironment)
* [saveBuildType](docs/sdks/application/README.md#savebuildtype)
* [saveGithubProvider](docs/sdks/application/README.md#savegithubprovider)
* [saveGitlabProvider](docs/sdks/application/README.md#savegitlabprovider)
* [saveBitbucketProvider](docs/sdks/application/README.md#savebitbucketprovider)
* [saveDockerProvider](docs/sdks/application/README.md#savedockerprovider)
* [saveGitProdiver](docs/sdks/application/README.md#savegitprodiver)
* [markRunning](docs/sdks/application/README.md#markrunning)
* [update](docs/sdks/application/README.md#update)
* [refreshToken](docs/sdks/application/README.md#refreshtoken)
* [deploy](docs/sdks/application/README.md#deploy)
* [cleanQueues](docs/sdks/application/README.md#cleanqueues)
* [readTraefikConfig](docs/sdks/application/README.md#readtraefikconfig)
* [updateTraefikConfig](docs/sdks/application/README.md#updatetraefikconfig)
* [readAppMonitoring](docs/sdks/application/README.md#readappmonitoring)

### [auth](docs/sdks/auth/README.md)

* [createAdmin](docs/sdks/auth/README.md#createadmin)
* [createUser](docs/sdks/auth/README.md#createuser)
* [login](docs/sdks/auth/README.md#login)
* [getOne](docs/sdks/auth/README.md#getone)
* [logout](docs/sdks/auth/README.md#logout)
* [update](docs/sdks/auth/README.md#update)
* [generateToken](docs/sdks/auth/README.md#generatetoken)
* [get](docs/sdks/auth/README.md#get)
* [generate2FASecret](docs/sdks/auth/README.md#generate2fasecret)
* [verify2faSetup](docs/sdks/auth/README.md#verify2fasetup)
* [verifyLogin2FA](docs/sdks/auth/README.md#verifylogin2fa)
* [disable2FA](docs/sdks/auth/README.md#disable2fa)
* [sendResetPasswordEmail](docs/sdks/auth/README.md#sendresetpasswordemail)
* [resetPassword](docs/sdks/auth/README.md#resetpassword)
* [confirmEmail](docs/sdks/auth/README.md#confirmemail)

### [backup](docs/sdks/backup/README.md)

* [create](docs/sdks/backup/README.md#create)
* [get](docs/sdks/backup/README.md#get)
* [update](docs/sdks/backup/README.md#update)
* [remove](docs/sdks/backup/README.md#remove)
* [manualBackupPostgres](docs/sdks/backup/README.md#manualbackuppostgres)
* [manualBackupMysql](docs/sdks/backup/README.md#manualbackupmysql)
* [manualBackupMariadb](docs/sdks/backup/README.md#manualbackupmariadb)
* [manualBackupMongo](docs/sdks/backup/README.md#manualbackupmongo)

### [bitbucket](docs/sdks/bitbucket/README.md)

* [create](docs/sdks/bitbucket/README.md#create)
* [get](docs/sdks/bitbucket/README.md#get)
* [providers](docs/sdks/bitbucket/README.md#providers)
* [getRepositories](docs/sdks/bitbucket/README.md#getrepositories)
* [getBranches](docs/sdks/bitbucket/README.md#getbranches)
* [testConnection](docs/sdks/bitbucket/README.md#testconnection)
* [update](docs/sdks/bitbucket/README.md#update)

### [certificates](docs/sdks/certificates/README.md)

* [create](docs/sdks/certificates/README.md#create)
* [get](docs/sdks/certificates/README.md#get)
* [remove](docs/sdks/certificates/README.md#remove)
* [all](docs/sdks/certificates/README.md#all)

### [cluster](docs/sdks/cluster/README.md)

* [getNodes](docs/sdks/cluster/README.md#getnodes)
* [removeWorker](docs/sdks/cluster/README.md#removeworker)
* [addWorker](docs/sdks/cluster/README.md#addworker)
* [addManager](docs/sdks/cluster/README.md#addmanager)

### [compose](docs/sdks/compose/README.md)

* [create](docs/sdks/compose/README.md#create)
* [getOne](docs/sdks/compose/README.md#getone)
* [update](docs/sdks/compose/README.md#update)
* [delete](docs/sdks/compose/README.md#delete)
* [cleanQueues](docs/sdks/compose/README.md#cleanqueues)
* [fetchSourceType](docs/sdks/compose/README.md#fetchsourcetype)
* [randomizeCompose](docs/sdks/compose/README.md#randomizecompose)
* [getConverted](docs/sdks/compose/README.md#getconverted)
* [deploy](docs/sdks/compose/README.md#deploy)
* [redeploy](docs/sdks/compose/README.md#redeploy)
* [stop](docs/sdks/compose/README.md#stop)
* [getDefaultCommand](docs/sdks/compose/README.md#getdefaultcommand)
* [refreshToken](docs/sdks/compose/README.md#refreshtoken)
* [deployTemplate](docs/sdks/compose/README.md#deploytemplate)
* [getTemplates](docs/sdks/compose/README.md#gettemplates)
* [getTags](docs/sdks/compose/README.md#gettags)

### [deployment](docs/sdks/deployment/README.md)

* [get](docs/sdks/deployment/README.md#get)
* [allByCompose](docs/sdks/deployment/README.md#allbycompose)
* [allByServer](docs/sdks/deployment/README.md#allbyserver)

### [destination](docs/sdks/destination/README.md)

* [create](docs/sdks/destination/README.md#create)
* [testConnection](docs/sdks/destination/README.md#testconnection)
* [getOne](docs/sdks/destination/README.md#getone)
* [get](docs/sdks/destination/README.md#get)
* [remove](docs/sdks/destination/README.md#remove)
* [update](docs/sdks/destination/README.md#update)

### [docker](docs/sdks/docker/README.md)

* [getContainers](docs/sdks/docker/README.md#getcontainers)
* [restartContainer](docs/sdks/docker/README.md#restartcontainer)
* [getConfig](docs/sdks/docker/README.md#getconfig)
* [getContainersByAppNameMatch](docs/sdks/docker/README.md#getcontainersbyappnamematch)
* [getContainersByAppLabel](docs/sdks/docker/README.md#getcontainersbyapplabel)


### [domain](docs/sdks/domain/README.md)

* [create](docs/sdks/domain/README.md#create)
* [byApplicationId](docs/sdks/domain/README.md#byapplicationid)
* [byComposeId](docs/sdks/domain/README.md#bycomposeid)
* [generateDomain](docs/sdks/domain/README.md#generatedomain)
* [update](docs/sdks/domain/README.md#update)
* [get](docs/sdks/domain/README.md#get)
* [delete](docs/sdks/domain/README.md#delete)

### [github](docs/sdks/github/README.md)

* [one](docs/sdks/github/README.md#one)
* [getRepositories](docs/sdks/github/README.md#getrepositories)
* [getBranches](docs/sdks/github/README.md#getbranches)
* [getProviders](docs/sdks/github/README.md#getproviders)
* [testConnection](docs/sdks/github/README.md#testconnection)
* [update](docs/sdks/github/README.md#update)

### [gitlab](docs/sdks/gitlab/README.md)

* [create](docs/sdks/gitlab/README.md#create)
* [one](docs/sdks/gitlab/README.md#one)
* [providers](docs/sdks/gitlab/README.md#providers)
* [getGitlabRepositories](docs/sdks/gitlab/README.md#getgitlabrepositories)
* [getGitlabBranches](docs/sdks/gitlab/README.md#getgitlabbranches)
* [testConnection](docs/sdks/gitlab/README.md#testconnection)
* [update](docs/sdks/gitlab/README.md#update)

### [gitProvider](docs/sdks/gitprovider/README.md)

* [getAll](docs/sdks/gitprovider/README.md#getall)
* [remove](docs/sdks/gitprovider/README.md#remove)

### [mariadb](docs/sdks/mariadb/README.md)

* [create](docs/sdks/mariadb/README.md#create)
* [get](docs/sdks/mariadb/README.md#get)
* [start](docs/sdks/mariadb/README.md#start)
* [stop](docs/sdks/mariadb/README.md#stop)
* [saveExternalPort](docs/sdks/mariadb/README.md#saveexternalport)
* [deploy](docs/sdks/mariadb/README.md#deploy)
* [changeStatus](docs/sdks/mariadb/README.md#changestatus)
* [remove](docs/sdks/mariadb/README.md#remove)
* [saveEnvironment](docs/sdks/mariadb/README.md#saveenvironment)
* [reload](docs/sdks/mariadb/README.md#reload)
* [update](docs/sdks/mariadb/README.md#update)

### [mongo](docs/sdks/mongo/README.md)

* [create](docs/sdks/mongo/README.md#create)
* [get](docs/sdks/mongo/README.md#get)
* [start](docs/sdks/mongo/README.md#start)
* [stop](docs/sdks/mongo/README.md#stop)
* [saveExternalPort](docs/sdks/mongo/README.md#saveexternalport)
* [deploy](docs/sdks/mongo/README.md#deploy)
* [changeStatus](docs/sdks/mongo/README.md#changestatus)
* [reload](docs/sdks/mongo/README.md#reload)
* [remove](docs/sdks/mongo/README.md#remove)
* [saveEnvironment](docs/sdks/mongo/README.md#saveenvironment)
* [update](docs/sdks/mongo/README.md#update)

### [mounts](docs/sdks/mounts/README.md)

* [create](docs/sdks/mounts/README.md#create)
* [remove](docs/sdks/mounts/README.md#remove)
* [get](docs/sdks/mounts/README.md#get)
* [update](docs/sdks/mounts/README.md#update)

### [mysql](docs/sdks/mysql/README.md)

* [create](docs/sdks/mysql/README.md#create)
* [get](docs/sdks/mysql/README.md#get)
* [start](docs/sdks/mysql/README.md#start)
* [stop](docs/sdks/mysql/README.md#stop)
* [saveExternalPort](docs/sdks/mysql/README.md#saveexternalport)
* [deploy](docs/sdks/mysql/README.md#deploy)
* [changeStatus](docs/sdks/mysql/README.md#changestatus)
* [reload](docs/sdks/mysql/README.md#reload)
* [remove](docs/sdks/mysql/README.md#remove)
* [saveEnvironment](docs/sdks/mysql/README.md#saveenvironment)
* [update](docs/sdks/mysql/README.md#update)

### [notification](docs/sdks/notification/README.md)

* [createSlack](docs/sdks/notification/README.md#createslack)
* [updateSlack](docs/sdks/notification/README.md#updateslack)
* [testSlackConnection](docs/sdks/notification/README.md#testslackconnection)
* [createTelegram](docs/sdks/notification/README.md#createtelegram)
* [updateTelegram](docs/sdks/notification/README.md#updatetelegram)
* [testTelegramConnection](docs/sdks/notification/README.md#testtelegramconnection)
* [createDiscord](docs/sdks/notification/README.md#creatediscord)
* [updateDiscord](docs/sdks/notification/README.md#updatediscord)
* [testDiscordConnection](docs/sdks/notification/README.md#testdiscordconnection)
* [createEmail](docs/sdks/notification/README.md#createemail)
* [updateEmail](docs/sdks/notification/README.md#updateemail)
* [testEmailConnection](docs/sdks/notification/README.md#testemailconnection)
* [remove](docs/sdks/notification/README.md#remove)
* [getAll](docs/sdks/notification/README.md#getall)

### [notifications](docs/sdks/notifications/README.md)

* [get](docs/sdks/notifications/README.md#get)

### [port](docs/sdks/port/README.md)

* [create](docs/sdks/port/README.md#create)
* [get](docs/sdks/port/README.md#get)
* [delete](docs/sdks/port/README.md#delete)
* [update](docs/sdks/port/README.md#update)

### [postgres](docs/sdks/postgres/README.md)

* [create](docs/sdks/postgres/README.md#create)
* [get](docs/sdks/postgres/README.md#get)
* [start](docs/sdks/postgres/README.md#start)
* [stop](docs/sdks/postgres/README.md#stop)
* [saveExternalPort](docs/sdks/postgres/README.md#saveexternalport)
* [deploy](docs/sdks/postgres/README.md#deploy)
* [changeStatus](docs/sdks/postgres/README.md#changestatus)
* [remove](docs/sdks/postgres/README.md#remove)
* [saveEnvironment](docs/sdks/postgres/README.md#saveenvironment)
* [reload](docs/sdks/postgres/README.md#reload)
* [update](docs/sdks/postgres/README.md#update)

### [project](docs/sdks/project/README.md)

* [create](docs/sdks/project/README.md#create)
* [get](docs/sdks/project/README.md#get)
* [all](docs/sdks/project/README.md#all)
* [remove](docs/sdks/project/README.md#remove)
* [update](docs/sdks/project/README.md#update)

### [redirects](docs/sdks/redirects/README.md)

* [create](docs/sdks/redirects/README.md#create)
* [getOne](docs/sdks/redirects/README.md#getone)
* [delete](docs/sdks/redirects/README.md#delete)
* [update](docs/sdks/redirects/README.md#update)

### [redis](docs/sdks/redis/README.md)

* [create](docs/sdks/redis/README.md#create)
* [get](docs/sdks/redis/README.md#get)
* [start](docs/sdks/redis/README.md#start)
* [reload](docs/sdks/redis/README.md#reload)
* [stop](docs/sdks/redis/README.md#stop)
* [saveExternalPort](docs/sdks/redis/README.md#saveexternalport)
* [deploy](docs/sdks/redis/README.md#deploy)
* [changeStatus](docs/sdks/redis/README.md#changestatus)
* [remove](docs/sdks/redis/README.md#remove)
* [saveEnvironment](docs/sdks/redis/README.md#saveenvironment)
* [update](docs/sdks/redis/README.md#update)

### [registry](docs/sdks/registry/README.md)

* [create](docs/sdks/registry/README.md#create)
* [remove](docs/sdks/registry/README.md#remove)
* [update](docs/sdks/registry/README.md#update)
* [getAll](docs/sdks/registry/README.md#getall)
* [get](docs/sdks/registry/README.md#get)
* [testRegistry](docs/sdks/registry/README.md#testregistry)

### [security](docs/sdks/security/README.md)

* [create](docs/sdks/security/README.md#create)
* [get](docs/sdks/security/README.md#get)
* [delete](docs/sdks/security/README.md#delete)
* [update](docs/sdks/security/README.md#update)

### [server](docs/sdks/server/README.md)

* [create](docs/sdks/server/README.md#create)
* [all](docs/sdks/server/README.md#all)
* [withSSHKey](docs/sdks/server/README.md#withsshkey)
* [setup](docs/sdks/server/README.md#setup)
* [remove](docs/sdks/server/README.md#remove)
* [update](docs/sdks/server/README.md#update)

### [servers](docs/sdks/servers/README.md)

* [get](docs/sdks/servers/README.md#get)

### [settings](docs/sdks/settings/README.md)

* [reloadServer](docs/sdks/settings/README.md#reloadserver)
* [reloadTraefik](docs/sdks/settings/README.md#reloadtraefik)
* [toggleDashboard](docs/sdks/settings/README.md#toggledashboard)
* [cleanUnusedImages](docs/sdks/settings/README.md#cleanunusedimages)
* [cleanUnusedVolumes](docs/sdks/settings/README.md#cleanunusedvolumes)
* [cleanStoppedContainers](docs/sdks/settings/README.md#cleanstoppedcontainers)
* [cleanDockerBuilder](docs/sdks/settings/README.md#cleandockerbuilder)
* [cleanDockerPrune](docs/sdks/settings/README.md#cleandockerprune)
* [cleanAll](docs/sdks/settings/README.md#cleanall)
* [cleanMonitoring](docs/sdks/settings/README.md#cleanmonitoring)
* [saveSshPrivateKey](docs/sdks/settings/README.md#savesshprivatekey)
* [assignDomainServer](docs/sdks/settings/README.md#assigndomainserver)
* [cleanSshPrivateKey](docs/sdks/settings/README.md#cleansshprivatekey)
* [updateDockerCleanup](docs/sdks/settings/README.md#updatedockercleanup)
* [readTraefikConfig](docs/sdks/settings/README.md#readtraefikconfig)
* [updateTraefikConfig](docs/sdks/settings/README.md#updatetraefikconfig)
* [readWebServerTraefikConfig](docs/sdks/settings/README.md#readwebservertraefikconfig)
* [updateWebServerTraefikConfig](docs/sdks/settings/README.md#updatewebservertraefikconfig)
* [readMiddlewareTraefikConfig](docs/sdks/settings/README.md#readmiddlewaretraefikconfig)
* [updateMiddlewareTraefikConfig](docs/sdks/settings/README.md#updatemiddlewaretraefikconfig)
* [checkAndUpdateImage](docs/sdks/settings/README.md#checkandupdateimage)
* [updateServer](docs/sdks/settings/README.md#updateserver)
* [getDokployVersion](docs/sdks/settings/README.md#getdokployversion)
* [readDirectories](docs/sdks/settings/README.md#readdirectories)
* [updateTraefikFile](docs/sdks/settings/README.md#updatetraefikfile)
* [readTraefikFile](docs/sdks/settings/README.md#readtraefikfile)
* [getIp](docs/sdks/settings/README.md#getip)
* [getOpenApiDocument](docs/sdks/settings/README.md#getopenapidocument)
* [readTraefikEnv](docs/sdks/settings/README.md#readtraefikenv)
* [writeTraefikEnv](docs/sdks/settings/README.md#writetraefikenv)
* [haveTraefikDashboardPortEnabled](docs/sdks/settings/README.md#havetraefikdashboardportenabled)
* [readStats](docs/sdks/settings/README.md#readstats)
* [getLogRotateStatus](docs/sdks/settings/README.md#getlogrotatestatus)
* [toggleLogRotate](docs/sdks/settings/README.md#togglelogrotate)
* [haveActivateRequests](docs/sdks/settings/README.md#haveactivaterequests)
* [toggleRequests](docs/sdks/settings/README.md#togglerequests)
* [isCloud](docs/sdks/settings/README.md#iscloud)
* [health](docs/sdks/settings/README.md#health)

### [sshKey](docs/sdks/sshkey/README.md)

* [remove](docs/sdks/sshkey/README.md#remove)
* [get](docs/sdks/sshkey/README.md#get)
* [generate](docs/sdks/sshkey/README.md#generate)
* [update](docs/sdks/sshkey/README.md#update)

### [sshKeys](docs/sdks/sshkeys/README.md)

* [create](docs/sdks/sshkeys/README.md#create)
* [all](docs/sdks/sshkeys/README.md#all)

### [stripe](docs/sdks/stripe/README.md)

* [getProducts](docs/sdks/stripe/README.md#getproducts)
* [createCheckoutSession](docs/sdks/stripe/README.md#createcheckoutsession)
* [createCustomerPortalSession](docs/sdks/stripe/README.md#createcustomerportalsession)
* [canCreateMoreServers](docs/sdks/stripe/README.md#cancreatemoreservers)

### [user](docs/sdks/user/README.md)

* [getAll](docs/sdks/user/README.md#getall)
* [byAuthId](docs/sdks/user/README.md#byauthid)
* [byUserId](docs/sdks/user/README.md#byuserid)

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`adminAssignPermissions`](docs/sdks/admin/README.md#assignpermissions)
- [`adminCreateUserInvitation`](docs/sdks/admin/README.md#createuserinvitation)
- [`adminGetOne`](docs/sdks/admin/README.md#getone)
- [`adminGetUserByToken`](docs/sdks/admin/README.md#getuserbytoken)
- [`adminRemoveUser`](docs/sdks/admin/README.md#removeuser)
- [`applicationCleanQueues`](docs/sdks/application/README.md#cleanqueues)
- [`applicationCreate`](docs/sdks/application/README.md#create)
- [`applicationDelete`](docs/sdks/application/README.md#delete)
- [`applicationDeploy`](docs/sdks/application/README.md#deploy)
- [`applicationGetOne`](docs/sdks/application/README.md#getone)
- [`applicationMarkRunning`](docs/sdks/application/README.md#markrunning)
- [`applicationReadAppMonitoring`](docs/sdks/application/README.md#readappmonitoring)
- [`applicationReadTraefikConfig`](docs/sdks/application/README.md#readtraefikconfig)
- [`applicationRedeploy`](docs/sdks/application/README.md#redeploy)
- [`applicationRefreshToken`](docs/sdks/application/README.md#refreshtoken)
- [`applicationReload`](docs/sdks/application/README.md#reload)
- [`applicationSaveBitbucketProvider`](docs/sdks/application/README.md#savebitbucketprovider)
- [`applicationSaveBuildType`](docs/sdks/application/README.md#savebuildtype)
- [`applicationSaveDockerProvider`](docs/sdks/application/README.md#savedockerprovider)
- [`applicationSaveEnvironment`](docs/sdks/application/README.md#saveenvironment)
- [`applicationSaveGithubProvider`](docs/sdks/application/README.md#savegithubprovider)
- [`applicationSaveGitlabProvider`](docs/sdks/application/README.md#savegitlabprovider)
- [`applicationSaveGitProdiver`](docs/sdks/application/README.md#savegitprodiver)
- [`applicationStart`](docs/sdks/application/README.md#start)
- [`applicationStop`](docs/sdks/application/README.md#stop)
- [`applicationUpdate`](docs/sdks/application/README.md#update)
- [`applicationUpdateTraefikConfig`](docs/sdks/application/README.md#updatetraefikconfig)
- [`authConfirmEmail`](docs/sdks/auth/README.md#confirmemail)
- [`authCreateAdmin`](docs/sdks/auth/README.md#createadmin)
- [`authCreateUser`](docs/sdks/auth/README.md#createuser)
- [`authDisable2FA`](docs/sdks/auth/README.md#disable2fa)
- [`authGenerate2FASecret`](docs/sdks/auth/README.md#generate2fasecret)
- [`authGenerateToken`](docs/sdks/auth/README.md#generatetoken)
- [`authGet`](docs/sdks/auth/README.md#get)
- [`authGetOne`](docs/sdks/auth/README.md#getone)
- [`authLogin`](docs/sdks/auth/README.md#login)
- [`authLogout`](docs/sdks/auth/README.md#logout)
- [`authResetPassword`](docs/sdks/auth/README.md#resetpassword)
- [`authSendResetPasswordEmail`](docs/sdks/auth/README.md#sendresetpasswordemail)
- [`authUpdate`](docs/sdks/auth/README.md#update)
- [`authVerify2faSetup`](docs/sdks/auth/README.md#verify2fasetup)
- [`authVerifyLogin2FA`](docs/sdks/auth/README.md#verifylogin2fa)
- [`backupCreate`](docs/sdks/backup/README.md#create)
- [`backupGet`](docs/sdks/backup/README.md#get)
- [`backupManualBackupMariadb`](docs/sdks/backup/README.md#manualbackupmariadb)
- [`backupManualBackupMongo`](docs/sdks/backup/README.md#manualbackupmongo)
- [`backupManualBackupMysql`](docs/sdks/backup/README.md#manualbackupmysql)
- [`backupManualBackupPostgres`](docs/sdks/backup/README.md#manualbackuppostgres)
- [`backupRemove`](docs/sdks/backup/README.md#remove)
- [`backupUpdate`](docs/sdks/backup/README.md#update)
- [`bitbucketCreate`](docs/sdks/bitbucket/README.md#create)
- [`bitbucketGet`](docs/sdks/bitbucket/README.md#get)
- [`bitbucketGetBranches`](docs/sdks/bitbucket/README.md#getbranches)
- [`bitbucketGetRepositories`](docs/sdks/bitbucket/README.md#getrepositories)
- [`bitbucketProviders`](docs/sdks/bitbucket/README.md#providers)
- [`bitbucketTestConnection`](docs/sdks/bitbucket/README.md#testconnection)
- [`bitbucketUpdate`](docs/sdks/bitbucket/README.md#update)
- [`certificatesAll`](docs/sdks/certificates/README.md#all)
- [`certificatesCreate`](docs/sdks/certificates/README.md#create)
- [`certificatesGet`](docs/sdks/certificates/README.md#get)
- [`certificatesRemove`](docs/sdks/certificates/README.md#remove)
- [`clusterAddManager`](docs/sdks/cluster/README.md#addmanager)
- [`clusterAddWorker`](docs/sdks/cluster/README.md#addworker)
- [`clusterGetNodes`](docs/sdks/cluster/README.md#getnodes)
- [`clusterRemoveWorker`](docs/sdks/cluster/README.md#removeworker)
- [`composeCleanQueues`](docs/sdks/compose/README.md#cleanqueues)
- [`composeCreate`](docs/sdks/compose/README.md#create)
- [`composeDelete`](docs/sdks/compose/README.md#delete)
- [`composeDeploy`](docs/sdks/compose/README.md#deploy)
- [`composeDeployTemplate`](docs/sdks/compose/README.md#deploytemplate)
- [`composeFetchSourceType`](docs/sdks/compose/README.md#fetchsourcetype)
- [`composeGetConverted`](docs/sdks/compose/README.md#getconverted)
- [`composeGetDefaultCommand`](docs/sdks/compose/README.md#getdefaultcommand)
- [`composeGetOne`](docs/sdks/compose/README.md#getone)
- [`composeGetTags`](docs/sdks/compose/README.md#gettags)
- [`composeGetTemplates`](docs/sdks/compose/README.md#gettemplates)
- [`composeRandomizeCompose`](docs/sdks/compose/README.md#randomizecompose)
- [`composeRedeploy`](docs/sdks/compose/README.md#redeploy)
- [`composeRefreshToken`](docs/sdks/compose/README.md#refreshtoken)
- [`composeStop`](docs/sdks/compose/README.md#stop)
- [`composeUpdate`](docs/sdks/compose/README.md#update)
- [`deploymentAllByCompose`](docs/sdks/deployment/README.md#allbycompose)
- [`deploymentAllByServer`](docs/sdks/deployment/README.md#allbyserver)
- [`deploymentGet`](docs/sdks/deployment/README.md#get)
- [`destinationCreate`](docs/sdks/destination/README.md#create)
- [`destinationGet`](docs/sdks/destination/README.md#get)
- [`destinationGetOne`](docs/sdks/destination/README.md#getone)
- [`destinationRemove`](docs/sdks/destination/README.md#remove)
- [`destinationTestConnection`](docs/sdks/destination/README.md#testconnection)
- [`destinationUpdate`](docs/sdks/destination/README.md#update)
- [`dockerGetConfig`](docs/sdks/docker/README.md#getconfig)
- [`dockerGetContainers`](docs/sdks/docker/README.md#getcontainers)
- [`dockerGetContainersByAppLabel`](docs/sdks/docker/README.md#getcontainersbyapplabel)
- [`dockerGetContainersByAppNameMatch`](docs/sdks/docker/README.md#getcontainersbyappnamematch)
- [`dockerRestartContainer`](docs/sdks/docker/README.md#restartcontainer)
- [`domainByApplicationId`](docs/sdks/domain/README.md#byapplicationid)
- [`domainByComposeId`](docs/sdks/domain/README.md#bycomposeid)
- [`domainCreate`](docs/sdks/domain/README.md#create)
- [`domainDelete`](docs/sdks/domain/README.md#delete)
- [`domainGenerateDomain`](docs/sdks/domain/README.md#generatedomain)
- [`domainGet`](docs/sdks/domain/README.md#get)
- [`domainUpdate`](docs/sdks/domain/README.md#update)
- [`githubGetBranches`](docs/sdks/github/README.md#getbranches)
- [`githubGetProviders`](docs/sdks/github/README.md#getproviders)
- [`githubGetRepositories`](docs/sdks/github/README.md#getrepositories)
- [`githubOne`](docs/sdks/github/README.md#one)
- [`githubTestConnection`](docs/sdks/github/README.md#testconnection)
- [`githubUpdate`](docs/sdks/github/README.md#update)
- [`gitlabCreate`](docs/sdks/gitlab/README.md#create)
- [`gitlabGetGitlabBranches`](docs/sdks/gitlab/README.md#getgitlabbranches)
- [`gitlabGetGitlabRepositories`](docs/sdks/gitlab/README.md#getgitlabrepositories)
- [`gitlabOne`](docs/sdks/gitlab/README.md#one)
- [`gitlabProviders`](docs/sdks/gitlab/README.md#providers)
- [`gitlabTestConnection`](docs/sdks/gitlab/README.md#testconnection)
- [`gitlabUpdate`](docs/sdks/gitlab/README.md#update)
- [`gitProviderGetAll`](docs/sdks/gitprovider/README.md#getall)
- [`gitProviderRemove`](docs/sdks/gitprovider/README.md#remove)
- [`mariadbChangeStatus`](docs/sdks/mariadb/README.md#changestatus)
- [`mariadbCreate`](docs/sdks/mariadb/README.md#create)
- [`mariadbDeploy`](docs/sdks/mariadb/README.md#deploy)
- [`mariadbGet`](docs/sdks/mariadb/README.md#get)
- [`mariadbReload`](docs/sdks/mariadb/README.md#reload)
- [`mariadbRemove`](docs/sdks/mariadb/README.md#remove)
- [`mariadbSaveEnvironment`](docs/sdks/mariadb/README.md#saveenvironment)
- [`mariadbSaveExternalPort`](docs/sdks/mariadb/README.md#saveexternalport)
- [`mariadbStart`](docs/sdks/mariadb/README.md#start)
- [`mariadbStop`](docs/sdks/mariadb/README.md#stop)
- [`mariadbUpdate`](docs/sdks/mariadb/README.md#update)
- [`mongoChangeStatus`](docs/sdks/mongo/README.md#changestatus)
- [`mongoCreate`](docs/sdks/mongo/README.md#create)
- [`mongoDeploy`](docs/sdks/mongo/README.md#deploy)
- [`mongoGet`](docs/sdks/mongo/README.md#get)
- [`mongoReload`](docs/sdks/mongo/README.md#reload)
- [`mongoRemove`](docs/sdks/mongo/README.md#remove)
- [`mongoSaveEnvironment`](docs/sdks/mongo/README.md#saveenvironment)
- [`mongoSaveExternalPort`](docs/sdks/mongo/README.md#saveexternalport)
- [`mongoStart`](docs/sdks/mongo/README.md#start)
- [`mongoStop`](docs/sdks/mongo/README.md#stop)
- [`mongoUpdate`](docs/sdks/mongo/README.md#update)
- [`mountsCreate`](docs/sdks/mounts/README.md#create)
- [`mountsGet`](docs/sdks/mounts/README.md#get)
- [`mountsRemove`](docs/sdks/mounts/README.md#remove)
- [`mountsUpdate`](docs/sdks/mounts/README.md#update)
- [`mysqlChangeStatus`](docs/sdks/mysql/README.md#changestatus)
- [`mysqlCreate`](docs/sdks/mysql/README.md#create)
- [`mysqlDeploy`](docs/sdks/mysql/README.md#deploy)
- [`mysqlGet`](docs/sdks/mysql/README.md#get)
- [`mysqlReload`](docs/sdks/mysql/README.md#reload)
- [`mysqlRemove`](docs/sdks/mysql/README.md#remove)
- [`mysqlSaveEnvironment`](docs/sdks/mysql/README.md#saveenvironment)
- [`mysqlSaveExternalPort`](docs/sdks/mysql/README.md#saveexternalport)
- [`mysqlStart`](docs/sdks/mysql/README.md#start)
- [`mysqlStop`](docs/sdks/mysql/README.md#stop)
- [`mysqlUpdate`](docs/sdks/mysql/README.md#update)
- [`notificationCreateDiscord`](docs/sdks/notification/README.md#creatediscord)
- [`notificationCreateEmail`](docs/sdks/notification/README.md#createemail)
- [`notificationCreateSlack`](docs/sdks/notification/README.md#createslack)
- [`notificationCreateTelegram`](docs/sdks/notification/README.md#createtelegram)
- [`notificationGetAll`](docs/sdks/notification/README.md#getall)
- [`notificationRemove`](docs/sdks/notification/README.md#remove)
- [`notificationsGet`](docs/sdks/notifications/README.md#get)
- [`notificationTestDiscordConnection`](docs/sdks/notification/README.md#testdiscordconnection)
- [`notificationTestEmailConnection`](docs/sdks/notification/README.md#testemailconnection)
- [`notificationTestSlackConnection`](docs/sdks/notification/README.md#testslackconnection)
- [`notificationTestTelegramConnection`](docs/sdks/notification/README.md#testtelegramconnection)
- [`notificationUpdateDiscord`](docs/sdks/notification/README.md#updatediscord)
- [`notificationUpdateEmail`](docs/sdks/notification/README.md#updateemail)
- [`notificationUpdateSlack`](docs/sdks/notification/README.md#updateslack)
- [`notificationUpdateTelegram`](docs/sdks/notification/README.md#updatetelegram)
- [`portCreate`](docs/sdks/port/README.md#create)
- [`portDelete`](docs/sdks/port/README.md#delete)
- [`portGet`](docs/sdks/port/README.md#get)
- [`portUpdate`](docs/sdks/port/README.md#update)
- [`postgresChangeStatus`](docs/sdks/postgres/README.md#changestatus)
- [`postgresCreate`](docs/sdks/postgres/README.md#create)
- [`postgresDeploy`](docs/sdks/postgres/README.md#deploy)
- [`postgresGet`](docs/sdks/postgres/README.md#get)
- [`postgresReload`](docs/sdks/postgres/README.md#reload)
- [`postgresRemove`](docs/sdks/postgres/README.md#remove)
- [`postgresSaveEnvironment`](docs/sdks/postgres/README.md#saveenvironment)
- [`postgresSaveExternalPort`](docs/sdks/postgres/README.md#saveexternalport)
- [`postgresStart`](docs/sdks/postgres/README.md#start)
- [`postgresStop`](docs/sdks/postgres/README.md#stop)
- [`postgresUpdate`](docs/sdks/postgres/README.md#update)
- [`projectAll`](docs/sdks/project/README.md#all)
- [`projectCreate`](docs/sdks/project/README.md#create)
- [`projectGet`](docs/sdks/project/README.md#get)
- [`projectRemove`](docs/sdks/project/README.md#remove)
- [`projectUpdate`](docs/sdks/project/README.md#update)
- [`redirectsCreate`](docs/sdks/redirects/README.md#create)
- [`redirectsDelete`](docs/sdks/redirects/README.md#delete)
- [`redirectsGetOne`](docs/sdks/redirects/README.md#getone)
- [`redirectsUpdate`](docs/sdks/redirects/README.md#update)
- [`redisChangeStatus`](docs/sdks/redis/README.md#changestatus)
- [`redisCreate`](docs/sdks/redis/README.md#create)
- [`redisDeploy`](docs/sdks/redis/README.md#deploy)
- [`redisGet`](docs/sdks/redis/README.md#get)
- [`redisReload`](docs/sdks/redis/README.md#reload)
- [`redisRemove`](docs/sdks/redis/README.md#remove)
- [`redisSaveEnvironment`](docs/sdks/redis/README.md#saveenvironment)
- [`redisSaveExternalPort`](docs/sdks/redis/README.md#saveexternalport)
- [`redisStart`](docs/sdks/redis/README.md#start)
- [`redisStop`](docs/sdks/redis/README.md#stop)
- [`redisUpdate`](docs/sdks/redis/README.md#update)
- [`registryCreate`](docs/sdks/registry/README.md#create)
- [`registryGet`](docs/sdks/registry/README.md#get)
- [`registryGetAll`](docs/sdks/registry/README.md#getall)
- [`registryRemove`](docs/sdks/registry/README.md#remove)
- [`registryTestRegistry`](docs/sdks/registry/README.md#testregistry)
- [`registryUpdate`](docs/sdks/registry/README.md#update)
- [`securityCreate`](docs/sdks/security/README.md#create)
- [`securityDelete`](docs/sdks/security/README.md#delete)
- [`securityGet`](docs/sdks/security/README.md#get)
- [`securityUpdate`](docs/sdks/security/README.md#update)
- [`serverAll`](docs/sdks/server/README.md#all)
- [`serverCreate`](docs/sdks/server/README.md#create)
- [`serverRemove`](docs/sdks/server/README.md#remove)
- [`serverSetup`](docs/sdks/server/README.md#setup)
- [`serversGet`](docs/sdks/servers/README.md#get)
- [`serverUpdate`](docs/sdks/server/README.md#update)
- [`serverWithSSHKey`](docs/sdks/server/README.md#withsshkey)
- [`settingsAssignDomainServer`](docs/sdks/settings/README.md#assigndomainserver)
- [`settingsCheckAndUpdateImage`](docs/sdks/settings/README.md#checkandupdateimage)
- [`settingsCleanAll`](docs/sdks/settings/README.md#cleanall)
- [`settingsCleanDockerBuilder`](docs/sdks/settings/README.md#cleandockerbuilder)
- [`settingsCleanDockerPrune`](docs/sdks/settings/README.md#cleandockerprune)
- [`settingsCleanMonitoring`](docs/sdks/settings/README.md#cleanmonitoring)
- [`settingsCleanSshPrivateKey`](docs/sdks/settings/README.md#cleansshprivatekey)
- [`settingsCleanStoppedContainers`](docs/sdks/settings/README.md#cleanstoppedcontainers)
- [`settingsCleanUnusedImages`](docs/sdks/settings/README.md#cleanunusedimages)
- [`settingsCleanUnusedVolumes`](docs/sdks/settings/README.md#cleanunusedvolumes)
- [`settingsGetDokployVersion`](docs/sdks/settings/README.md#getdokployversion)
- [`settingsGetIp`](docs/sdks/settings/README.md#getip)
- [`settingsGetLogRotateStatus`](docs/sdks/settings/README.md#getlogrotatestatus)
- [`settingsGetOpenApiDocument`](docs/sdks/settings/README.md#getopenapidocument)
- [`settingsHaveActivateRequests`](docs/sdks/settings/README.md#haveactivaterequests)
- [`settingsHaveTraefikDashboardPortEnabled`](docs/sdks/settings/README.md#havetraefikdashboardportenabled)
- [`settingsHealth`](docs/sdks/settings/README.md#health)
- [`settingsIsCloud`](docs/sdks/settings/README.md#iscloud)
- [`settingsReadDirectories`](docs/sdks/settings/README.md#readdirectories)
- [`settingsReadMiddlewareTraefikConfig`](docs/sdks/settings/README.md#readmiddlewaretraefikconfig)
- [`settingsReadStats`](docs/sdks/settings/README.md#readstats)
- [`settingsReadTraefikConfig`](docs/sdks/settings/README.md#readtraefikconfig)
- [`settingsReadTraefikEnv`](docs/sdks/settings/README.md#readtraefikenv)
- [`settingsReadTraefikFile`](docs/sdks/settings/README.md#readtraefikfile)
- [`settingsReadWebServerTraefikConfig`](docs/sdks/settings/README.md#readwebservertraefikconfig)
- [`settingsReloadServer`](docs/sdks/settings/README.md#reloadserver)
- [`settingsReloadTraefik`](docs/sdks/settings/README.md#reloadtraefik)
- [`settingsSaveSshPrivateKey`](docs/sdks/settings/README.md#savesshprivatekey)
- [`settingsToggleDashboard`](docs/sdks/settings/README.md#toggledashboard)
- [`settingsToggleLogRotate`](docs/sdks/settings/README.md#togglelogrotate)
- [`settingsToggleRequests`](docs/sdks/settings/README.md#togglerequests)
- [`settingsUpdateDockerCleanup`](docs/sdks/settings/README.md#updatedockercleanup)
- [`settingsUpdateMiddlewareTraefikConfig`](docs/sdks/settings/README.md#updatemiddlewaretraefikconfig)
- [`settingsUpdateServer`](docs/sdks/settings/README.md#updateserver)
- [`settingsUpdateTraefikConfig`](docs/sdks/settings/README.md#updatetraefikconfig)
- [`settingsUpdateTraefikFile`](docs/sdks/settings/README.md#updatetraefikfile)
- [`settingsUpdateWebServerTraefikConfig`](docs/sdks/settings/README.md#updatewebservertraefikconfig)
- [`settingsWriteTraefikEnv`](docs/sdks/settings/README.md#writetraefikenv)
- [`sshKeyGenerate`](docs/sdks/sshkey/README.md#generate)
- [`sshKeyGet`](docs/sdks/sshkey/README.md#get)
- [`sshKeyRemove`](docs/sdks/sshkey/README.md#remove)
- [`sshKeysAll`](docs/sdks/sshkeys/README.md#all)
- [`sshKeysCreate`](docs/sdks/sshkeys/README.md#create)
- [`sshKeyUpdate`](docs/sdks/sshkey/README.md#update)
- [`stripeCanCreateMoreServers`](docs/sdks/stripe/README.md#cancreatemoreservers)
- [`stripeCreateCheckoutSession`](docs/sdks/stripe/README.md#createcheckoutsession)
- [`stripeCreateCustomerPortalSession`](docs/sdks/stripe/README.md#createcustomerportalsession)
- [`stripeGetProducts`](docs/sdks/stripe/README.md#getproducts)
- [`userByAuthId`](docs/sdks/user/README.md#byauthid)
- [`userByUserId`](docs/sdks/user/README.md#byuserid)
- [`userGetAll`](docs/sdks/user/README.md#getall)

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { Dokploy } from "dokploy";

const dokploy = new Dokploy({
  authorization: process.env["DOKPLOY_AUTHORIZATION"] ?? "",
});

async function run() {
  const result = await dokploy.admin.getOne({
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Dokploy } from "dokploy";

const dokploy = new Dokploy({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
  authorization: process.env["DOKPLOY_AUTHORIZATION"] ?? "",
});

async function run() {
  const result = await dokploy.admin.getOne();

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`DokployError`](./src/models/errors/dokployerror.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                            |
| ------------------- | ---------- | ------------------------------------------------------ |
| `error.message`     | `string`   | Error message                                          |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                     |
| `error.headers`     | `Headers`  | HTTP response headers                                  |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned. |
| `error.rawResponse` | `Response` | Raw HTTP response                                      |

### Example
```typescript
import { Dokploy } from "dokploy";
import * as errors from "dokploy/models/errors";

const dokploy = new Dokploy({
  authorization: process.env["DOKPLOY_AUTHORIZATION"] ?? "",
});

async function run() {
  try {
    const result = await dokploy.admin.getOne();

    console.log(result);
  } catch (error) {
    if (error instanceof errors.DokployError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);
    }
  }
}

run();

```

### Error Classes
**Primary error:**
* [`DokployError`](./src/models/errors/dokployerror.ts): The base class for HTTP error responses.

<details><summary>Less common errors (6)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`DokployError`](./src/models/errors/dokployerror.ts)**:
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Dokploy } from "dokploy";

const dokploy = new Dokploy({
  serverURL: "http://your-dokploy-instance.com/api",
  authorization: process.env["DOKPLOY_AUTHORIZATION"] ?? "",
});

async function run() {
  const result = await dokploy.admin.getOne();

  console.log(result);
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to use the `"beforeRequest"` hook to to add a
custom header and a timeout to requests and how to use the `"requestError"` hook
to log errors:

```typescript
import { Dokploy } from "dokploy";
import { HTTPClient } from "dokploy/lib/http";

const httpClient = new HTTPClient({
  // fetcher takes a function that has the same signature as native `fetch`.
  fetcher: (request) => {
    return fetch(request);
  }
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new Dokploy({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Dokploy } from "dokploy";

const sdk = new Dokploy({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `DOKPLOY_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=dokploy&utm_campaign=typescript)
