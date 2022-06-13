---
sidebar_position: 6
---
**Security**
- Manage access to AWS resources and APIs using identity federation, IAM users, and IAM roles. Establish credential management policies and procedures for creating, distributing, rotating, and revoking AWS access credentials.
- Implement the least permissive rules for your security group.
- Regularly patch, update, and secure the operating system and applications on your instance.

**Storage**
- Understand the implications of the root device type for data persistence, backup, and recovery.
- Use separate Amazon EBS volumes for the operating system versus your data. Ensure that the volume with your data persists after instance termination.
- Use the instance store available for your instance to store temporary data. Remember that the data stored in instance store is deleted when you stop, hibernate, or terminate your instance. If you use instance store for database storage, ensure that you have a cluster with a replication factor that ensures fault tolerance.
- Encrypt EBS volumes and snapshots.

**Resource management**
- Use instance metadata and custom resource tags to track and identify your AWS resources.
- View your current limits for Amazon EC2. Plan to request any limit increases in advance of the time that you'll need them.

**Backup and recovery**
- Regularly back up your EBS volumes using Amazon EBS snapshots, and create an Amazon Machine Image (AMI) from your instance to save the configuration as a template for launching future instances.
- Deploy critical components of your application across multiple Availability Zones, and replicate your data appropriately.
- Design your applications to handle dynamic IP addressing when your instance restarts.
- Ensure that you are prepared to handle failover. For a basic solution, you can manually attach a network interface or Elastic IP address to a replacement instance.
- Regularly test the process of recovering your instances and Amazon EBS volumes if they fail.

**Networking**
- Set the time-to-live(TTL) value for your applications to 255, for IPv4 and IPv6. If you use a smaller value, there is a risk that the TTL will expire while application traffic is in transit, causing reachability issues for your instances.