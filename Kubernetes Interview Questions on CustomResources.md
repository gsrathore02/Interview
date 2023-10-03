```
#Kubernetes Interview Questions on CustomResources
```
```
1. What are Custom Resources in Kubernetes?

Asnwer: Custom Resources (CRs) are an extension mechanism in Kubernetes that allows you to define and use custom objects in addition to the built-in resources like Pods, Services, and Deployments. They provide a way to extend the Kubernetes API to suit your application's specific needs.
```
```
2. Why would you use Custom Resources in Kubernetes?

Custom Resources are useful when you need to represent and manage application-specific resources that are not natively supported by Kubernetes. They enable you to define, create, and manage these resources using the Kubernetes API and tooling.
```
```
3. What is the difference between Custom Resources and Custom Resource Definitions (CRDs)?

Custom Resources are instances of custom objects, while Custom Resource Definitions (CRDs) define the schema or structure for these custom objects. CRDs specify the kind of custom resources that can be created and their validation rules.
```
```
4. How do you create a Custom Resource in Kubernetes?

To create a Custom Resource, you first need to define a Custom Resource Definition (CRD) that specifies the resource's schema. Once the CRD is created, you can create instances of the custom resource by applying YAML manifests that conform to the CRD's schema.
```
```
5. Explain the structure of a Custom Resource Definition (CRD).

A CRD typically includes the following fields:

apiVersion: The API version of the CRD.

kind: The kind of resource, which is typically "CustomResourceDefinition."

metadata: Metadata for the CRD.

spec: Defines the structure and validation rules for the custom resource, including its fields and their types.

```
```
6. What is a Controller in the context of Custom Resources?

Controllers are Kubernetes components or custom operators that watch for changes to Custom Resources and take action based on those changes. They help automate the management of custom resources by reconciling the desired state specified in the CR with the actual state of the resource.
```
```
7. Can you explain the reconciliation loop in a Custom Resource Controller?

The reconciliation loop is a core concept in a Custom Resource Controller. It continuously watches for changes in Custom Resources, compares the current state of the resource with the desired state specified in the CR, and takes actions to align them. This loop ensures that the custom resources are maintained as per their specifications.
```
```
8. What are some common use cases for Custom Resources in Kubernetes?

Common use cases include managing application-specific configurations, deploying and scaling custom applications, managing external resources or services, and automating complex workflows.
```
```
9. What tools or libraries can you use to build Custom Resource Controllers?

Popular choices include Kubernetes client libraries (e.g., client-go), Operator SDK, and Kubebuilder. These tools help simplify the development of Custom Resource Controllers.
```
```
10. How do you validate a Custom Resource to ensure it adheres to its CRD's schema?

You can define validation rules within the spec field of the CRD. Kubernetes will automatically validate any Custom Resources created against these rules. Additionally, you can implement custom validation logic in your Custom Resource Controller.
```
