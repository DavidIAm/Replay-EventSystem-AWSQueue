# Replay-Mongo
Amazon Web Services SNS/SQS event support for the Replay framework

We need fast and smooth event transfer for Replay to operate meaningfully.

# Capabilities Provided

## Replay::EventSystem::AWSQueue

this is the portion of the configuration of Replay that chooses to use the 
AWSQueue event system and defines the parameters used for connecting to it.  
Use the AWSQueue mode of the EventSystem and this package will be utilized.  
Include the information about what is needed to connect to your AWS
instance inside the structure

```perl
  Replay->new (
        EventSystem => {
            Mode     => 'AWSQueue',
            awsIdentity => 'MY AWS IDENTITY', 
            snsService  => 'URL OF YOUR SNS SERVICE',
            sqsService  => 'URL OF YOUR SQS SERVICE',
        },
  );
```

Honestly, its been a long time since I worked on this particular part of the
code.  I do know that it works, its live and operating in production. Bother me
have this text updated with the details of what exactly needs to be configured
to make this work.  I do remember that it is not trivial.

