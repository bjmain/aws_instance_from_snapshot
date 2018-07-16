# aws_instance_from_snapshot

This protocol assumes you have a snapshot that you want to launch as an instance.

1. Create a volume from the snapshot.
2. Launch an EC2 instance in the same region as the volume from step 1. Then STOP it.
3. Find and copy the root volume ID (typcially 8Gb) by clicking on the root device path: /dev/sda1
4. Force detach the root volume: Search in volumes then force detach.
5. Attach the snapshot volume: paste new instance ID and device path (/dev/sda1).
6. Start instance
