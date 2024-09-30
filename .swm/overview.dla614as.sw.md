---
title: Overview
---
WhoOwesWhat-Net48 is a system designed to manage and track debts and credits among friends, allowing users to keep track of who owes what to whom.

## Main Components

### Service Controllers

Service Controllers are interfaces that define the contract for various operations related to users, errors, synchronization, and friend requests. They are responsible for handling the logic and interactions between the service layer and the underlying data repositories, ensuring that the appropriate actions are taken based on the requests they receive.

- <SwmLink doc-title="Service Controllers Overview">[Service Controllers Overview](/.swm/service-controllers-overview.1p4ryvu4.sw.md)</SwmLink>

### Service Configuration

Service configuration involves setting up various parameters and dependencies required for the application to function correctly. This includes configuring database connections, logging mechanisms, dependency injection, and handling cross-origin requests. Proper configuration is essential for the application to operate seamlessly across different environments and to facilitate maintenance and updates.

- <SwmLink doc-title="Service Configuration Overview">[Service Configuration Overview](/.swm/service-configuration-overview.3f3w18ln.sw.md)</SwmLink>
- <SwmLink doc-title="Dockerfile Configuration for WhoOwesWhat.Service">[Dockerfile Configuration for WhoOwesWhat.Service](/.swm/dockerfile-configuration-for-whooweswhatservice.gwoiqdka.sw.md)</SwmLink>

### Deployment Scripts

Deployment scripts automate the process of building, packaging, and deploying the application to various environments, ensuring consistency and reducing manual errors.

- <SwmLink doc-title="Deployment Scripts Overview">[Deployment Scripts Overview](/.swm/deployment-scripts-overview.ww8fjgsx.sw.md)</SwmLink>

### Data Provider Interfaces

Data Provider Interfaces define the contract for data operations, ensuring a consistent way to handle data access and manipulation across different entities like groups, friends, and transactions.

- <SwmLink doc-title="Data Provider Interfaces Overview">[Data Provider Interfaces Overview](/.swm/data-provider-interfaces-overview.g6sw2byx.sw.md)</SwmLink>

### Data Provider

Data Provider refers to the component responsible for managing data access and manipulation. It includes logic for updating entities, mapping data between different layers, and ensuring data consistency. The Data Provider plays a crucial role in abstracting the data access layer, allowing for easier testing and maintenance of the codebase.

- <SwmLink doc-title="Overview of Post Entity in Data Provider">[Overview of Post Entity in Data Provider](/.swm/overview-of-post-entity-in-data-provider.eupgs5jz.sw.md)</SwmLink>
- <SwmLink doc-title="Basic Concepts of Transaction Entity in Data Provider">[Basic Concepts of Transaction Entity in Data Provider](/.swm/basic-concepts-of-transaction-entity-in-data-provider.ut3np06t.sw.md)</SwmLink>
- <SwmLink doc-title="Basic concepts of Who Owes What Context">[Basic concepts of Who Owes What Context](/.swm/basic-concepts-of-who-owes-what-context.lv23w8ep.sw.md)</SwmLink>
- <SwmLink doc-title="Getting Started with Person Entity in Data Provider">[Getting Started with Person Entity in Data Provider](/.swm/getting-started-with-person-entity-in-data-provider.232n6ydq.sw.md)</SwmLink>
- <SwmLink doc-title="Getting Started with User Credential Management">[Getting Started with User Credential Management](/.swm/getting-started-with-user-credential-management.5lc50qvh.sw.md)</SwmLink>
- **Group entity**
  - <SwmLink doc-title="Getting Started with Group Entity in Data Provider">[Getting Started with Group Entity in Data Provider](/.swm/getting-started-with-group-entity-in-data-provider.srabf7cg.sw.md)</SwmLink>
  - <SwmLink doc-title="The IGroupContext class">[The IGroupContext class](/.swm/the-igroupcontext-class.eryvw.sw.md)</SwmLink>

### Domain Logic

Domain Logic refers to the part of the application that encodes the business rules, processes, and logic specific to the problem domain. It is responsible for implementing the core functionality and behavior of the system, such as handling transactions, managing relationships between entities, and enforcing business rules. Domain Logic ensures that the system operates according to the defined business requirements and constraints.

- <SwmLink doc-title="Exploring Friend in Domain Logic">[Exploring Friend in Domain Logic](/.swm/exploring-friend-in-domain-logic.bv0gw9cr.sw.md)</SwmLink>
- <SwmLink doc-title="Basic Concepts of Group Management">[Basic Concepts of Group Management](/.swm/basic-concepts-of-group-management.yynpmv9g.sw.md)</SwmLink>
- <SwmLink doc-title="Basic Concepts of Post in Domain Logic">[Basic Concepts of Post in Domain Logic](/.swm/basic-concepts-of-post-in-domain-logic.q39e3ud9.sw.md)</SwmLink>

### Flows

- <SwmLink doc-title="Setting Up an Azure Web Application Environment">[Setting Up an Azure Web Application Environment](/.swm/setting-up-an-azure-web-application-environment.7ti3dl1n.sw.md)</SwmLink>

## Tests

<SwmLink doc-title="Tests Overview">[Tests Overview](/.swm/tests-overview.2kip0aw4.sw.md)</SwmLink>

*This is an auto-generated document by Swimm AI 🌊 and has not yet been verified by a human*

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48"><sup>Powered by [Swimm](https://app.swimm.io/)</sup></SwmMeta>
