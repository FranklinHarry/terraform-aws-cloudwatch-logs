<!-- This file was automatically generated by the `build-harness`. Make all changes to `README.yaml` and run `make readme` to rebuild this file. -->

[![Cloud Posse](https://cloudposse.com/logo-300x69.svg)](https://cloudposse.com)

# terraform-aws-cloudwatch-logs [![Build Status](https://travis-ci.org/cloudposse/terraform-aws-cloudwatch-logs.svg?branch=master)](https://travis-ci.org/cloudposse/terraform-aws-cloudwatch-logs) [![Latest Release](https://img.shields.io/github/release/cloudposse/terraform-aws-cloudwatch-logs.svg)](https://github.com/cloudposse/terraform-aws-cloudwatch-logs/releases/latest) [![Slack Community](https://slack.cloudposse.com/badge.svg)](https://slack.cloudposse.com)


Terraform module for creation of CloudWatch Log Streams and Log Groups for use with Fluentd.


---

This project is part of our comprehensive ["SweetOps"](https://docs.cloudposse.com) approach towards DevOps. 


It's 100% Open Source and licensed under the [APACHE2](LICENSE).










## Usage

```terraform
module "cloudwatch_log" {
  namespace    = "${var.namespace}"
  stage        = "${var.stage}"
  stream_names = ["kafka-instance-1", "kafka-instance-2"]
}
```






## Makefile Targets
```
Available targets:

  help                                This help screen
  help/all                            Display help for all targets
  lint                                Lint terraform code

```

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| additional_permissions | Additional permissions granted to assumed role | list | `<list>` | no |
| attributes | Additional attributes (e.g. `policy` or `role`) | list | `<list>` | no |
| delimiter | Delimiter to be used between `name`, `namespace`, `stage`, etc. | string | `-` | no |
| name | Name  (e.g. `bastion` or `db`) | string | `` | no |
| namespace | Namespace (e.g. `cp` or `cloudposse`) | string | - | yes |
| retention_in_days | Number of days you want to retain log events in the log group | string | `30` | no |
| stage | Stage (e.g. `prod`, `dev`, `staging`) | string | - | yes |
| stream_names | Names of streams | list | `<list>` | no |
| tags | Additional tags (e.g. map(`BusinessUnit`,`XYZ`) | map | `<map>` | no |
| trusted_roles | Roles allow to assume role | list | `<list>` | no |

## Outputs

| Name | Description |
|------|-------------|
| assumed_role_arn | ARN of role to assume |
| assumed_role_name | Name of role to assume |
| log_group_arn | ARN of the log group |
| log_group_name | Name of log group |
| policy_arn | ARN of role to assume |
| policy_name | Name of role to assume |
| stream_arns | ARN of the log stream |




## Related Projects

Check out these related projects.

- [terraform-aws-cloudwatch-flow-logs](https://github.com/cloudposse/terraform-aws-cloudwatch-flow-logs) - Terraform module for enabling flow logs for vpc and subnets.
- [terraform-aws-ecs-web-app](https://github.com/cloudposse/terraform-aws-ecs-web-app) - Terraform module that implements a web app on ECS and supporting AWS resources.
- [terraform-aws-cloudtrail-cloudwatch-alarms](https://github.com/cloudposse/terraform-aws-cloudtrail-cloudwatch-alarms) - Terraform module for creating alarms for tracking important changes and occurances from cloudtrail.
- [prometheus-to-cloudwatch](https://github.com/cloudposse/prometheus-to-cloudwatch) - Utility for scraping Prometheus metrics from a Prometheus client endpoint and publishing them to CloudWatch
- [terraform-aws-cloudwatch-logs](https://github.com/cloudposse/terraform-aws-cloudwatch-logs) - Terraform Module to Provide a CloudWatch Logs Endpoint
- [terraform-aws-efs-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-efs-cloudwatch-sns-alarms) - Terraform module that configures CloudWatch SNS alerts for EFS
- [terraform-aws-ecs-cloudwatch-autoscaling](https://github.com/cloudposse/terraform-aws-ecs-cloudwatch-autoscaling) - Terraform module to autoscale ECS Service based on CloudWatch metrics
- [terraform-aws-ecs-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-ecs-cloudwatch-sns-alarms) - Terraform module to create CloudWatch Alarms on ECS Service level metrics.
- [terraform-aws-sqs-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-sqs-cloudwatch-sns-alarms) - Terraform module for creating alarms for SQS and notifying endpoints
- [terraform-aws-elasticache-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-elasticache-cloudwatch-sns-alarms) - Terraform module that configures CloudWatch SNS alerts for ElastiCache
- [terraform-aws-ec2-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-ec2-cloudwatch-sns-alarms) - Terraform module that configures CloudWatch SNS alerts for EC2 instances
- [terraform-aws-rds-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-rds-cloudwatch-sns-alarms) - Terraform module that configures important RDS alerts using CloudWatch and sends them to an SNS topic
- [terraform-aws-lambda-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-lambda-cloudwatch-sns-alarms) - Terraform module for creating a set of Lambda alarms and outputting to an endpoint
- [terraform-aws-alb-target-group-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-alb-target-group-cloudwatch-sns-alarms) - Terraform module to create CloudWatch Alarms on ALB Target level metrics.
- [terraform-aws-sns-lambda-notify-slack](https://github.com/cloudposse/terraform-aws-sns-lambda-notify-slack) - Terraform module to provision a lambda function that subscribes to SNS and notifies to Slack.



## Help

**Got a question?**

File a GitHub [issue](https://github.com/cloudposse/terraform-aws-cloudwatch-logs/issues), send us an [email][email] or join our [Slack Community][slack].

## Commercial Support

Work directly with our team of DevOps experts via email, slack, and video conferencing. 

We provide [*commercial support*][commercial_support] for all of our [Open Source][github] projects. As a *Dedicated Support* customer, you have access to our team of subject matter experts at a fraction of the cost of a full-time engineer. 

[![E-Mail](https://img.shields.io/badge/email-hello@cloudposse.com-blue.svg)](mailto:hello@cloudposse.com)

- **Questions.** We'll use a Shared Slack channel between your team and ours.
- **Troubleshooting.** We'll help you triage why things aren't working.
- **Code Reviews.** We'll review your Pull Requests and provide constructive feedback.
- **Bug Fixes.** We'll rapidly work to fix any bugs in our projects.
- **Build New Terraform Modules.** We'll develop original modules to provision infrastructure.
- **Cloud Architecture.** We'll assist with your cloud strategy and design.
- **Implementation.** We'll provide hands-on support to implement our reference architectures. 


## Community Forum

Get access to our [Open Source Community Forum][slack] on Slack. It's **FREE** to join for everyone! Our "SweetOps" community is where you get to talk with others who share a similar vision for how to rollout and manage infrastructure. This is the best place to talk shop, ask questions, solicit feedback, and work together as a community to build *sweet* infrastructure.

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/cloudposse/terraform-aws-cloudwatch-logs/issues) to report any bugs or file feature requests.

### Developing

If you are interested in being a contributor and want to get involved in developing this project or [help out](https://github.com/orgs/cloudposse/projects/3) with our other projects, we would love to hear from you! Shoot us an [email](mailto:hello@cloudposse.com).

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull Request** so that we can review your changes

**NOTE:** Be sure to merge the latest changes from "upstream" before making a pull request!


## Copyright

Copyright © 2017-2018 [Cloud Posse, LLC](https://cloudposse.com)



## License 

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) 

See [LICENSE](LICENSE) for full details.

    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.









## Trademarks

All other trademarks referenced herein are the property of their respective owners.

## About

This project is maintained and funded by [Cloud Posse, LLC][website]. Like it? Please let us know at <hello@cloudposse.com>

[![Cloud Posse](https://cloudposse.com/logo-300x69.svg)](https://cloudposse.com)

We're a [DevOps Professional Services][hire] company based in Los Angeles, CA. We love [Open Source Software](https://github.com/cloudposse/)!

We offer paid support on all of our projects.  

Check out [our other projects][github], [apply for a job][jobs], or [hire us][hire] to help with your cloud strategy and implementation.

  [docs]: https://docs.cloudposse.com/
  [website]: https://cloudposse.com/
  [github]: https://github.com/cloudposse/
  [commercial_support]: https://github.com/orgs/cloudposse/projects
  [jobs]: https://cloudposse.com/jobs/
  [hire]: https://cloudposse.com/contact/
  [slack]: https://slack.cloudposse.com/
  [linkedin]: https://www.linkedin.com/company/cloudposse
  [twitter]: https://twitter.com/cloudposse/
  [email]: mailto:hello@cloudposse.com


### Contributors

|  [![Igor Rodionov][goruha_avatar]][goruha_homepage]<br/>[Igor Rodionov][goruha_homepage] | [![Vladimir][SweetOps_avatar]][SweetOps_homepage]<br/>[Vladimir][SweetOps_homepage] |
|---|---|

  [goruha_homepage]: https://github.com/goruha
  [goruha_avatar]: https://github.com/goruha.png?size=150
  [SweetOps_homepage]: https://github.com/SweetOps
  [SweetOps_avatar]: https://github.com/SweetOps.png?size=150


