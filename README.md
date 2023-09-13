# Rapid PowerUp Synapse-Leakix

Synapse-LeakIX is a Rapid Power-Up for Synapse, designed to improve your
cybersecurity and threat intelligence workflows by integrating with the LeakIX
platform. LeakIX is a resource indexing internet services while actively
identifying security misconfigurations.

With the Synapse-LeakIX Rapid Power-Up, you can tap into LeakIX's repository of
information and leverage its insights directly within your Synapse environment.
This README serves as your comprehensive guide, walking you through the
installation process and offering illustrative examples on how to harness the
full potential of Synapse-LeakIX.


## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation-from-source)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have met the following requirements:

1. **Synapse:** You must have a functioning installation of Synapse. If you
haven't already, refer to the Synapse documentation for installation
instructions.

2. **LeakIX Account:** You must have an active LeakIX account with API access
credentials.

## Installation from source

1. **Clone the Repository:** Clone this repository to your Synapse environment
using Git or download it as a ZIP archive and extract it.

2. **Deploy the Power-Up:** Copy the synapse-leakix directory to your Synapse
Power-Ups directory. The location may vary depending on your Synapse
installation.

    ```
    python -m synapse.tools.genpkg ./synapse-leakix.yaml \
      --push tcp://USER:PASSWORD@localhost/cortex
    ```

3. **Configuration:** Configure the Power-Up by providing your LeakIX API key.
You can do this by running a configuration command. Refer to the
[Usage](#usage) section for details.

## Usage

Once Synapse-LeakIX is installed and configured, you can use it to query LeakIX
directly from your Synapse environment. Here are some essential commands and
usage instructions:

1. **Configuring your LeakIX API Key:** Use the following command to set your
LeakIX API key:

	```
	> cyl.leakix.setup.apikey --self <your_api_key>
	```
 
2. **Querying LeakIX:** To perform queries using LeakIX, you can use commands
provided by this Power-Up. Refer to the [Examples](#examples) section for
sample queries.

## Examples

Let's explore a few examples of how to use Synapse-LeakIX:

- **Querying for IP Information**: Retrieve detailed information about a
  specific IP address using the LeakIX Power-Up.

  ```
  > cyl.leakix.search --query 'ip:8.8.8.8' --yield
  ```

- **Searching for Domains**: Perform domain-based searches with LeakIX to
  gather threat intelligence.

  ```
  > cyl.leakix.search --query 'host:google.com' --yield
  ```

These are just a few examples of what you can achieve with Synapse-LeakIX.
Refer to the documentation for more advanced queries and options.

## Contributing

We welcome contributions from the community to improve and expand the
capabilities of Synapse-LeakIX. If you have ideas, bug reports, or feature
requests, please feel free to open an issue or submit a pull request in this
repository.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use,
modify, and distribute it in accordance with the terms of the license.

---

Thank you for using Synapse-LeakIX! We hope this Power-Up enhances your
cybersecurity efforts and threat intelligence workflows. 