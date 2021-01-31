### Simple simplified use case of an IBOR solution
The scenario is as below:
* Each time an event (transaction) is received both cash and asset positions will be impacted
* Value will be added/subtracted to/from cash position for each event
* Value will be added/subtracted to/from asset position for each event
* Portfolio will be valuated for each event
<br> ibor-transactions notebook contains the code to connect to the Azure Event Hub and consume the events
<br> Program.cs is a simple code to send message to the Azure Event Hub created
<br> Ibor-transactions.json is a fie example sent to the Azure Event Hub

<br>Here are the steps to follow:
* Setup Azure event hubs and Azure Databricks with this article [Azure Event Hub Azure Databrick](https://medium.com/@tiwesley/azure-event-hubs-azure-databricks-2e3dc5389b0d)
* Run the notebook except the last step that stops the stream
* Execute Program.cs to send event(s) (make sure to update the file with the file path used to send an event and also the connection string key of your Azure Event Hub)
* Run the cell (the one before stoping the stream) to vizualise how the portfolio valuation is updated

<br> References
<br>[Microsoft Azure Event Hub](https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-dotnet-standard-getstarted-send)
<br>[Databricks Azure Event Hub](https://docs.databricks.com/spark/latest/structured-streaming/streaming-event-hubs.html)
