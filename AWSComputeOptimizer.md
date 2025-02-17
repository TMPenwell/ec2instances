# AWS Cost Optimizer
#### [Made by Tasha Penwell with Scribe](https://scribehow.com/shared/AWS_Cost_Optimizer__Ph8y0_9QQUe0Hyhtik739A)
The AWS Cost Optimizer guide offers a valuable resource for businesses looking to enhance their cloud cost efficiency and performance. By leveraging this free service, users can receive tailored recommendations for optimizing their EC2 instances, Auto Scaling groups, and other AWS resources, ultimately reducing unnecessary expenses. The guide provides clear instructions for opting into the service and understanding the various classifications of resource utilization, enabling users to make data-driven decisions about their cloud infrastructure. Overall, this guide is essential for anyone seeking to maximize their AWS investments while maintaining optimal performance.

#### Getting Started


1\. **To opt-in to this free service, sign in to your AWS account and go to<https://docs.aws.amazon.com/compute-optimizer/latest/ug/account-opt-in.html>**

Click the **Get started** button

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/c55bcbea-a55e-4f6d-aa9a-be281f368b56/ascreenshot.jpeg?tl_px=272,214&br_px=3024,1753&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=644,277)


2\. **Computer Optimizer creates recommendations for instance types listed in the below table.**

Please go to <https://docs.aws.amazon.com/compute-optimizer/latest/ug/supported-resources.html#supported-ec2-instances> to find the most update list of supported instance types.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/0ff6451c-0a90-42fe-bc0b-7dfaa2acce33/screenshot.jpeg?tl_px=0,0&br_px=1082,559&force_format=jpeg&q=100&width=1083)


💡 Tip: Compute Optimizer does not produce EC2 rightsizing recommendations for Spot Instances.


3\. **Costs Related to Compute Optimizer**

- There is no additional charge for using Compute Optimizer.
- Recommendations for EC2 instance types and Auto Scaling provided by Compute Optimizer are free.
- You are required to pay for the compute services that you use and any CloudWatch monitoring fees.


4\. **Review the information provided as you begin the process to opt-in.**

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/53e02d33-cbfd-4e4b-887b-97b69312fab5/user_cropped_screenshot.jpeg?tl_px=0,0&br_px=3024,1890&force_format=jpeg&q=100&width=1120.0)


5\. **Compute Optimizer supports the following types of AWS accounts:**

- Standalone accounts, which do not belong to an AWS Organization.
- Member accounts that are part of an AWS Organization.
- Managed accounts within an AWS Organization.


6\.** This demo is using a standalone account, so select **Only this account** 

Click **Opt in**

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/58cf77aa-63f9-4978-b7f3-522b782dfcbf/ascreenshot.jpeg?tl_px=0,0&br_px=3024,1890&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=1034,608)


7\. **AWS Compute Optimizer is a service that operates regionally but it provides a unified console experience for analyzing resources across multiple AWS regions.** 

This is why you will see your region now set to *Global*.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/e2b99784-2f58-4cea-9f91-a9aa9991c8a4/ascreenshot.jpeg?tl_px=272,0&br_px=3024,1538&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=893,80)


8\. **In the menu on the left side, you see options that provide *Recommendations*.**

These recommendations include 

- EC2 Instances 
- EC3 Auto Scaling groups
- EBS Volumes
- Lambda functions
- RDS databases
- ECS services on Fargate

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/3a951df3-5403-432c-b2ba-b7f9d9256940/user_cropped_screenshot.jpeg?tl_px=0,0&br_px=3024,1890&force_format=jpeg&q=100&width=1120.0)


#### Result Classifications


9\. **Classifications**

**Compute Optimizer categorizes findings into four main classifications:**

### 1. Under Provisioned

- **Definition**: At least one specification (CPU, memory, or network) does not meet the performance requirements.
- **Impact**: This can result in poor performance.

### 2. Over Provisioned

