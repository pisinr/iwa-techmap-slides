# Serverless

---

* Amazon Lambda
* Google Cloud Function
* Azure Functions
* Kubeless

---

# It's a glorified CGI

* You provide codes.
* The provider spin a server to response to event
  * May be a HTTP request?
  * May be a push notification?
  * May be email?
* It may never run.

^^^

* No state, no persistence.
* Utilize their platform as much as possible
  * S3, DynamoDB, SES, ElasticEncoder
* Happy being locked in to a platform.

