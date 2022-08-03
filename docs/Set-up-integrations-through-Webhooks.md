---
stoplight-id: 19cudwq6kznwf
---

# Overview

Amplify webhooks apply to Unified Catalog API Subscription requests, Marketplace Product Subscription requests and Integration Resource Webhooks.

This API defines a webhook api for all.

* Refer to this [online doc](https://docs.axway.com/bundle/amplify-central/page/docs/integrate_with_central/integrate_with_webhooks/index.html) for details on Amplify webhooks.
* Refer to this [online doc](https://docs.axway.com/bundle/amplify-central/page/docs/integrate_with_central/webhook/marketplace_subscription_webhook/index.html) for details on Marketplace Product Subscription webhooks.
* Refer to this [online doc](https://docs.axway.com/bundle/amplify-central/page/docs/integrate_with_central/webhook/unified_catalog_webhook/index.html) for details on Unified Catalog Subscription webhooks.

The general form of a webhook is shown below (example of a Marketplace Product Subscription webhook payload):

```
{
  "id": "4d2bbd32-6f....37",
  "time": "2022-06-20T11:30:28.133+0000",
  "version": "v1",
  "product": "AmplifyCentral",
  "correlationId": "f0a1d4ef-d5a.......9",
  "organization": {
    "id": "org id number"
  },
  "type": "SubResourceUpdated",
  "payload": {
   "metadata": {
      ........
      ........
      ........
      "selfLink": "/catalog/v1alpha1/subscriptions/subscription-name-goes-here"
    },
    "marketplace": {
      "resource": {
        "owner": {
          "id": "e4e0.....8",
          "type": "team",
          "organization": {
            "id": "org id number"
          }
        }
      }
    },
    "kind": "Subscription",
    "approval": {
      "state": "pending"
    },
    "title": "*** DISPLAY NAME ***",
    "spec": {
      "plan": {
        "name": "*** PLAN NAME ***"
      },
      "product": "*** PRODUCT NAME ***"
    },
    "apiVersion": "v1alpha1",
    "name": "*** SUBSCRIPTION NAME ***",
    "group": "catalog",
    "status": {
      "level": "Success"
    }
  },
  "metadata": {
    "subresource": "approval"
  }
}
```