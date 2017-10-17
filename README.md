# Witness Scheduler Electron build
_requirements:-_
- Node
- Yarn

## Clone repository
```
C:\Users\mike\projects
λ git clone https://github.com/mikeq/electronbuild.git
```

## Install Electron dependencies
cd into the folder where you cloned the repository.

Run yarn to install Electron and Electron Builder dependencies
```
C:\Users\mike\projects\electronbuild
λ yarn
```

## Configuration
Edit `config.js` and point the url to a valid instance of the scheduler client application

The config file should now look like this

```
const config = {
  url: 'https://_server_/client/'
}

module.exports = config;
```

### Running in Electron
```
C:\Users\mike\projects\electronbuild
λ yarn start
```
_an Electron application window will launch with the URL specified in the config.js file._

_Use this first to test the correct URL has been set in the config before carrying out the build_

### Building Setup executable

```
C:\Users\mike\projects\electronbuild
λ yarn dist
```

A Windows Setup executable file will be created in the `dist/` folder once the process completes
