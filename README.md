# Ansible Role kanboard
[![Build Status](https://travis-ci.org/reminec/ansible-role-kanboard.svg?branch=master)](https://travis-ci.org/reminec/ansible-role-kanboard)
Install or update to the latest kanboard version.

This role can also install apache2 to run your kanboard installation - disabled by default

## Requirements
None.

## Role Variables

All variables are optionnals

### Install apache2
By default, the role let you install your preffered webserver.
If you want install apache2, change this var to true

```yaml
kanboard_install_apache2: true
```

### Enable url rewrite on kanboard
```yaml
kanboard_enable_url_rewrite: false
```

### Configuring a gitlab oAuth instance
```yaml
# Gitlab related vars
kanboard_use_gitlab_auth: true
kanboard_gitlab_client_id: '' # change it
kanboard_gitlab_client_secret: '' # change it
kanboard_gitlab_oauth_authorize_url: 'https://gitlab.com/oauth/authorize'
kanboard_gitlab_oauth_token_url: 'https://gitlab.com/oauth/token'
kanboard_gitlab_api_url: 'https://gitlab.com/api/v3/'
```

### Configuring a github oAuth instance
```yaml
# Github related vars
kanboard_use_github_auth: true
kanboard_github_client_id: '' # change it
kanboard_github_client_secret: '' # change it
```

### Other default usefull vars
```yaml
kanboard_path: /var/www
kanboard_release_url: http://kanboard.net/kanboard-latest.zip
kanboard_chmod_user: www-data
kanboard_chmod_group: www-data
```

## Dependencies

None.

## Example Playbook


    - hosts: kanboard
      roles:
         - { role: reminec.kanboard }

## License
MIT - [See LICENSE](LICENSE)

## Author Information
This role was created by [Reminec](https://github.com/reminec)
