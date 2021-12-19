# Generate Markdown from Ansible Facts

To use ansible facts for autogenerating a documentation on network inventory, this small playbook and template is a good start.


## Installation

- simply configure output location and location of git repositorys in the vars file.
- unfortunatly withouth git repo, the script will break at the moment, should be easy to fix
- make sure hostnames are unique - or the templates get overwritten

### requirements

- `ansible-galaxy collection install community.general`
- netstat on host for the open ports
- python >= 2.7 on host for the docker functionality

## Usage

- simply create an inventory and `ansible-playbook generateFactsMarkdown.yml -i hosts`
- totally recommended in combination with mkdocs or any static site generator. 
- if i keep working on this, ill be working at it at work so from that point i cannot update here anymore since it belongs to the firm
