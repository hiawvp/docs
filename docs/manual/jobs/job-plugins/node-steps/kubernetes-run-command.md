# Kubernetes Clusters - Run Command (Beta)
:::enterprise
:::

## Overview

This plugin allows you to execute a command in a pod within a Kubernetes cluster. It is designed to work in conjunction with the AWS EKS, GCP GKE, and Azure AKS node-source plugins.

:::warning
Kubernetes Clusters Node Step plugins are in a Beta state
:::

## Configuration

### Required Fields

* **Pod Name**: The name of the pod to execute the command in.
* **Namespace**: The namespace where the pod resides. Default is `default`.
* **Command**: The command to execute in the pod.

### Optional Fields

* **Container**: Specify a particular container within the pod to execute the command in.
* **Shell**: Specific shell to use for executing the command in the container. Default is `/bin/sh`.

## Usage

1. Provide the name of the pod you want to execute the command in.
2. Specify the namespace where the pod is located.
3. Enter the command you want to execute.
4. Optionally, specify a particular container and/or shell to use.

## Authentication

Follow the authentication setup instructions in the [Kubernetes Plugins Overview](/manual/plugins/kubernetes-plugins-overview) documentation.

## Notes

- Make sure the command you're executing is available in the specified container.
- If no specific container is specified, the command will be executed in the first container of the pod.
- The shell option allows you to choose a different shell if the default `/bin/sh` is not available or if you need to use a different shell for specific commands.
