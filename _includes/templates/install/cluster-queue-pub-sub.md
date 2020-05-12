{% include templates/install/queue-pub-sub-config.md %}

Configure ThingsBoard environment file:

```text
sudo nano .env
```
{: .copy-code}

Check following line:**

```.env
TB_QUEUE_TYPE=pubsub
```
{: .copy-code}

Configure Pub/Sub environment file for ThingsBoard queue service:

```text
sudo nano queue-pubsub.env
```
{: .copy-code}

Don’t forget to replace “YOUR_PROJECT_ID”, "YOUR_SERVICE_ACCOUNT" with your **real Pub/Sub project id, and service account (it is whole data from json file):**

**Note**: You should increase "REMOTE_JS_MAX_REQUEST_TIMEOUT" value due to network latency and delays for the creation of the queue instances.

```.env
TB_QUEUE_TYPE=pubsub
TB_QUEUE_PUBSUB_PROJECT_ID=YOUR_PROJECT_ID
TB_QUEUE_PUBSUB_SERVICE_ACCOUNT=YOUR_SERVICE_ACCOUNT
REMOTE_JS_MAX_REQUEST_TIMEOUT=60000
```
{: .copy-code}