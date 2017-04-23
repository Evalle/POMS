# POMS
The main ideas from the ["Principles of Microservices"](http://shop.oreilly.com/product/0636920043935.do) course

## Contents
[introduction](#introduction)  

### Introduction
The Microservices (M) are small, **autonomous** services that work together
*Small* here means that they're doing one thing well. 
The Microservices are just one of the implementations of Service Oriented Architecture (SOA)

## Advantages of M:
 - better allignment with the organization
 - ship faster
 - independent scaling
 - enable segregation models
 - adopt technologies more easily (you can use different languages/technologies for each M.)
 
## Disadvantages of M:
  - lots of options (can be as the Advantage or the Disadvantage)
  - it takes a lot of time to get into M. 
  - testing of M. is more complex 
  - monitoring and investigation of failures is more complex
  - resiliency isn't free
  - disrtibutes systems are hard! - with Monolith you have a binary state - it's up or down, with M. some of your services can be down,
  another - up and running.
  
## Principles of M:
  1. Modelled around business domain
  2. Culture of automation
  3. Hide implementation details
  4. Decentralise all the things
  5. Deploy independently
  6. Consumer first
  7. Isolate failure
  8. Highly observable

## 1. Modelled around Business Domain
[Presentation] -> [Business Logic] -> [Data Access] - jst a simple example.

## 2. Culture of automation
- Continous Delivery (build -> test -> UAT -> prod)
- API - driven machine provisioning (creating a new node via API), see AWS, DO, OpenStack, Vagrant, etc
- API - driven OS configurationm, see Chef, Puppet, Ansible 
- Custom image creation, see Packer
- 
  
 