- **Definition**: At least one specification (CPU, memory, or network) can be reduced in size while still meeting performance requirements.
- **Criteria**: This classification is only applied if *no specification* is under provisioned.
- **Impact**: May result in unnecessary costs.

### 3. Optimized

- **Definition**: All specifications (CPU, memory, and network) meet the workload's performance requirements and are not over provisioned.

### 4. None

- **Definition**: No recommendations are available.
- **Possible Reasons**:
  - The service was opted into for 12 hours or less.
  - The instance has been running for less than 30 hours.
  - The instance type is not supported by Compute Optimizer.


#### Reviewing Recommendations


10\. **Recommendations for EC2 Instances**

This page provides a list of your current EC2 instances with the top recommendation options generated by Compute Optimizer.

This demo shows no recommendations. Recall this could be due to any of the following:

- The service was opted into for 12 hours or less.
- The instance has been running for less than 30 hours.
- The instance type is not supported by Compute Optimizer.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/6a595670-7848-43ff-b4b9-bc41f5033709/user_cropped_screenshot.jpeg?tl_px=0,208&br_px=2752,1747&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=43,277)


💡 Tip: If an EC2 instance is not listed at <https://docs.aws.amazon.com/compute-optimizer/latest/ug/supported-resources.html#supported-ec2-instances> it is not supported.


11\. **EC2 Auto Scaling Groups**

This page lists your current EC2 Auto Scaling groups with the top recommendation options generated by Compute Optimizer.

This demo shows no recommendations. Recall this could be due to any of the following:

- The service was opted into for 12 hours or less.
- The instance has been running for less than 30 hours.
- The instance type is not supported by Compute Optimizer.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/b2235af4-55bb-4100-949b-9c0d88809433/user_cropped_screenshot.jpeg?tl_px=0,0&br_px=3024,1890&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=37,348)


12\. **Compute Optimizer creates recommendations for Amazon EC2 Auto Scaling groups. It supports groups Auto Scaling groups that have the following

- Single EC2 instance types
- Mixed EC2 instance types
- One or multiple scaling policies based on CPU utilization
  - target tracking
  - predictive scaling
  - simple scaling
  - step scaling
- Scheduled scaling policies
- No scaling policy**


13\. **EBS Volumes**

This table lists the current volumes with their top recommendation options that you can use to improve workload performance and reduce cost.

New volumes are not analyzed until they have enough recent metric history. At least 30 hours of CloudWatch metric data is needed for Compute Optimizer to analyze the utilization and provide the recommendations.

This demo shows no recommendations. Recall this could be due to any of the following:

- The service was opted into for 12 hours or less.
- The instance has been running for less than 30 hours.
- The instance type is not supported by Compute Optimizer.

###

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/889e1de4-83af-4fd9-a408-b62ed2a3c1ad/user_cropped_screenshot.jpeg?tl_px=0,0&br_px=3024,1890&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=38,372)


14\. **Compute Optimizer supports recommendations for the following EBS volume types that are attached to an instance**

- HDD st1 and sc1
- General Purpose SSD gp2 and gp3
- Provisioned IOPS SSD io1, io2, and io2 Block Express


Tip: Compute Optimizer also makes recommendation to move data from previous generation volumes (such as HDD Magnetic).


15\. **Lambda Functions**

This table lists the configuration of current Lambda functions, along with their top recommended memory configurations generated by Compute Optimizer.

This demo shows no recommendations. Recall this could be due to any of the following:

- The service was opted into for 12 hours or less.
- The instance has been running for less than 30 hours.
- The instance type is not supported by Compute Optimizer.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/f377b3ed-bdf4-4648-80c3-200c98adb897/user_cropped_screenshot.jpeg?tl_px=0,351&br_px=2752,1890&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=43,295)


16\. **RDS Databases**

This page lists your current RDS instances and Compute Optimizer findings and recommendation options.

This demo shows no recommendations. Recall this could be due to any of the following:

