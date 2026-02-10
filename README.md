<a name="readme-top"></a>
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <!-- <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a> -->

  <h1 align="center">Carla Apollo Bridge</h1>
  <p align="center">
    <b>Carla & Apollo Co-simulation</b>
    <br />
    <a href="https://github.com/guardstrikelab/apollo_carla">View Demo</a>
    ·
    <a href="https://github.com/guardstrikelab/apollo_carla/issues">Report Bug</a>
    ·
    <a href="https://github.com/guardstrikelab/apollo_carla/pulls">Request Feature</a>
    <br>
  </p>
</div>


![visitor](https://komarev.com/ghpvc/?username=cleamm&label=PROFILE+VIEWS)
![issues](https://img.shields.io/github/issues/cleamm/carla_apollo_bridge_10.0)
![issues-closed](https://img.shields.io/github/issues-closed/cleamm/carla_apollo_bridge_10.0)
![issues-pr](https://img.shields.io/github/issues-pr/cleamm/carla_apollo_bridge_10.0)
![last-commit](https://img.shields.io/github/last-commit/cleamm/carla_apollo_bridge_10.0)
[![TODOs](https://badgen.net/https/api.tickgit.com/badgen/github.com/guardstrikelab/carla_apollo_bridge)](https://www.tickgit.com/browse?repo=github.com/guardstrikelab/carla_apollo_bridge)
![milestones](https://img.shields.io/github/milestones/all/cleamm/carla_apollo_bridge_10.0)
![repo-size](https://img.shields.io/github/repo-size/cleamm/carla_apollo_bridge_10.0)
![lines](https://img.shields.io/tokei/lines/github/cleamm/carla_apollo_bridge_10.0)
![language](https://img.shields.io/badge/language-python-orange.svg)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://github.com/guardstrikelab/carla_apollo_bridge/blob/master/LICENSE)
![stars](https://img.shields.io/github/stars/cleamm/carla_apollo_bridge_10.0?style=social)

<!-- ABOUT THE PROJECT -->
## About
This project aims to provide a data and control bridge for the communication between Carla and Apollo. It was tested with [Carla 0.9.14](https://github.com/carla-simulator/carla/tree/0.9.14) and the [Apollo v10.0.0](https://github.com/ApolloAuto/apollo/tree/v10.0.0) (v10.0.0)

![image](docs/images/demo.gif)

<!-- GETTING STARTED -->
## Getting Started
Please refer to [Getting Started](docs/GettingStarted.md)

### HIL cluster management

Supporting remote scheduling of VTD HIL, Dspace HIL, task management, data import and export, simulation logs, and simulation report retrieval.

### SIL simulation capability

Supporting perceptual algorithm testing, regulatory testing, and end-to-end testing of perceptual regulation. The algorithm supports Apollo/ROS/Simulink/C++ access.

### Scenario library management

Unified management of scene libraries, classification, grouping, and labeling of scene libraries, support for automatic push of scene libraries to HIL SIL simulation software for simulation testing.

### Sensor model management

Supporting the definition of sensor internal and external parameters for different vehicle models and versions, and supporting the deployment of sensor configurations for a certain vehicle model to the HIL SIL simulation platform.

### Scenario building

Supporting different departments and teams to build scenarios through UI and code, making it easy for testing departments to use.

### Analyze and evaluate

Supporting the testing department to uniformly write testing rules in the cloud for backup.

### Cloud simulation task creation

With the freedom to select scenarios and evaluation rules, sensor models, and tested objects (algorithm software or domain controllers) to initiate simulation tasks, and automatically send back test reports.

### Task management

Supporting different departments and teams to conduct simulation tasks, scenario building tasks, evaluation rule writing tasks, algorithm code submission tasks, etc. based on different business permissions.

<!-- CONTRIBUTING -->
## Contribution

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contribution you make is **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the Apache-2.0 License. See `LICENSE` for more information.

## Acknowledgments

This work is based on the following open-source projects:

* [Apollo](https://github.com/ApolloAuto/apollo)
* [Carla Apollo Bridge](https://github.com/AuroAi/carla_apollo_bridge)
* [Carla Apollo](https://github.com/casper-auto/carla-apollo)

* [ApolloAuto - application-core](https://github.com/ApolloAuto/application-core/tree/10.0.0)

## Forked This Page!

* [guardstrikelab Carla Apollo Bridge](https://github.com/guardstrikelab/carla_apollo_bridge)


<p align="right">(<a href="#readme-top">back to top</a>)</p>