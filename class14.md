# Day 14 - Cloud Network Traffic Analysis
10/22/20

* [What is Traffic Mirroring?](https://docs.aws.amazon.com/vpc/latest/mirroring/vpc-tm.pdf#traffic-mirroring-how-it-works)

"Traffic Mirroring is an Amazon VPC feature that you can use to copy network traffic from an elastic
network interface of Amazon EC2 instances. You can then send the traffic to out-of-band security and
monitoring appliances for:
* Content inspection
* Threat monitoring
* Troubleshooting"

### Key concepts for Traffic Mirroring:
* **Target** — The destination for mirrored traffic.
* **Filter** — A set of rules that defines the traffic that is copied in a traffic mirror session.
* **Session** — An entity that describes Traffic Mirroring from a source to a target using filters.

You can use: 
* AWS Management Console
* AWS Command Line Interface (AWS CLI)
* AWS SDKs
* Query API

Benefits:
* Simplified operation
* Enhanced security
* Increased monitoring options