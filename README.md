# Course detailes

[Udemy link](https://sisense.udemy.com/course/software-architecture-design-of-modern-large-scale-systems/learn/lecture/27280376#overview)

# Section 1: Introduction

Course workbook: [PDF](Software+Architecture+and+Design+of+Large+Scale+Systems+-+Workbook.pdf)

# Section 2: System Requirements & Architectural Drivers

## 4. Feature Requirements - Step by Step Process

- UML (unified modeling language) 
- Sequence Diagram

## 5. System Quality Attributes Requirements

Consideration of quality attributes:
- Teasting and Measurability
- Trade offs (a balance achieved between two desirable but incompatible features; a compromise)
- Feasibility (the state or degree of being easily or conveniently done)

## 6. System Constraints in Software Architecture

- Technical Constraints
- Business Constraints
- Regulatory/Legal Constrains

# Section 3: Most Important Quality Attributes in Large Scale Systems

## 7. Performance

- Response time (Processing time + Waiting time) - time between sending req and receiving res
- Throughput - amount of work/data processed by our system per unit of time

Important Consideration:
- Proper measuring of response time
- Response time percentile distribution
- Performance degradation

## 8. Scalability

Load/Traffic Patterns

Vertical scalability - adding resources or upgrading existing in SINGLE machine
Horisontal scalability - adding resources or upgrading existing in DIFFERENT machines

Team/Organization scalabillity

## 9. Availability - Introduction & Measurement

Uptime - service is available to the user
Downtime - service is unavailable to the user
MTBF - Mean time between failures
MTTR - Mean time to recovery

Availability = MTBF / (MTBF + MTTR)

99,9% - is standart in the industry (3 'nines'), if 99,99% - 4 'nines'

## 10. Fault Tolerance & High Availability

Falures:
1. Human Errors
2. Software Errors
3. Hardware Falures

Fault Tolerence:
- Failure Prevemtion
- Failure Detection and Isolation
- Recovery

## 11. SLA, SLO, SLI

## 12. Real World SLA Examples from the Industry

Cloud Vendor SLA Examples
AWS Service Level Agreements (SLAs)
Google Cloud Platform Service Level Agreements
Microsoft Azure Service Level Agreement
GitHub Enterprise Service Level Agreement
Atlassian Products Service Level Agreement