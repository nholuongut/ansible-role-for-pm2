# Ansible Role - pm2

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Install and configure PM2 for a nodejs project

## Variables

```yaml
vars:
  flags:
    - init # Basic initialization
    - processes # Configure the node processes to start at reboot
    - upgrade # Upgrade relevant packages

  deploy_dir: # Required for where the base path lives
```

## Examples

```yaml
- hosts: all

  roles:
    - { role: nholuong.pm2, flags: ["init"] }
    - { role: nholuong.pm2, flags: ["processes"] }
    - { role: nholuong.pm2, flags: ["upgrade"] }
```

```bash
export deploy="'deploy_dir': '/opt/servers/node'"

ansible-playbook playbooks/pm2.yml -e "{'flags': ['init'], ${deploy }}" -t init
ansible-playbook playbooks/pm2.yml -e "{'flags': ['configure'], ${deploy }}" -t processes
ansible-playbook playbooks/pm2.yml -e "{'flags': ['packages'], ${deploy }}" -t upgrade
```

## Linting

```bash
yamllint -c yamllint.yaml .
ansible-lint .
```

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
