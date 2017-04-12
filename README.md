# EC2 Starter

### setup_instance

the `setup_instance` script has the following options:

```bash
eakl@hostname:~/ec2-starter $ ./setup_instance
usage: setup_instance <command>

commands:
   --help                            Get help

   --defaults                        Apply default options

   --name <text>                     Name of VPC and Instance (eakl)
   --region <type>                   Region of the VPC and Instance (eu-west-1)
   --instance-type <type>            Instance type (t2.micro)
   --image-id <id>                   AMI id (ami-405f7226)
   --volume-name <text>              Name of the EBS volume (eakl)
   --device-name <path_name>         Path of the device (/dev/sda1)
   --volume-size <num>               Size of the EBS volume in GB (0)
   --volume-type <type>              Type of the volume (gp2)
   --delete-on-termination <bool>    Delete volume on termination (true)
   --user-data <file_name>           Script executed at instance startup (startup_data.txt)
```

##### Examples

```bash
eakl@hostname:~/ec2-starter $ ./setup_instance --defaults
The instance will be configured with the following options:

Name.............: eakl
Region...........: eu-west-1
Instance Type....: t2.micro
Image Id.........: ami-405f7226

Volume Name......:
Device Name......:
Volume Size......: 0
Volume Type......:
Delete Volume....:

User Data........:

Do you want to continue? (y/n [n])
```
or

```bash
eakl@hostname:~/ec2-starter $ ./setup_instance --user-data ./startup_data.txt
The instance will be configured with the following options:

Name.............: eakl
Region...........: eu-west-1
Instance Type....: t2.micro
Image Id.........: ami-405f7226

Volume Name......:
Device Name......:
Volume Size......: 0
Volume Type......:
Delete Volume....:

User Data........: ./startup_data.txt

Do you want to continue? (y/n [n])
```

The script generates two files. A delete script and a config file.

##### Output

```bash
Delete script.........: delete-vpc-<name>-<vpc_id>
Config file...........: .aws
```

The `config file (.aws)` contains all the information of your VPC and instance configuration. The `delete script` will delete your VPC, your config file and itself.

### create_instance

This script will read your config file, start your instance and create an `instance` script:

```bash
eakl@hostname:~/ec2-starter $ ./create_instance
This instance will be created:

Name.............: eakl
Region...........: eu-west-1
Instance Type....: t2.micro
Image Id.........: ami-405f7226

Volume Name......:
Device Name......:
Volume Size......: 0
Volume Type......:
Delete Volume....:

User Data........: ./startup_data.txt

Do you want to continue? (y/n [n])
```

##### Output

```bash
Instance script...: instance
```

### instance

```bash
eakl@hostname:~/ec2-starter $ ./instance
usage: instance <command>

commands:
   help                            Get help
   show                            Show instance information
   connect                         Connect to the instance
   upload    <local>   <remote>    Upload from local source to remote destination
   download  <remote>  <local>     Download from remote source to local destination
   start                           Start the instance
   stop                            Stop the instance
   reboot                          Reboot the instance
   delete                          Delete the instance
```

The `delete` option will terminate the instance (automatically deleted) and delete the `instance` script itself. Note that you must preferably call `./instance delete` __BEFORE__ `./delete-vpc-<name>-<vpc_id>`.

### manage_keypair

```bash
eakl@hostname:~/ec2-starter $ ./manage_keypair
usage: manage_keypair <command>

commands:
   --show                  Show Key Pairs
   --delete <key_name>     Delete <key_name>
```

This script uses my own environment variable `$CONFIG` pointing to my config folder where an `aws` folder keeps my AWS keypairs.
