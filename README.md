# 🐧 Comandos básicos de Linux, Kubectl e K9s

Este documento reúne comandos simples e úteis para o dia a dia no terminal Linux, no Kubernetes e no K9s.  

---

## 🧩 Linux Básico

### 📁 Navegação entre diretórios

**CD** Muda o diretório atual.
```bash
cd ..
```

**LS** Lista arquivos e pastas do diretório atual.
```bash
ls
```

**PWD** Mostra o caminho completo do diretório atual.
```bash
pwd
```

---

### 📂 Manipulação de arquivos e pastas

**TOUCH** Cria um novo arquivo vazio.
```bash
touch arquivo.txt
```

**MKDIR** Cria um novo diretório.
```bash
mkdir pasta_nova
```

**CAT** Exibe o conteúdo de um arquivo.
```bash
cat arquivo.txt
```

**LESS** Exibe o conteúdo de um arquivo página por página.
```bash
less arquivo.txt
```

---

### ⚙️ Sistema e processos

**CLEAR** Limpa o terminal.
```bash
clear
```

**WHOAMI** Mostra o nome do usuário logado.
```bash
whoami
```

**TOP** Mostra processos em execução.
```bash
top
```

**FREE -H** Mostra o uso de memória.
```bash
free -h
```

**DF -H** Mostra o uso do disco.
```bash
df -h
```

---

### ☸️ Comandos básicos de Kubectl

Ver todos os contextos configurados:
```bash
kubectl config get-contexts
```

Ver o contexto ativo:
```bash
kubectl config current-context
```

Listar todos os namespaces:
```bash
kubectl get namespaces
```

Listar todos os pods de um namespace:
```bash
kubectl get pods -n <nome-do-namespace>
```

Listar todos os serviços:
```bash
kubectl get svc -n <nome-do-namespace>
```

Listar deployments:
```bash
kubectl get deployments -n <nome-do-namespace>
```

---

### 🧠 Detalhamento e logs

Ver detalhes de um pod específico:
```bash
kubectl describe pod <nome-do-pod> -n <namespace>
```

Ver logs de um pod:
```bash
kubectl logs <nome-do-pod> -n <namespace>
```

Ver logs de um pod com múltiplos containers:
```bash
kubectl logs <nome-do-pod> -c <nome-do-container> -n <namespace>
```

### Acesso ao pod

Entrar no shell do pod:
```bash
kubectl exec -it <nome-do-pod> -n <namespace> -- /bin/bash
```

⚠️ Cuidado: Use este comando apenas para consultar ou inspecionar.
Evite alterar configurações dentro do pod em ambiente de trabalho.

---

### 🖥️ Comandos básicos do K9s

O K9s é uma interface interativa de terminal para Kubernetes.
Comandos principais

**Abrir** o K9s:
```bash
k9s
```

**Sair** do K9s:
```bash
:q
```
Ou
```bash
Ctrl + C
```

### Navegação (K9s)

Buscar recurso:	/   
Ver pods:	po   
Ver deployments:	d   
Ver namespaces:	:ns   
Mudar contexto:	:ctx   
Filtrar resultados:	/texto   
Atualizar tela:	Ctrl + R   
Voltar:	Esc   

### Ações úteis (K9s)

Ver logs do pod selecionado:	l   
Entrar no shell do container:	s   
Descrever recurso selecionado:	Shift + d
Ver detalhes do container:	Enter
Ver eventos do namespace atual:	0

