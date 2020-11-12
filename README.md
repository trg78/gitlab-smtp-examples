# gitlab-smtp-examples
Works with GitLab 13.0.5 (9097f912ba5) FOSS  GitLab Shell 13.2.0  PostgreSQL  11.7
You should add it to /etc/gitlab/gitlab.rb
and start gitlab-ctl reconfigure


It works for mirohost.net on 12 11 2020
'''
gitlab_rails['smtp_enable'] = true
gitlab_rails['smtp_address'] = "mx1.mirohost.net"
gitlab_rails['smtp_port'] = 587
gitlab_rails['smtp_user_name'] = "gitlab@testdomain.ua"
gitlab_rails['smtp_password'] = "SomePassword"
gitlab_rails['smtp_authentication'] = "login"
gitlab_rails['smtp_enable_starttls_auto'] = true
gitlab_rails['smtp_tls'] = false
gitlab_rails['smtp_openssl_verify_mode'] = 'peer' # Can be: 'none', 'peer', 'cl
gitlab_rails['gitlab_email_reply_to'] = "gitlab@testdomain.ua"
'''

It works for mailgun.org  on 12 11 2020

'''
gitlab_rails['smtp_enable'] = true
gitlab_rails['smtp_address'] = "smtp.mailgun.org"
gitlab_rails['smtp_port'] = 587
gitlab_rails['smtp_user_name'] = "postmaster@sandbox123123123bebebe"
gitlab_rails['smtp_password'] = "SomePassword123123123123"
gitlab_rails['smtp_authentication'] = "login"
gitlab_rails['smtp_enable_starttls_auto'] = true
gitlab_rails['smtp_tls'] = false
gitlab_rails['smtp_openssl_verify_mode'] = 'peer' # Can be: 'none', 'peer', 'cl
gitlab_rails['smtp_ssl'] = false
'''


How to debug - 
https://docs.gitlab.com/ee/administration/troubleshooting/debug.html
