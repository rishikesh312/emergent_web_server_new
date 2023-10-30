**Emergent Web Server (EWS)**

**Abstract:**  
EWS serves as a model to study online learning in self-adaptive systems with a compositional structure. This reference implementation will guide users on setting up and interacting with the EWS system.

---

**1. Introduction**

EWS is available as a Docker container, easing the setup process. The exemplar facilitates exploration of the learning capabilities in compositional adaptive systems. The system can also be setup natively. This document provides a comprehensive guide for both methods.

---

**2. Quick Start with Docker**

* **Requirements:** Docker (Installation guide available at [Docker's official website](https://www.docker.com/get-started)).

* **Steps:**

  i. Pull and run the EWS Docker image:
     ```bash
     $ docker run --name=ews -p 2011-2012:2011-2012 -d robertovrf/ews:1.0
     ```

  ii. Verify if the EWS container is active:
     ```bash
     $ docker container ls
     ```

  iii. Access EWS terminal within the container:
     ```bash
     $ docker exec -it ews bash
     ```

  iv. Launch EWS:
     ```bash
     # dana -sp ../repository InteractiveEmergentSys.o
     ```

* **Interactions:** Once launched, you can use commands such as `sys> help` and `sys> get_all_configs` to interact with the EWS API. For more detailed instructions, refer to the "Interactive Emergent System" section in the original guide.

---

**3. Native Installation**

* **Requirements:**

  i. Dana Programming Language (v251) - [Installation Guide](http://www.projectdana.com/dana/guide/installation)
  
  ii. Python 3.7 - [Download](https://www.python.org/downloads/)
  
  iii. Perl 5 - [Download](https://www.perl.org/get.html)

* **Setup:**

  i. Clone the EWS repository.

  ii. Navigate to the main project directory.

  iii. Build the project using the `make.dn` building tool:
     ```bash
     $ dana make.dn
     $ dana make.o -l all
     ```

  iv. Start EWS:
     ```bash
     $ dana -sp ../repository InteractiveEmergentSys.o
     ```

  v. Interact using available client scripts or use the Python module, PyEWS.

---

**4. Troubleshooting**

Logs related to EWS activities in the Docker container are available at `'emergent_web_server/pal/em.log'`. If any issues arise, this log file can provide insights. For other concerns or inquiries, users can contact the developers via email.

---

**5. Conclusion**

This reference implementation serves as a concise guide for users aiming to explore the EWS system's capabilities. With options for a Docker container setup or a native installation, users can choose their preferred method to dive deep into the functionalities and features of EWS.
