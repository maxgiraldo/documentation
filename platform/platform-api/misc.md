# Frequently Asked Questions

## Querying: How do I get a list of conversations or messages?

Layer provides a number of similar looking but fundamentally distinct services.  All of these are built on top of Layer's Messaging Service, which provides a Cassandra database of events that can handle the great volume and performance needed to handle large scale messaging applications.  Neither Cassandra, nor event streams allow for the kinds of querys that customers would need from the Platform API.

The following alternatives are being worked on, but are not yet available:

1. The REST API: The REST API is able to expose a Query API for a specific authenticated user.  It does this by listening to the Messaging Service for events relevant to that user and inserting it into its local queryable database.
2. The Webhooks: Calls your server with events from the Messaging Service
3. Insights: Allows for querying of Messages and Conversations that were recently active only.

