# CanvasAppsSharingApprovalWebHook Sample
Sample solution based on O365 Audit Log webhook to implement approval whenever a user shares a Canvas App.

Download and view the PowerPoint file for step by step guide in registering the webhook for O365 Audit log.
The solution file includes four Power Automate Cloud Flows and a Dataverse table.
The four flows are:
1. Audit Log List Subscribers - lists any subscribed webhooks for the Audit Log.
2. Audit Log Subscriber - subscribes the flow as a webhook for the Audit Log. 
3. Audit Log Unsubscriber - unsubscribes the flow as webhook for the Audit Log.
4. Audit Receiver - the main cloud flow to respond to the webhook from Audit Log. 
It checks for PowerAppPermissionEdited operation, and then checks if the app has been registered in the Dataverse table. 
If not, an approval is created and any sharing permission is removed automatically.
