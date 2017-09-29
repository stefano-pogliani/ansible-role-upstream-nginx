upstream-nginx
==============
Install NGINX using the upstream repos.
If a distribution is unsupported fallback to the distro's repos.


Requirements
------------
Nothing.


Role Variables
--------------

| Variable | Description | Default |
| -------- | ----------- | ------- |
| `upstream_nginx_package` | The name of the package to install | `'nginx'` |
| `upstream_nginx_service` | The name of the NGINX service | `'nginx'` |
| `upstream_nginx_service_enabled` | Should the service be enabled? | `'yes'` |
| `upstream_nginx_service_manage` | Should the service be managed? | `true` |
| `upstream_nginx_service_state` | Should the service be running? | `'started'` |


Dependencies
------------
None.


Example Playbook
----------------
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: webs
      roles:
         - role: upstream-nginx


License
-------
MIT


Testing
-------
This role uses [test-kitchen](http://kitchen.ci/) and
[kitchen-ansible](https://github.com/neillturner/kitchen-ansible).

  1. Install gems: `bundle install bundle install --path=.vendor --binstubs`
  2. Run kitchen: `./bin/kitchen test`
