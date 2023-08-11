# Module 7: Key Vault

## Task

The source code is available [here](../../../petstore).

Azure Key Vault is a service that offers centralized secrets management, granting comprehensive control over access policies and audit history. In this module, you will practice working with secrets from Azure Key Vault in your App Service or Azure Function application, all without necessitating any code alterations.

**Please complete the following task:**

1. Create a Key Vault instance.
2. Store the Azure Database for PostgreSQL connection string as a secret in the Key Vault.
3. Enable managed identity for the App Service.
4. Create a Key Vault access policy for the App Service managed identity.
5. Obtain the unique secret URI associated with the stored database connection string.
6. Update App Service's application settings to include the Azure Key Vault reference syntax.
7. Reference the stored secret URI in your app's settings to securely access the database connection string.

**Definition of Done:**

1. Database credentials are not stored in configuration files or code.
2. A Key Vault is created with a secret value assigned to the database connection string.
3. Managed identity is enabled for the App Service.
4. A Key Vault access policy is created with the correct permissions for the App Service managed identity.
5. A new setting is added to the App Service's application settings, referencing the Key Vault secret using it unique URL.
6. The App Service successfully utilizes the configuration setting that directs it to the Key Vault secret.

<img src="images/scheme.png" width="550" style="margin: 20px 0; display: inline-block;"/>

<div style="border: 1px solid #ccc; background-color: #eee;">
  <ul>
    <li>When presenting the results of the practical tasks, please <a href="../common/presenting-results/presenting-results.md">follow these guidelines</a>.</li>
    <li>When you have completed the task, attach the screenshot to the "Result" field, and update the status to "Done."</li>
    <li>Delete resources.</li>
  </ul>
</div>
<hr>

>**IMPORTANT:** Leaving resources running can result in additional costs. Either delete resources individually or remove the entire set of resources by deleting the resource group.