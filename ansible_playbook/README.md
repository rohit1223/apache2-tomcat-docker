Populate "`inventory`" file with corerct IP address of VM and ssh pass.

Make sure ansible connection is made prior to running this palybook

After cloning the repo beome sudo user before running this play.

`sudo su` (in ubuntu)

`ansible-playbook -i inventory play.yml`

To clean-up all the docker containers, swarm, stack and services run the clean-up play.

`ansible-playbook -i inventory clean-up.yml`

In case of any error in clean-up process debug the `clean-up.yml` file accordingly.
