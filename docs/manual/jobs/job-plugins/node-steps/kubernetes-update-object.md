# Kubernetes Clusters - Update Object (Beta)
:::enterprise
:::

## Overview

This plugin updates a specified object of a selected kind within a Kubernetes cluster. It is designed to work in conjunction with the AWS EKS, GCP GKE, and Azure AKS node-source plugins.

:::warning
Kubernetes Clusters Node Step plugins are in a Beta state
:::

## Configuration

### Required Fields

* **Object Name**: The name of the object to be updated.
* **YAML Definition**: The YAML definition of the object to be updated.
* **Namespace**: The namespace where the object resides. Default is `default`.

### Optional Fields

* **Object Type**: Select the type of object to update (e.g., Pods, Deployments, Services). Default is "Pods".

## Usage

1. Provide the name of the object you want to update.
2. Select the desired object type from the dropdown menu.
3. Enter the updated YAML definition for the object.
4. Specify the namespace where the object is located.

## Authentication

Follow the authentication setup instructions in the [Kubernetes Plugins Overview](/manual/plugins/kubernetes-plugins-overview) documentation.

## Notes

- The plugin uses a field manager named "runbook-automation/apply-patch" for tracking changes.
- Ensure that the YAML definition provided is complete and correct for the object you're updating.
