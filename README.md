# Apache Pulsar Cluster with MQTT Plugin

This repository contains a Docker Compose file to deploy a Pulsar cluster with the MQTT protocol enabled using the MQTT-on-Pulsar (MoP) plugin. The setup includes Zookeeper, Bookkeeper, Pulsar Broker, and Pulsar Manager services.

## Overview

- **Zookeeper**: Manages configuration information and provides coordination services.
- **Bookkeeper**: A distributed ledger system used by Pulsar for storing messages.
- **Pulsar Broker**: The message broker that handles message routing and storage. This broker is configured to support MQTT protocol through the MoP plugin.
- **Pulsar Manager**: A web-based GUI for managing and monitoring Pulsar clusters.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. **Clone the Repository**: Clone this repository to your local machine.
2. **Prepare the MQTT Plugin**: Download the MQTT-on-Pulsar (MoP) plugin and place it in the `./protocols` directory.
3. **Configure Pulsar**: Ensure the Pulsar configuration files are correctly set up in the `./conf` directory.
4. **Start the Cluster**: Run `docker-compose up -d` to start the Pulsar cluster.

## Accessing Services

- **Pulsar Dashboard**: Access the Pulsar Manager GUI at `http://localhost:9527`.
- **MQTT**: Connect to the MQTT service on port `1883`.

## Configuration

- **MQTT Plugin**: The MQTT plugin is mounted into the Pulsar broker using Docker volumes. Ensure the MoP plugin NAR file is placed in the `./protocols` directory.
- **Pulsar Configuration**: Pulsar configuration files are mounted into the Pulsar broker from the `./conf` directory.

## Additional Information

- **MQTT-on-Pulsar (MoP)**: For more information on the MQTT-on-Pulsar plugin, refer to the [MoP GitHub repository](https://github.com/streamnative/mop).
- **Pulsar Manager**: For more details on Pulsar Manager, visit the [Pulsar Manager GitHub repository](https://github.com/apache/pulsar-manager).
