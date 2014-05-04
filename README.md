# Ansible Postfix Role #

Ansible role to make sure postfix is installed, configured and running.
Feedback, bug-reports, requests, is welcomed and can be done via
[github issues](https://github.com/New-Edge-Engineering/ansible-postfix/issues).

## Requirements & Dependencies ##
- Tested on Mac OS X with Ansible 1.5.

#### Variables

```yaml
mail_type: "client"
smtpd_use_tls: "yes"
smtp_sasl_auth_enable: "yes"
smtp_sasl_password_maps: "hash:/etc/postfix/sasl_passwd"
smtp_sasl_security_options: "noanonymous"
smtp_tls_cafile: "/etc/ssl/certs/Thawte_Premium_Server_CA.pem"
smtp_use_tls: "yes"
myorigin: "example.com"
mydomain: 
myhostname: "{{ ansible_hostname }}"
mail_relay_networks: "127.0.0.0/8" # network mask of what machines on the network can use this postfix mail relayer
smtp_sasl_user_name: "example"     # Mail account user name to relay messages through.
smtp_sasl_passwd: "example"        # Mail account password
relay_host_port: "25"              # SMTP port to relay messages on, either 25, 465
```

## License ##

Licensed under the MIT License. See the LICENSE file for details.