- The service was opted into for 12 hours or less.
- The instance has been running for less than 30 hours.
- The instance type is not supported by Compute Optimizer.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/1414230b-b95f-4b62-8dbd-7410a5fcc700/user_cropped_screenshot.jpeg?tl_px=0,0&br_px=3024,1890&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=34,415)


17\. **Compute Optimizer supports recommendations for the following**

**Database Engines**

- RDS for MySQL
- RDS for PostgresSQL
- Aurora MySQL-Compatible
- Aurora PostgresSQL-Compatible

**Database Instance Storage**

- General Purpose SSD gp2 and gp3
- Provisioned IOPS SSD io1


18\. **The below RDS instance types are supported.  Please refer to <https://docs.aws.amazon.com/compute-optimizer/latest/ug/supported-resources.html#supported-ec2-instances> for the current full list.**

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/3b6721c7-8b46-47ae-8e4c-0a73a66d85b4/screenshot.jpeg?tl_px=0,0&br_px=1072,484&force_format=jpeg&q=100)


19\. **The below Amazon Aurora instance types are supported.  Please refer to <https://docs.aws.amazon.com/compute-optimizer/latest/ug/supported-resources.html#supported-ec2-instances> for the full and current list**

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/bb609c97-54a9-4e68-b436-c4745bf7791f/screenshot.jpeg?tl_px=0,0&br_px=1072,524&force_format=jpeg&q=100)


20\. **ECS Services on Fargate**

This page lists your current Amazon ECS services on Fargate with Compute Optimizer’s findings and recommendation options.

This demo shows no recommendations. Recall this could be due to any of the following:

- The service was opted into for 12 hours or less.
- The instance has been running for less than 30 hours.
- The instance type is not supported by Compute Optimizer.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2025-02-17/6c3b2526-1aaf-477f-adaa-97bc186b8893/user_cropped_screenshot.jpeg?tl_px=0,351&br_px=2752,1890&force_format=jpeg&q=100&width=1120.0&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=34,344)


21\. **When evaluating EC2 instance recommendations, follow this structured approach to ensure optimal performance and cost efficiency:**

### Data Analysis

- **Historical Data Review**:
  - Recommendations are generated based on the analysis of data from the past 14 days.
  - Note: These recommendations do not account for future needs or anticipated changes.
- **Metric Evaluation**:
  - Examine graphed metrics to determine if actual usage is consistently lower than the instance's capacity.
  - Utilize CloudWatch to view detailed metrics such as average, peak, and percentiles. Assess whether CPU usage varies throughout the day and if peak times need accommodation.

### Burstable Performance Instances

- **Definition**: Burstable performance instances are EC2 instances that provide a baseline level of CPU performance with the ability to burst above the baseline when needed. They are designed to handle occasional spikes in load.
- For instances with burstable performance capabilities:
  - If the instance periodically exceeds its baseline performance, ensure that it can continue to do so with the virtual CPUs (vCPUs) of any new instance type you consider.

### Cost and Compatibility Considerations

- **Reserved Instances**:
  - Analyze the impact on any Reserved Instance options you might be using before committing to changes.
- **Instance Generation and Compatibility**:
  - Whenever possible, consider upgrading to newer instance generations to enhance performance and efficiency.
  - When migrating to a different instance family, ensure compatibility in virtualization, architecture, and network configurations between the current and new instance types.

### Risk Assessment and Testing

- **Risk Rating**:
  - Review the risk rating provided with each recommendation. This indicates the level of effort required to validate the recommendations properly.
- **Testing**:
  - Conduct load and performance testing both before and after implementing any changes to verify improvements and avoid potential issues.

By adhering to these guidelines, you can make informed decisions that align with your performance goals and budgetary constraints.
#### [Made with Scribe](https://scribehow.com/shared/AWS_Cost_Optimizer__Ph8y0_9QQUe0Hyhtik739A)


