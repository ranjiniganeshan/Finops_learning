
# Finops Best practise

1. Optimize your x86-based Amazon EC2 Workloads

* Running your x86 EC2 workloads on AMD-based EC2 instances to achieve at least 10% cost savings.

Usecase 1: https://aws.amazon.com/blogs/big-data/increase-amazon-elasticsearch-service-performance-by-upgrading-to-graviton2/


Comments: ELK 7.9 existing datanodes and master is moved from x86 processor to graviton. This helps in increase in performance and reduce the cost by 10%.

Benefits of moving x86 to graviton processor


* You can enjoy up to 38% improvement in indexing throughput compared to the corresponding x86-based counterparts
* The Graviton2 instance family provides up to 50% reduction in indexing latency, and up to 30% improvement in query performance when compared to the current generation (M5, C5, R5)
* Amazon OpenSearch Service Graviton2 instances provide up to 44% price/performance improvement over previous generation instances
* Graviton2 instances include support for all recently launched features like encryption at rest and in flight, role-based access control, cross-cluster search, Auto-Tune, Trace Analytics, Kibana Reporting, and UltraWarm


![Screen Shot 2023-06-15 at 3 59 39 PM](https://github.com/ranjiniganeshan/Finops_learning/assets/32661402/5600a7c3-90b7-4c0a-952b-b01a53cfbbcb)


2. Besides saving on the instance type alone, compute savings can be even greater 

* **Amazon EC2 Reserved Instances** provide a significant discount (up to 72%) compared to On-Demand pricing and provide a capacity reservation when used in a specific Availability zone. Amazon EC2 Savings Plans provide savings up to 72% in exchange for commitment to usage of individual instance families in a Region. This automatically reduces your cost on the selected instance family in that region regardless of Availability Zone, Operating System, or tenancy type. Compute Savings plans provide the most flexibility and help to reduce your costs by up to 66%. These plans automatically apply to EC2 instance usage regardless of instance family, size, Availability Zone, Region, Operating System or tenancy, and also apply to Fargate or Lambda usage

* **Amazon EC2 Spot instances** let you take advantage of unused EC2 capacity in the AWS cloud. Spot Instances are available at up to a 90% discount compare to On-Demand prices. You can use Spot instances for various stateless, fault-tolerant, or flexible applications such as big data, containerized workloads, CI/CD, web servers and more.

* If your organization has EC2 workloads that require an x86 based CPU, they can be run on AMD-powered Amazon EC2 instances and achieve 10% cost savings compared with other x86 based EC2 instances. Running compute workloads on AMD based instances is a great way to recognize short-term savings, as your organization creates a migration path to run their applications on arm64 based Graviton-based EC2 instances. If your organization determines that AMD instances should be required for new and current workloads, you can implement guardrails through AWS Service Catalog. Last, by leveraging Amazon EC2 Reserved Instances, Amazon EC2 Savings Plans or Amazon Compute Savings Plans, your organization can achieve even larger savings on their Amazon EC2 compute workloads.

2. Empower your engineers to take an active role in cost optimization

* Build trust and partnership between CFM(cloud finacial management and Engineering teams
 
 The CFM team understand the pain points of Engineering, and which optimization measures are low hanging fruit vs. longer term projects. Additionally, Engineering can provide guidance on optimization efforts that may negatively impact performance or customer experience. By doing this, Engineering can gain insights into data analysis and overall cloud cost management processes. This creates a vital and collaborative feedback loop and cost optimization recommendations process.
 
 * Enable teams with cost management tools and data

Engineering teams can lack visibility into ongoing cloud costs consumption of their respective applications. It is unrealistic to expect them to act on something they cannot see. We recommend building AWS Cost and Usage Reports (CUR) dashboards using tools like AWS Cost Explorer (CE) or the AWS Cloud Intelligence Dashboard (CID). This will give all relevant stakeholders access to near-real time data, and ultimately increase accountability through the proper cost allocation models. The purpose of the dashboards should be showback, not shameback. These dashboards must be simple, so that users can access the data they care about quickly, and at the right level of granularity. With this data, engineering teams will be better equipped to do dive deep analyses like determining usage patterns, finding top AWS resource spend, or performing root cause analysis of a cost anomaly. They’ll also be able to make more timely and informed decisions related to architectural changes and cost optimization.


 ![Screen Shot 2023-06-15 at 5 12 13 PM](https://github.com/ranjiniganeshan/Finops_learning/assets/32661402/515263db-7009-4b8f-99ca-93b8d735b720)

 
 



