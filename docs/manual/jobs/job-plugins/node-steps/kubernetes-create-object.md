# Kubernetes Clusters - Create Object
:::enterprise
:::

## Overview

This plugin creates an object of a selected kind within a Kubernetes cluster. It is designed to work in conjunction with the AWS EKS, GCP GKE, and Azure AKS node-source plugins.

## Configuration

### Required Fields

* **YAML Definition**: The YAML definition of the object to be created.
* **Namespace**: The namespace where the object will be created. Default is `default`.

### Optional Fields

* **Object Type**: Select the type of object to create (e.g., Pods, ConfigMaps, Deployments). Default is "Pods".
* **Output Format**: Choose the format for the output (JSON or YAML). Default is JSON.

## Usage

1. Select the desired object type from the dropdown menu.
2. Provide the YAML definition for the object you want to create.
3. Specify the namespace where the object should be created.
4. Choose the preferred output format.

## Authentication

Follow the authentication setup instructions in the [Kubernetes Plugins Overview](/manual/plugins/kubernetes-plugins-overview) documentation.
