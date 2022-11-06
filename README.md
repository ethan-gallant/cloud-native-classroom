# Cloud-Native Classroom
A platform for learning Kubernetes administration and application development.

## What is Cloud-Native Classroom?
Cloud-Native Classroom is a platform designed to help a group of students learn to work with Kubernetes. It does all the heavy-lifting so students don't need to learn the complexities of getting their environments set up. It also provides a way for students to work together on a shared project (soon).

## How does it work?
Cloud-Native Classroom is a Kubernetes operator that configures OAuth2 for students in a given directory. Students once setup will have access to a namespace and a VSCode remote IDE in the web with Kubectl and required tools installed. Each student gets their own namespace and can work on their own projects.

The IDE (VSCode Server) is hosted within the namespace that the student will work in. This allows students to work on their own projects and not have to worry about other students messing with their work. The IDE is also configured to use the student's namespace as the default namespace for Kubectl. This means that students can use Kubectl without having to specify the namespace each time.

There are three parts:
1. The operator which handles creating Classrooms and keeps students namespaces in sync
2. The Registrar which handles authentication, creating namespaces, and configuring the IDE in the student's namespace
3. The Class-Portal an Envoy proxy that handles routing to the correct IDE per student
4. The IDE (VSCode Server) which is hosted in the student's namespace. Each student gets their own IDE.
5. The Proctor which provides a visual interface for students and the instructor to see what is happening inside the cluster with graph visualisation. 