
## Getting Started

<!-- ### Prerequisites

We will run Carla and Apollo in docker. Furthermore, NVIDIA Container Toolkit is needed. You can refer to the following link to install NVIDIA Container Toolkit:
* https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html

Alternatively, simply perform the following steps：

* docker

  ```sh
  sudo apt-get install docker.io
  ```
* NVIDIA Container Toolkit

  ```sh
  curl https://get.docker.com | sh && sudo systemctl --now enable docker
  ```
  ```sh
  distribution=$(. /etc/os-release;echo $ID$VERSION_ID) \
      && curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
      && curl -s -L https://nvidia.github.io/libnvidia-container/$distribution/libnvidia-container.list | \
            sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
            sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
  ```
  ```sh
  sudo apt-get update
  sudo apt-get install -y nvidia-docker2
  sudo systemctl restart docker
  ```

* docker-compose

  ```
  sudo curl -L "https://github.com/docker/compose/releases/download/v2.0.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  ```

* Change File Permission:

  ``` sh
  sudo chmod +x /usr/local/bin/docker-compose 
  ```

> Apply executable permissions to the standalone binary in the target path for the installation.
> Test and execute compose commands using docker-compose.
> **Note:**
> If the command docker-compose fails after installation, check your path. You can also create a symbolic link to /usr/bin or any other directory in your path. For example:

```sh
 sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
``` -->

### Build And Run Apollo

* Refer to this link：
  <br> https://apollo.baidu.com/docs/apollo/10.x/md_docs_2_xE5_xAE_x89_xE8_xA3_x85_xE6_x8C_x87_xE5_x8D_x97_2_xE5_xAE_x89_xE8_xA3_x85_xE6_x8C_x87_xE5_x8D_x97.html

1. Clone apollo-core v10.0.0 
    ```sh
    # Using SSH
    git clone git@github.com:ApolloAuto/application-core.git


    # Using HTTPS
    git clone https://github.com/ApolloAuto/application-core.git
    ```

2. Build Apollo
    ```sh
    cd application-core

    # env setting
    bash setup.sh

    # container start
    aem start
    ```
    Then, build

    ```sh
    buildtool build

    # check path
    - application-core/.aem # hidden folder
    - application-core/.aem/envroot/opt/apollo/neo/include/cyber
    - application-core/.aem/envroot/opt/apollo/neo/python/cyber/proto
    - application-core/.aem/envroot/opt/apollo/neo/python/cyber/python/cyber_py3
    ```

    Run this command in the container to start Dreamview
  
    ```sh
    aem bootstrap start --plus
    ```
    Finally, open the link in your browser

    ```sh
    http://localhost:8888/
    ```

<!-- ### Refined Controller

Note that this project provides a refined MPC controller that improves the performance of the Apollo MPC controller in this co-simulation. Please refer to [RefinedController.md](RefinedController.md) for details. -->

3. Run Carla

* Clone the carla_apollo_bridge project outside Apollo container
  ```sh
  # Using SSH
  git clone git@github.com:cleamm/carla_apollo_bridge_10.0.git
  
  #Using HTTPS
  git clone https://github.com/cleamm/carla_apollo_bridge_10.0.git
  ```

* Pull carla image and run

  ```sh
  cd carla_apollo_bridge
  ./carla_scripts/docker_run_carla.sh
  ```

## Run carla_apollo_bridge
1.  Copy the src folder into Apollo container
    ```sh
    docker cp carla_bridge <apollo_container_name>:/apollo/modules/carla_bridge
    ```
2.  Install carla_bridge

    Enter the Apollo container and run:
    ```sh
    cd /apollo/modules/carla_bridge
    chmod +x install.sh
    ./install.sh
    source ~/.bashrc
    ```

    but I don't need command `source ~/.bashrc`

3. Start the bridge
    ```
    python3 main.py
    ```

<!-- ### Result
If everything above goes well, you should see this in Apollo client: 
 
![image](images/Apollo.png)

and this in Carla:

![image](images/CarlaUE4.png) -->
<!-- ## Example: start a co-simulation
1. Open apollo client: http://localhost:8888
2. If dreamview doesn't display the map, switch to carla_town04 and then switch back. 
3. (Optional) Select "Task" in the sidebar and turn on "Camera Sensor" in "Others".
4. (Optional) Select "Layer Menu" in the sidebar and turn on "Point Cloud" in "Perception".
5. Select "Module Controller" in the sidebar and turn on "Routing", "Localization", "Planning", "Control", "Predict" module.
6. Select "Route Editing" in the sidebar.
7. Click "Add Point of Interest" and left click at any point on the road to set the destination.
8. Click "Send Routing Request". -->


