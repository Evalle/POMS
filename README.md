# POMS
The main ideas from the ["Principles of Microservices"](http://shop.oreilly.com/product/0636920043935.do) course

## Table of Contents
1. [Introduction](#introduction)  
2. [Advantages of Microservices](#advantages-of-m)
3. [Disadvantages of Microservices](#disadvantages-of-m)
4. [Principles of Microservices](#principles-of-m)
   - [Modelled around Business Domain](#modelled-around-business-domain)
   - [Culture of automation](#culture-of-automation)
   - [Hide implementation details](#hide-implementation-details)
   - [Decentralise all the things](#decentralise-all-the-things)
   - [Deploy independently](#deploy-independently)
   - [Consumer first](#consumer-first)
   - [Isolate failures](#isolate-failures)
   - [Highly observable](#highly-observable)
5. [When YOU should use Microservices](#when-you-should-use-m)
6. [Useful Books](#useful-books)

### Introduction
The Microservices (M) are small, **autonomous** services that work together
*Small* here means that they're doing one thing well. 
The Microservices are just one of the implementations of Service Oriented Architecture (SOA)

### Advantages of M
 - better allignment with the organization
 - ship faster
 - independent scaling
 - enable segregation models
 - adopt technologies more easily (you can use different languages/technologies for each M.)
 
### Disadvantages of M
  - lots of options (can be as the Advantage or the Disadvantage)
  - it takes a lot of time to get into M. 
  - testing of M. is more complex 
  - monitoring and investigation of failures is more complex
  - resiliency isn't free
  - disrtibutes systems are hard! - with Monolith you have a binary state - it's up or down, with M. some of your services can be down,
  another - up and running.
  
### Principles of M
  1. Modelled around business domain
  2. Culture of automation
  3. Hide implementation details
  4. Decentralise all the things
  5. Deploy independently
  6. Consumer first
  7. Isolate failure
  8. Highly observable

### Modelled around Business Domain
[Presentation] -> [Business Logic] -> [Data Access] - jst a simple example.

### Culture of Automation
- Continous Delivery (build -> test -> UAT -> prod)
- API - driven machine provisioning (creating a new node via API), see AWS, DO, OpenStack, Vagrant, etc
- API - driven OS configurationm, see [Chef](https://www.chef.io/chef/), [Puppet](https://puppet.com/), [Ansible](https://www.ansible.com/) 
- Custom image creation, see [Packer](https://www.packer.io/)
- Declarative environment provisioning, see [Docker Compose](https://docs.docker.com/compose/), [Terraform](https://www.terraform.io/)
- Automatic testing

### Hide implementation Details
- Hide your DB!
- Think about protocols: YAML. JSON, XML, SOAP
- Be careful of client libraries

### Decentralise all the things
- internal open source model, see [Gitlab](https://about.gitlab.com/)
- orchestration
- self-service
- owner operator (each team is the main operator of their piece of software)

### Deploy Independently
- One service per OS/VM/Container
- Consumer-driven contracts, see [Pact](https://docs.pact.io/)
- Co-existing service versions
- Multiple enpoints (e.g. another API version of the same service)

### Consumer First
- Conversations
- Consumer-driven contracts, see [Pact](https://docs.pact.io/)
- Standards, see [PayPal API standards for example](https://github.com/paypal/api-standards/blob/master/api-style-guide.md)
- API documentation, see [Swagger](http://swagger.io/)
- Service Discovery, see [Consul](https://www.consul.io/), [etcd](https://coreos.com/etcd/docs/latest/), DNS

### Isolate Failures
- M. aren't reliable by default
- Cascading failures can hurt
- Timeouts

### Highly Observable
- Standrad monitoring
- Service monitoring, see [docker stats](https://docs.docker.com/engine/reference/commandline/stats/), [collectd](https://collectd.org/)
- Health check pages
- Log aggregation, see [Logstash](https://www.elastic.co/products/logstash), [fluentd](http://www.fluentd.org/), [kibana](https://www.elastic.co/products/kibana) 
- State aggregation, see [Graphite](https://graphiteapp.org/)
- Semantic monitoring (for example try to mock user actions each 5 minutes)
- Correlation ID (every action with ID, so you can catch it on every M. logs by this ID)

### When YOU should use M
- What are you looking for?
- What kind of problem from the M. advantages are you trying to solve?

### Useful Books
1. 




