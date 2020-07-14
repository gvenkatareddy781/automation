Automation Scripts for Linux

These automation scripts are useful to achieve the following items:
Linux RHEL 6/7 and Centos 6/7
* prepare_instance_for_ami_and_shutdown.sh - Run the prepare-for-wigs scripts for the Servers
* rhel-subscription-manager.sh - Run RHEL subscription script only for RedHat Linux
* sshd_config.sh - Configure SSHD to allow pubkey authentication

Scripts that are helpful are:
* Disable LDAP on RHEL code 
    ```mv /etc/sssd/sssd.conf /etc/sssd/sssd.conf.orig
    chkconfig sssd off
    /etc/init.d/sssd stop
    /etc/init.d/nslcd stop 
    chkconfig nslcd off
    mv /etc/nslcd.conf /etc/nslcd.conf.orig 
    ```

* Remove existing .aws folder
    ```
    rm -rf /root/.aws
    ```
    
 Note: The script rhel-subsription-manager.sh need to be updated with the subscription emailid and password before running it
