# ce10-2-14-assignment
Assignment 2.14

Answer the following:

1. Does SNS guarantee exactly once delivery to subscribers?

No, a message is delivered at least once, and occationally more than once.


2. What is the purpose of the Dead-letter Queue (DLQ)? This is a feature available to SQS/SNS/EventBridge.

It is a queue to hold messages which the consumer failed to process after the set number of retries.


3. How would you enable a notification to your email when messages are added to the DLQ?

Create a SNS topic and subscribe to that topic using the email. Then create a EventBridge rule with the source being the DLQ and the target being the SNS topic. 
