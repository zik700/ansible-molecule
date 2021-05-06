### First lab with molecule
in this lab i wll try to test nginx webserver with molecule. 

```bash
printf "Stay awesome! :)"
```

## Requirements
```bash
pip3 install molecule
pip3 install molecule-docker
```
The second package solve problem - "Error: Invalid value for "--driver-name" / "-d": invalid choice: docker. (choose from delegated)"

## Initialize role

```bash
molecule init role nginx.webserver -d docker
```

This gave me a whole ansible directory structure

## First test

```bash
molecule test
```

But nothing worked :(

## Verify the documentation
It's time to verify documentation, after that i saw my fault

For the first time we need to create our enviroment with containers
```bash
molecule create
```
For listing all instances defined in molecule.yml in platforms section
```bash
molecule list
```
To execute all tasks 
```bash
molecule converage
```

To execute test scenario
```bash
molecule test
```