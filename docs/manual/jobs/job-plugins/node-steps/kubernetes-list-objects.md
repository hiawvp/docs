# Kubernetes Clusters - List Objects (Beta)
:::enterprise
:::

## Overview

This plugin lists objects of a selected kind within a Kubernetes cluster. It is designed to work in conjunction with the AWS EKS, GCP GKE, and Azure AKS node-source plugins.

:::warning
Kubernetes Clusters Node Step plugins are in a Beta state
:::

## Configuration

### Required Fields

* **Namespace**: The namespace to list objects from. Default is `default`.

### Optional Fields

* **Object Type**: Select the type of object to list (e.g., Pods, ConfigMaps, Deployments). Default is "Pods".
* **All Namespaces**: If selected, retrieve objects from across all namespaces. The 'Namespace' field will be ignored.
* **Label Selector**: Filter objects based on labels. Supports equality-based and set-based selectors.
* **Field Selector**: Filter objects based on fields. Supports equality-based and set-based selectors.
* **Output Format**: Choose the format for the output (Simple List, JSON, or YAML). Default is "Simple List".

## Usage

1. Select the desired object type from the dropdown menu.
2. Specify the namespace or choose to list from all namespaces.
3. Optionally, add label or field selectors to filter the results.
4. Choose the preferred output format.

## Authentication

Follow the authentication setup instructions in the [Kubernetes Plugins Overview](/manual/plugins/kubernetes-plugins-overview) documentation.

## Notes

- For detailed information on label selectors, refer to the [Kubernetes documentation on label selectors](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/#label-selectors).
- For detailed information on field selectors, refer to the [Kubernetes documentation on field selectors](https://kubernetes.io/docs/concepts/overview/working-with-objects/field-selectors/).
