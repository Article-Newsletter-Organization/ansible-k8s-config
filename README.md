# Introduction

This project aims to configurate the DevOps tools in use on the system. The ``Ansible``, a tool for work automation, is used in this project.  

## Modules

This project have multiples divisions, one for each tool,and each of them have your own dependencies. 

The documentation is on the `/doc` folder.

## Requeriments

- **Ansible** - Latest version


<details>
  <summary><b>Note:</b> Use linux distribuition! </summary>
  
  The ansible works better in Linux environment, if your Operating System is Windows you might use WSL(Windows Subsystem Linux). 

</details>

## Usage

The modules are organized with this approach:

```
foldername
-- config
-- playbook 
---- example.playbook.yaml
```

For execute the automation:
```
ansible-playbook playbook/example.playbook.yaml
```

## Pré-requisitos
- `kubectl` configurado
- credenciais de uma conta no GCP(Google Cloud Provider) em formato de json nomeado `gcp-credentials.private.json` na raiz do projeto
- 

```
kubectl create secret generic -n vault kms-creds --from-file=../gcp-crede
ntials.private.json
```