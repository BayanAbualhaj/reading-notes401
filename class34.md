# login **and** Auth

![](https://miro.medium.com/max/3176/1*SzrSsS1stZQ7ipYObndbAw.png)


## Why is the Context API useful?

allows you to share information to any component

--------------------
## Can a component outside of a provider get its context?

Yes

------------------

## What are some common use cases for using the Context API?

change the theam

---------------------


## Describe “Context Hell”.

Without useContext, you may need to pass or drilling props to each components in the app to be access for the components that will consume it.

-------------------

* **global state**	state in multiple components that are not directly connected.

* **global context**: Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user.

* **provider**: React uses provider pattern in Context API to share data across tree descendants

* **consumer**: <MyContext.Consumer> {value => /* render something based on the context value */} </MyContext.Consumer> A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.

__________________________

## What is Role-Based Access Control


Role-based access control (RBAC) restricts network access based on a person’s role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.


Through RBAC, you can control what end-users can do at both broad and granular levels. You can designate whether the user is an administrator, a specialist user, or an end-user, and align roles and access permissions with your employees’ positions in the organization. Permissions are allocated only with enough access as needed for employees to do their jobs.


What if an end-user’s job changes? You may need to manually assign their role to another user, or you can also assign roles to a role group or use a role assignment policy to add or remove members of a role group.


## Some of the designations in an RBAC tool can include:

* Management role scope – it limits what objects the role group is allowed to manage.
* Management role group – you can add and remove members.
* Management role – these are the types of tasks that can be performed by a specific role group.
* Management role assignment – this links a role to a role group.

## BENEFITS OF RBAC

* Reducing administrative work and IT support.
* Maximizing operational efficiency.
* Improving compliance.

## BEST PRACTICES FOR IMPLEMENTING RBAC


Implementing a RBAC into your organization shouldn’t happen without a great deal of consideration. There are a series of broad steps to bring the team onboard without causing unnecessary confusion and possible workplace irritations. Here are a few things to map out first.