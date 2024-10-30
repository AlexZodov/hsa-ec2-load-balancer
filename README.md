# hsa-ec2-load-balancer

# Task
Create 2 micro instances in AWS.

Setup application load balancer and assign instances to it.

# Solution
1. Created 2 EC2 instances and configured each with nginx server serving `/images/*` to internet (2 different files with same name created on them)
   1. ![](./proofs/two_ec2_instances_created.png)
   2. ![](./proofs/both_images_accessible.png)
2. Create target group 
   1. ![](./proofs/target_group_config.png)
3. Create load balancer (ALB) and configured it to use target group created earlier
   1. ![](./proofs/alb_created.png)
4. After heading to ALB external address and requesting resource filename existing on each instance
   1. ![](./proofs/image_via_alb_1.png)
   2. ![](./proofs/image_via_alb_2.png)