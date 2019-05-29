prerequisites for running caliper tests:

You must have installed:

1) NodeJS 8.X
2) node-gyp
3) Docker
4) Docker-compose

When all prerequistes are fulfilled:
1) In main(the same as this file) catalog run commands:
    1.1 npm install
    1.2 npm run repoclean
    1.3 npm run bootstrap

2) to run example tests go to packages/caliper-application/scripts/
    2.1 to run example fabric test use command
    node run-benchmark.js -c ../benchmark/simple/config.yaml -n ../network/fabric-v1.4/1org10peer/

    2.2 to run example Sawtooth test
    node run-benchmark.js -c ../benchmark/simple/config-sawtooth.yaml -n ../network/sawtooth-poet/sawtooth-poet-10-validators/sawtooth.json

    2.3 to run example iroha test

3) All test should be able to run succesfully on a local machine, tests with more validators might be not able to run due to too low CPU power.


How to install required software:
    1) NodeJS 8
        sudo apt update
        sudo apt install nodejs npm
        nodejs --version

        sudo apt install npm
        npm --version
    2) node-gyp
        sudo npm install -g node-gyp

    3) docker
        sudo apt-get update
        sudo apt-get install docker-ce docker-ce-cli containerd.io
        sudo docker run hello-world
    
    4) docker-compose
        sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

        sudo chmod +x /usr/local/bin/docker-compose
        docker-compose --version