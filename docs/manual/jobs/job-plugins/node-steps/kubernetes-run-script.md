# Kubernetes Clusters - Run Script (Beta)
:::enterprise
:::

## Overview

This plugin executes a script using a predefined container image within a Kubernetes cluster. It deploys a Kubernetes Job to run the script in a container, then deletes the Job after execution. This plugin is designed to work in conjunction with the AWS EKS, GCP GKE, and Azure AKS node-source plugins.

:::warning
Kubernetes Clusters Node Step plugins are in a Beta state
:::

## Configuration

### Required Fields

* **Script**: The script to execute in the container.
* **Invocation Command**: The command to execute the script in the container. Default is `sh -c`.
* **Container Image**: The container image to use for script execution. Default is `amazon/aws-cli`.
* **Namespace**: The namespace where the Kubernetes Job will be deployed. Default is `default`.

### Optional Fields

* **Environment Variables**: Environment variables to pass to the container (YAML syntax).
* **Image Pull Policy**: The image pull policy for the container. Options are "Always", "IfNotPresent", or "Never". Default is "Always".

## Usage

1. Enter the script you want to execute.
2. Specify the invocation command (if different from default).
3. Choose the container image to use.
4. Specify the namespace for the Job deployment.
5. Optionally, add environment variables and set the image pull policy.

## Authentication

Follow the authentication setup instructions in the [Kubernetes Plugins Overview](/manual/plugins/kubernetes-plugins-overview) documentation.

## Notes

- The Job is automatically deleted after script execution.
- Environment variables support the 'valueFrom' field for referencing secrets and other sources. See [Kubernetes Docs](https://kubernetes.io/docs/tasks/inject-data-application/define-environment-variable-container/) for detailed syntax and examples.
- Predefined container images include options like `amazon/aws-cli`, `bitnami/kubectl`, `mcr.microsoft.com/azure-cli`, `google/cloud-sdk`, and `dtzar/helm-kubectl`, but custom images can also be specified.
