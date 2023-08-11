# Module 3: App Service

## Task

In this and the upcoming modules, you'll work with the [PetStore](../../../README.md), a web application that consists of:

- **Web:** PetStoreApp
- **Public APIs:** PetService, ProductService, OrderService

The source code is available [here](../../../petstore).

**Please complete the following task:**

1. Deploy on Azure App Services using Docker deployment from Azure Container Registry:
   - Web (PetStoreApp) in two different regions
   - Public API Services (PetService, ProductService, and OrderService) in one region
2. Update the configuration of the Web (PetStoreApp) to point to the URLs of the respective Public APIs.
3. Configure the Public API Services (PetService, ProductService, OrderService) for auto-scaling based on CPU load increase.
4. Verify the scalability by testing with tools like k6 to generate a load on the Public APIs.
5. Set up deployment slots for the Web project (PetStoreApp).
6. Configure Traffic Manager to direct traffic to the two Web App Services.

>**IMPORTANT:** Avoid using Kubernetes for this course, as it is not included in the curriculum and could potentially lead to unnecessary expenses.

**Useful links:**

- [Step-by-Step Guide](guides/step-by-step-guide/step-by-step-guide.md)
- [Testing Using k6 Tool](guides/using-k6/using-k6.md)

**Definition of Done:**

1. Web deployed in two separate regions using Docker deployment from Azure Container Registry.
2. Public API Services deployed in one region using Docker deployment from Azure Container Registry.
3. Web app configuration is updated to link correctly with Public API URLs.
4. Deployment slots for the Web project in one of the regions are created.
5. Public APIs are set up to scale automatically based on the CPU load increases.
6. Autoscaling is tested, potentially with k6 tool.
7. The Traffic Manager directs traffic between both Web App instances.
8. Users can access the application via the Traffic Manager URL.

<img src="images/scheme.png" width="450" style="margin: 20px 0; display: inline-block;"/>

<div style="border: 1px solid #ccc; background-color: #eee;">
  <ul>
    <li>When presenting the results of the practical tasks, please <a href="../common/presenting-results/presenting-results.md">follow these guidelines</a>.</li>
    <li>When you have completed the task, attach the screenshot to the "Result" field, and update the status to "Done."</li>
    <li>Delete resources.</li>
  </ul>
</div>
<hr>

>**IMPORTANT:** Leaving resources running can result in additional costs. Either delete resources individually or remove the entire set of resources by deleting the resource group.