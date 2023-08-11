# Module 8: Service Bus. Event Hub. Event Grid. Logic Apps

## Task

The source code is available [here](../../../petstore).

The PetStore application enables customers to add products to their shopping carts, effectively initializing orders. Currently, the mechanism in place to transmit requests to the storage to reserve the selected items is implemented as a OrderItemsReserver service, utilizing HTTP Trigger Azure Functions.

**Please complete the following task:**

1. Establish communication between the PetStore application and the OrderItemsReserver through a messaging service (Azure Service Bus).
2. Update the OrderItemsReserver service to utilize Service Bus Trigger Azure Functions instead of HTTP Trigger.
3. The OrderItemsReserver should generate order requests and upload them as a JSON file to Blob Storage.
4. This should happen every time a customer updates the shopping cart during the same session.
5. The generated request should contain order details and the product list.
6. Ensure that the file is overwritten for each user session whenever an update is made.
7. Implement a retry policy for uploading to Blob Storage. In case of an unsuccessful attempt, the code will make up to 3 retry attempts.
8. Implement a fallback scenario using Logic Apps. If the file cannot be created (storage is unavailable, an exception occurs during processing, etc.), an email should be sent with the order details.

**Definition of Done:**

1. The PetStore application has been modified and deployed to the Azure App Service.
2. The OrderItemsReserver service has been updated and deployed as a Service Bus Trigger Azure Function.
3. The communication service (Service Bus) between the PetStore application and the OrderItemsReserver service is created and properly configured.
4. Every time a customer updates the shopping cart within the same session, a new JSON file containing the order details appears in Blob Storage.
5. If the file cannot be created in Blob Storage, an email with the order details is sent after 3 retry attempts.

<img src="images/scheme.png" width="650" style="margin: 20px 0; display: inline-block;"/>

<div style="border: 1px solid #ccc; background-color: #eee;">
  <ul>
    <li>When presenting the results of the practical tasks, please <a href="../common/presenting-results/presenting-results.md">follow these guidelines</a>.</li>
    <li>When you have completed the task, attach the screenshot to the "Result" field, and update the status to "Done."</li>
    <li>Delete resources.</li>
  </ul>
</div>
<hr>

>**IMPORTANT:** Leaving resources running can result in additional costs. Either delete resources individually or remove the entire set of resources by deleting the resource group.