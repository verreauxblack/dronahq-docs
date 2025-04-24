---
sidebar_position: 1
title: Trigger Data Queries 
---


import Thumbnail from '@site/src/components/Thumbnail';


The Trigger Data Query action in DronaHQ allows you to run data queries available in your application. This is especially helpful for initiating a query run and fetching data.

When a data query is set to "Run query only on manual trigger," it runs only when explicitly triggered using an action, such as a button click and more. By using the "Trigger Data Query" action, you can manually execute these queries at the right moment, ensuring better control, Avoiding Unintended Updates and enhancing Performance Optimization.



<figure>
<Thumbnail src="/img/reference/actionflow-blocks/trigger-data-query/trigger-data-query.jpg" alt="Trigger Data Query" />
<figcaption align='center'><i>Trigger Data Query</i></figcaption>
</figure>


### Understanding the TriggerDataQuery Action
With this action, you can trigger queries based on user interactions or other control actions and also can pass specific parameters. This feature is essential for creating actionflow, where user input or certain conditions initiate data queries.

### Using the TriggerDataQuery Action
1. Choose the relevant query that you wish to trigger from your data source.
2. Override Dynamic Variables Toggle - This toggle, allows you to automatically  set values for variables by enabling user to pass `custom parameters`. Query specific parameters that should be passed to the query will be auto-populated.
3. Trigger Data Query Dependencies Toggle - This toggle, when enabled, ensures that any dependent data queries are automatically re-triggered.




### Custom Parameters  

The `Custom Parameters` section allows users to pass specific values dynamically when executing a `Trigger Data Query`. These parameters take precedence over the default references defined within the data query itself, ensuring greater flexibility and control over query execution.  

#### When to Use Custom Parameters  

- Use custom parameters when you need to override default variable values in a query.  
- If a variable is `not passed` in the custom parameters section, its value will be automatically picked up from the references used within the data query section.  
- This feature is useful when executing queries based on user inputs or conditional triggers.  

:::note INFO
Custom parameters in **Trigger Data Query** allow users to pass runtime values that differ from the ones configured in the data query. If the values remain the same as those in the data query configuration, there's no need to pass anything in custom parameters—the query will automatically use the configured values.
:::

#### Defining Custom Parameters  

When specifying values in the `Custom Parameters` section, ensure proper formatting based on the data type:  

- `String values` should be wrapped in double quotes (`" "`)  
- `Numbers and objects` do not require quotes  

##### Example Custom Parameters:  

```json
{
  "id": "{{tablegrid.id}}",
  "name": "{{name}}",
  "emp_id": {{enter_emp_id}},
  "address": {{address_var}}
}
```  

##### Example Query:  

```sql
SELECT id, name, email, created_at  
FROM users  
WHERE id = "{{id}}";
```  

In this case, if `id` is provided in the custom parameters section, the query will use that value. Otherwise, it will fall back on the reference defined within the data query.

:::tip

#### Checking Available Custom Parameters

When using the Trigger Data Query action, you can view or check the available custom parameters directly within the `Data Query` section. All you have to do is go to your data query and check for its `Trigger Query from JS option` You can see the expected parameters, including their keys and data types, making it easier to pass the correct values dynamically. This ensures that the values being sent align with the expected query format.

<figure>
<Thumbnail src="/img/reference/actionflow-blocks/trigger-data-query/params.png" alt="Trigger Data Query" />
<figcaption align='center'><i>You can use the highlighted format to pass on in the custom params.</i></figcaption>
</figure>

:::

3. Use the dropdown to link the data query and adjust advanced settings as needed.

<figure>
<Thumbnail src="/img/reference/actionflow-blocks/trigger-data-query/feild.jpeg" alt="Trigger Data Query" />
<figcaption align='center'><i>Trigger Data Query</i></figcaption>
</figure>
