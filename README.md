### **Emergent Web Server (EWS)**

---

#### **1. Setting Up**

1. **Docker**: Ensure Docker is installed and configured on your machine. If not, follow the instructions at [Docker's Get Started page](https://www.docker.com/get-started).

---

#### **2. Quick Start with Docker**

1. **Running the EWS Container**:
    ```bash
    $ docker run --name=ews -p 2011-2012:2011-2012 -d robertovrf/ews:1.0
    ```

2. **Check the Running Containers**:
    ```bash
    $ docker container ls
    ```

3. **Accessing the EWS Container Terminal**:
    ```bash
    $ docker exec -it ews bash
    ```

4. **Executing EWS Tool inside the Container**:
    ```bash
    # dana -sp ../repository InteractiveEmergentSys.o
    ```

5. **Interacting with EWS API**:
    - Get all available commands:
        ```bash
        sys> help
        ```
    - List all available compositions:
        ```bash
        sys> get_all_configs
        ```
    - Check the current webserver composition:
        ```bash
        sys> get_config
        ```
    - Change composition (e.g., to 3):
        ```bash
        sys> set_config 3
        ```

6. **Access the Web Server**:
    - Open a web browser and go to: [http://localhost:2012/](http://localhost:2012/)

---

#### **3. Perception and Learning**

1. **Obtaining Perception Data**:
    ```bash
    sys> get_perception
    ```

2. **Execute the Learning Module**:
    ```bash
    sys> learn
    ```

    - When prompted, input the parameters as recommended:
        - Observation Window: `5000`
        - Exploration Threshold: `3`
        - Number of Rounds: `52`

3. **Executing a Client Script**:
    - Open a new terminal instance:
        ```bash
        $ docker exec -it ews bash
        ```
    - Navigate to client scripts directory:
        ```bash
        # cd ../ws_clients
        ```
    - Execute a client script (example):
        ```bash
        # dana ClientTextPattern.o
        ```

---

#### **4. Native Install**

For users who prefer not to use Docker, the native installation method requires the following:

1. **External Dependencies**:
    - Dana Programming Language: Follow the [installation guide](http://www.projectdana.com/dana/guide/installation).
    - Python 3.7: Download and install from [Python's official website](https://www.python.org/downloads/).
    - Perl 5: Download and install from [Perl's official website](https://www.perl.org/get.html).

2. **Compilation**:
    - Compile the `make.dn` tool:
        ```bash
        $ dana make.dn
        ```
    - Execute `make.o` with suitable options:
        ```bash
        $ dana make.o -l all
        ```

3. **Executing EWS Natively**:
    - Execute `EmergentSys.o`:
        ```bash
        $ dana -sp ../repository EmergentSys.o
        ```
    - Execute `InteractiveEmergentSys.o`:
        ```bash
        $ dana -sp ../repository InteractiveEmergentSys.o
        ```

4. **Executing Client Scripts**:
    - For example:
        ```bash
        $ dana ClientTextPattern.o
        ```

---

#### **5. Troubleshooting**

1. Check logs in `emergent_web_server/pal/em.log` for any issues.
2. For further assistance, contact `robertovito [at] ufg.br`.

---

Thank you for using the EWS artifact! 

**Note**: This reference guide provides a structured and easy-to-follow format based on the given information. It streamlines the process for users to set up and use the EWS tool.
