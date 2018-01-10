# Unami Lodge Server Setup
Documentation on building and the current configuration of Unami Lodge's Servers.

## Build
1. Clone [TheScoutmaster](https://github.com/col-bsa/TheScoutmaster) to your local machine and follow its instructions for:
   - Installation
   - DigitalOcean Configuration
   - GitHub Configuration
2. Update vars.yml
   - Add:
     - do_api_token
     - github_user
     - github_email
     - github_token
     - slack_hook
   - Update:
     - admin_email
     - github_owner
     - slack_channel
     - slack_user
     - do_name
     - virtual_hosts
       - repo
       - branch
       - alias
     - ssl_domains
3. Run `launch.yml`.
   - Within a couple minutes this will generate a droplet and its ip addresses.
4. Point whichever domains or subdomains you wish at the ip address.
5. Have a cup of coffee (Takes 10-20 minutes for the rest of the playbook to run).
6. When the playbook pauses to wait for domains to be updated, press `Enter`.

## Configuration

### Format
- *Server Name*
   - *host*
      - *alias*

### Servers
- [prod.unamilodge.org](#)
  - [prod.unamilodge.org](#)
    - [unamilodge.org](#)
    - [www.unamilodge.org](#)
    - [production.unamilodge.org](#)
- [dev.unamilodge.org](#)
  - [dev.unamilodge.org](#)
    - [development.unamilodge.org](#)
  - [dev.resicafalls.org](#)
    - [development.resicafalls.org](#)
- [prod.resicafalls.org](#)
  - [prod.resicafalls.org](#)
    - [resicafalls.org](#)
    - [www.resicafalls.org](#)
  - [prod.mussersr.org](#)
    - [mussersr.org](#)
    - [www.mussersr.org](#)
  - [downloads.resicafalls.org](#)
    - *Note: This virtual host is served from the volume attached to the server.*