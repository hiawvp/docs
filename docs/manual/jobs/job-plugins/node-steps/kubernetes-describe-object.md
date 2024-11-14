# Kubernetes Clusters - Describe Object (Beta)
:::enterprise
:::

## Overview

This plugin describes an object of a selected kind within a Kubernetes cluster. It is designed to work in conjunction with the AWS EKS, GCP GKE, and Azure AKS node-source plugins.

:::warning
Kubernetes Clusters Node Step plugins are in a Beta state
:::

## Configuration

### Required Fields

* **Name**: The name of the object to be described, such as Pod name or Deployment name.
* **Namespace**: The namespace where the object resides. Default is `default`.

### Optional Fields

* **Object Type**: Select the type of object to describe (e.g., Pods, ConfigMaps, Deployments). Default is "Pods".
* **Output Format**: Choose the format for the output (JSON or YAML). Default is JSON.

## Usage

1. Select the desired object type from the dropdown menu.
2. Provide the name of the object you want to describe.
3. Specify the namespace where the object is located.
4. Choose the preferred output format.

## Authentication

Follow the authentication setup instructions in the [Kubernetes Plugins Overview](/manual/plugins/kubernetes-plugins-overview) documentation.
