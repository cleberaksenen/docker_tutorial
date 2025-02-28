# Docker tutorial
## Istalação
### Passo 01: Atualizar os pacotes do sistema
```
sudo apt update && sudo apt upgrade -y
```

### Passo 2: Instalar dependências
```
sudo apt install -y ca-certificates curl gnupg
```

### Passo 3: Remover pacotes não mais necessários (opcional)
```
sudo apt autoremove -y
```

### Passo 4: Adicionar a chave GPG do Docker
```
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo tee /etc/apt/keyrings/docker.asc > /dev/null
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

### Passo 5: Adicionar o repositório oficial do Docker
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Passo 6: Atualizar a lista de pacotes
```
sudo apt update
```
## ---


## Perguntas
### Devo instalar o Docker em um ambiente versionado pelo conda por exemplo?
Não nesse caso. O Conda é um gerenciador de pacotes e ambientes que funciona bem para instalar e isolar pacotes de Python e algumas dependências do sistema. 
No entanto, o Docker não é um pacote Python, mas sim um serviço que roda no nível do sistema operacional.
