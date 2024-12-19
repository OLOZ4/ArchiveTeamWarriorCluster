# Archive Team Warrior Multi-Instance Docker Deployment

## Overview
----------
This repository provides a single Dockerfile configuration to launch multiple instances of [Archive Team Warrior](https://github.com/internetarchive/heritrix3/wiki) in using multiple containers. This allows for scalable and efficient web archiving.

## Prerequisites
--------------
* Docker installed on your machine
* Docker Compose installed on your machine

## Getting Started
-------------------
### Cloning the Repository
```git clone https://github.com/OLOZ4/ArchiveTeamWarriorCluster.git```


### Running the Container
```cd ArchiveTeamWarriorCluster```
```docker-compose up```

This will start multiple instances of Archive Team Warrior, as specified in the `docker-compose.yml` file.

## Configuration
--------------
### Environment Variables
| Variable   | Default Value  | Description  |
|----------|--------------|-------------|
| scale  | 10            | Number of Archive Team Warrior instances to launch  |
| ports    | 8001-8011  | Port range for the containers. port range should equal to variable "scale" (so let's say scale = 10, then ports are 8001-8011 if you subtract them you will get 10)|
| DOWNLOADER  | xxm | username  |


## Troubleshooting
-------------------
### Common Issues

* If you encounter issues with the container not launching, check the Docker logs for errors.
* If you need to adjust the port range or instance count, update the `docker-compose.yml` file and restart the containers.

## License
---------
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Acknowledgments
----------------
Special thanks to the Archive Team Warrior developers for their excellent work on this project!

## Contributing
--------------
If you'd like to contribute to this repository or suggest improvements, please submit a pull request.
