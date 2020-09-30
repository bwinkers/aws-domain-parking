# aws-domain-parking

Code to make domain parking at AWS easier.

## Create a root S3 bucket

We only need a single S3 bucket with web hosting enabled, our `website_bucket`. 
We export a `website_bucket` variable in Cloudformation that can be accessed by other stacks and scripts.

## Add a Site

A site represents a specific set of files and content. It is represented by a directory in the `website_bucket`.
Multiple site may serve the same market and be able to use the same content to reduce management effort.

## Add a domain to a Site

A site needs at least one domain hostname assigned to it to receive any traffic.
