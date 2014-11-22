
## CLI
### Overview

The MEAN CLI is a simple Command Line Interface for installing and managing MEAN applications. As a core module of the mean.io project, it provides a number of useful tools to make interaction with your MEAN application easier, with features such as: scaffolding, module creation and admin, status checks, and user management.
```bash
  $ mean
  $ mean --help
  $ mean help
```
  <code>mean help</code> can also be used in conjunction with any command to get more information about that particular functionality. For example, try <code>mean help init</code> to see the options for init
```bash
  $ mean help [command]
```
### Users

 <p>Information can be display for a specific customer via <code>mean user email</code>. Email is required. User roles can be assigned or removed with the <code>--addRole (or -a)</code> and <code>--removeRole (or -r)</code> options, respectively.</p>
  <p>For example, the <i>admin</i> role is required to edit tokens.</p>

```bash
  $ mean user <email> 
  $ mean user <email> --addRole <role>; 
  $ mean user <email> --removeRole <role>; 
```

### packages
#### Management
 <p class="alert alert-warning">All of the remaining of the commands must be run from the root folder of your MEAN application.</p>
  <p>Contributed MEAN packages can be installed or uninstalled via the CLI. Also, currently installed modules can be viewed with the <code>list</code> command.</p>

```bash
  $ mean list
  $ mean install <module>
  $ mean uninstall <module>
```

  <p class="alert alert-info">Mean packages installed via the installer are found in <i>/node_modules</i></p>
#### Search
To find new packages run the *mean search* command
```bash
  $ mean search [packagename]
```
mean search will return all of the available packages, mean search packagename will filter the search results.

#### Scaffolding
To create a new MEAN app, run <code>mean init</code>. Name for the application is optional. If no name is provided, "mean" is used. The MEAN project will be cloned from GitHub into a directory of the application name.
```bash
  $ mean init [name]
  $ cd [name] && npm install
```
  <p class="alert alert-info">Note: <a href="http://git-scm.com/downloads">git</a> must be installed for this command to work properly.</p>

### Misc
<h4>Status</h4>
<p>Check the database connection for a particular environment (e.g. development (default), test, production) and make sure that the meanio command line version is up to date.</p>
```bash
  $ mean status
```
<h4>Docs</h4>
<p>A simple shortcut to open the mean documentation in your default browser.</p>
```bash
  $ mean docs
```
