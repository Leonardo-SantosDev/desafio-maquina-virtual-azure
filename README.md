# ☁️ Desafio de Criação de Máquina Virtual no Azure  

## 📘 Descrição do Desafio
Este repositório foi criado como parte do **Desafio de Projeto da DIO**, com o objetivo de consolidar os conhecimentos adquiridos sobre **Máquinas Virtuais no Microsoft Azure**.  

O desafio consiste em **compreender o processo de criação, configuração e documentação** de uma Máquina Virtual (VM) na nuvem, utilizando o **portal do Azure** e o **GitHub** para registro da experiência.

---

## 🎯 Objetivos de Aprendizagem
Ao final deste desafio, é esperado que o aluno seja capaz de:
- Aplicar conceitos de **infraestrutura em nuvem (IaaS)**;  
- Compreender o processo de **criação de máquinas virtuais no Azure**;  
- Documentar de forma clara e técnica cada etapa do processo;  
- Utilizar o **GitHub** como ferramenta de versionamento e portfólio profissional.  

---

## ⚙️ Etapas Realizadas

### 1. Acesso ao Portal do Azure
Acesse o [Portal do Azure](https://portal.azure.com) utilizando sua conta Microsoft.  
Na tela inicial, clique em **“Máquinas Virtuais” → “Criar” → “Máquina Virtual do Azure”**.

---

### 2. Guia “Básico” – Configuração Inicial
- **Assinatura:** Azure for Students (ou Free Trial)  
- **Grupo de Recursos:** `RG-DesafioVM`  
- **Nome da Máquina Virtual:** `vm-desafio-dio`  
- **Região:** *East US (EUA Leste)*  
- **Imagem:** *Ubuntu Server 22.04 LTS* (também pode ser Windows Server)  
- **Tamanho:** `B1s (Free Tier)`  
- **Usuário Administrador:** `azureuser`  
- **Tipo de Autenticação:** Senha  
- **Portas de Entrada Permitidas:** SSH (22)

---

### 3. Guia “Discos”
- Tipo de disco do SO: **SSD padrão (Standard SSD)**
- Opção de criptografia: **Padrão**

---

### 4. Guia “Rede”
- Criado uma **nova rede virtual (VNet)** e uma **sub-rede padrão**  
- IP público habilitado  
- Grupo de segurança de rede (NSG): regras básicas de SSH permitidas  

---

### 5. Guia “Revisar + Criar”
Após validar as configurações, clique em **“Criar”**.  
O Azure provisiona automaticamente a máquina virtual em poucos minutos.

---

## 🖥️ Acesso à Máquina Virtual
Após a criação, o acesso pode ser feito via **SSH** (para Ubuntu) ou **RDP** (para Windows):

### Exemplo de acesso via SSH:
```bash
ssh azureuser@<ip-publico-da-vm>
