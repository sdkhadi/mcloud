MCloud master instance
==================

MCloud is dockerized QA infrastructure for remote web access to physical devices (Android and iOS). Is is fully integrated into the [qps-infra](http://www.qps-infra.io) ecosystem and can be used for manual so automation usage.

* It is built on the top of [OpenSTF](https://github.com/openstf) with supporting iOS devices remote control.

## Contents
* [Software prerequisites](#software-prerequisites)
* [Initial setup](#initial-setup)
* [Services start/stop/restart](#services-restart)
* [License](#license)

## Software prerequisites
* Install [docker](http://www.techrepublic.com/article/how-to-install-docker-on-ubuntu-16-04/)
* Installed [docker-composer](https://docs.docker.com/compose/install/#install-compose)

## Initial setup
* Clone repo and execute ./setup.sh shell script providing public ip address or fully qualified domain name of the MCloud server
```
git clone https://github.com/qaprosoft/mcloud
cd ./mcloud
./setup.sh demo.qaprosoft.com
```
<B>Note</B>: public ip and 80 http port should be accessible from user's browsers. Also to be able to connect to devices remotely range of ports should be opened (7400-7700).
* Setup Android provider using steps from [android-slave](https://github.com/qaprosoft/mcloud/tree/android-slave) branch
* Setup iOS provider using steps from [ios-slave](https://github.com/qaprosoft/mcloud/tree/ios-slave) branch

## Services start/stop/restart
* Use ./stop.sh script to stop everything
* User ./start.sh to start all containers

## Usage
* SmartTestFarm url to manage connected Android and iOS devices: http://<PUBLIC_IP>/stf 
  > authenticate yourself based on preconfigured auth system and enjoy.
* Selenium Grid Console url: http://<PUBLIC_IP>:4444/grid/console

## License
Code - [Apache Software License v2.0](http://www.apache.org/licenses/LICENSE-2.0)

Documentation and Site - [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/deed.en_US)
