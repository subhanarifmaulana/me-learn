# Project Title

**Bhinneka Life** Project  
Bhinneka dot com Life Assurance Company

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Things you need to install the software and how to install them, please refer the link below:

* [NodeJS](https://github.com/creationix/nvm) - using NVM (Node Version Manager),
* [Docker-CE](https://docs.docker.com/install/linux/docker-ce/ubuntu/) - Community Edition,
* [Docker-CE CLI](https://docs.docker.com/install/linux/linux-postinstall/) - Command Line Interface,
* [Docker Compose](https://docs.docker.com/compose/install/),
* [containerd.io](https://containerd.io/) - Container Management,
* [Git Kraken](https://www.liquidweb.com/kb/install-git-ubuntu-16-04-lts/),
* [Yarn](https://linuxize.com/post/how-to-install-yarn-on-ubuntu-18-04/) - Node Package Manager


### Installing

A step by step series of examples that tell you how to get a development env running

#### Git Credential
Config Git credential
```
git config credential.helper store
```
Pulling the git
```
git pull
```
Read the file
```
cat ~/.git-credentials
```
#### Modules
Fork and clone each module below:
* [account](https://code.senomas.com/seno/bhinneka-life-account.git),
* [client](https://code.senomas.com/seno/bhinneka-life-client.git),
* [client-admin](https://code.senomas.com/seno/bhinneka-life-client-admin.git),
* [cms](https://code.senomas.com/seno/bhinneka-life-cms.git),
* [param](https://code.senomas.com/seno/bhinneka-life-param.git),
* [util](https://code.senomas.com/seno/bhinneka-life-util.git),
* [micro-proxy](https://code.senomas.com/seno/micro-proxy.git)

##### Through the Modules
For each module above, repeat these steps below:  
*Start Repeating Steps*
* Rename the directory on your local computer by truncating the **bhinneka-life** prefix:  
```
mv old-name new-name
```
```
mv bhinneka-life-client client
```
* Get into the directory
```
cd client
```
* Check to see if there's no upstream yet
```
git remote -v
```
* dd the upstream to your local repository
```
git remote add upstream https://code.senomas.com/seno/bhinneka-life-client.git
```
* Check again to see if the upstream has been added to your local repository
```
git remote -v
```
* Fetching work to your local repository
```
git fetch upstream
```
* Then, merge into your local repository
```
git merge upstream/master
```
* Install Node Modules
```
export GIT_TERMINAL_PROMPT=1
yarn cache clean
cd account
yarn install
yarn upgrade
```
*End of Repeating Steps*

##### Seno Encryptor
We have another module that will be installed globally
First, install the encryptor module:
```
sudo npm install -g seno-encryptor
```
Then, initialized the user with your email address:
```
senc init spwinata@hanoman.co.id
senc invite
```
Get into your **util** directory
```
cd /util
```
Then read the file
```
senc cat config.secret.yaml
```

## Running the tests

How to run the automated tests for this system
```
gulp test
```

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

This system has deployed with two option, either you can run on a cloud with **docker** or by running locally with **gulp**. Below are the description for each option:
### Running using docker  
Get into the **util** directory
```
cd util
```
Log into the docker with these development authentication:
* uid: dev
* pwd: kampretGulun6

```
docker login docker.lumbungdana.co.id
```
Then lift up to the **Docker** by **Docker Compose**
```
docker-compose up -d
```

### Run with gulp
To run with **gulp**, get into the **cms** directory
```
cd cms
```
Then, run with gulp
```
gulp run
```
Then, get into the **client-admin** directory and run the front-end interface using **yarn**
```
cd client-admin
yarn serve
```

## Built With

* [NodeJS](https://github.com/creationix/nvm) - using NVM (Node Version Manager)
* [Yarn](https://yarnpkg.com/en/) - Dependency Management
* [Visual Studio Code](https://code.visualstudio.com/) - Code Editing - Redefined

## Contributing

Please read [CONTRIBUTING.md](https://code.senomas.com/subhan) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [Gogs](https://gogs.io/) for versioning. For the versions available, see the [tags on this repository](https://code.senomas.com/).

## Authors

* **Agus Senomas** - *Initial work* - [Senomas](https://code.senomas.com/)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
