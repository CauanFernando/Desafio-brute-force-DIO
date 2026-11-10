# Desafio-brute-force-DIO
entrega do desafio previsto no curso de brute force com medusa

# 🛡️ Simulação de Ataque de Força Bruta com Medusa no Kali Linux

Repositório criado para documentar o desafio prático de cibersegurança da **DIO**. O objetivo foi simular e analisar um ataque de força bruta (*Brute Force*) em ambiente de testes controlado utilizando a ferramenta **Medusa**.

---

## 🎯 Objetivo do Desafio
- Demonstrar na prática a vulnerabilidade de serviços com credenciais fracas ou padrão.
- Compreender o funcionamento de ferramentas automatizadas de quebra de credenciais.
- Praticar o uso de wordlists e do sistema Kali Linux.

---

## 🧰 Ferramentas Utilizadas
- **Kali Linux**: Sistema operacional para testes de invasão e auditoria de segurança.
- **Medusa**: Ferramenta rápida e modular para ataques de força bruta contra serviços de rede (como SSH, FTP, etc.).
- **Wordlists**: Dicionários de palavras e senhas utilizados no teste.

---

## 🚀 Execução do Laboratório

### 1. Preparação e Parâmetros
O comando básico utilizado com o Medusa seguiu a sintaxe:
\`\`\`bash
medusa -h <IP_ALVO> -u <USUARIO> -P <CAMINHO_DA_WORDLIST> -M <MODULO/SERVIÇO>
\`\`\`
*(Substitua ou explique aqui os parâmetros que você utilizou no seu teste).*

### 2. Resultados e Evidências
Abaixo estão as capturas de tela obtidas durante os testes:

#### Teste de Conexão / Execução do Ataque:
![Execução do Medusa](images/nome-do-seu-print.png)

#### Sucesso na Identificação das Credenciais:
![Resultado do Teste](images/outro-print.png)

*(Dica: troque `nome-do-seu-print.png` pelo nome exato do arquivo que você enviou na pasta images).*

---

## 🛡️ Medidas de Mitigação e Defesa
Na visão de segurança defensiva, ataques desse tipo podem ser prevenidos com:
- **Políticas de senhas fortes**: exigindo tamanho mínimo e complexidade.
- **Bloqueio de contas (Account Lockout)**: limitar o número de tentativas consecutivas incorretas (ex: via *Fail2ban*).
- **Autenticação de Dois Fatores (2FA/MFA)**: adicionando uma camada extra além de usuário e senha.
- **Alteração de portas padrão**: para dificultar a varredura automatizada.

---
## 🧪 Passo a Passo do Laboratório e Evidências

### 1. Configuração do Ambiente Virtual (Lab Setup)
Para simular um ambiente real e seguro, foram configuradas duas máquinas virtuais na mesma rede:
- **Atacante:** Kali Linux
- **Alvo:** Metasploitable 2 (máquina deliberadamente vulnerável para testes)

| Etapa | Evidência |
| :--- | :--- |
| Visão geral das VMs | ![VMs](<images/VMs.jpeg>) |
| Configuração de rede do Kali Linux | ![Rede Kali](<images/Config rede kali.jpeg>) |
| Configuração de rede da Metasploitable | ![Rede Metasploitable](<images/Config rede Metasploitable.jpeg>) |
| Identificação do IP do alvo | ![IP Alvo](<images/metasploitable ip.jpeg>) |

---

### 2. Reconhecimento e Conectividade
Antes de iniciar o ataque, foi verificada a comunicação entre as máquinas e as portas/serviços abertos no alvo.

| Etapa | Evidência |
| :--- | :--- |
| Verificação de portas abertas e serviços | ![Varredura](<images/tentando conexão com metasploitable e verificando portas abertas.jpeg>) |
| Diagnóstico e teste de falha de conexão | ![Teste Falho](<images/teste de conexão (falho).jpeg>) |
| Conexão estabelecida com sucesso | ![Conexão Completa](<images/conexao completa.jpeg>) |

---

### 3. Cenário 1: Ataque de Força Bruta em Aplicação Web (DVWA)
Simulação de tentativa de autenticação na aplicação DVWA (*Damn Vulnerable Web Application*) usando o Medusa:

1. **Tentativa manual:** Demonstração do erro com credenciais incorretas.
   ![Login Incorreto](<images/login incorreto dwva.jpeg>)

2. **Ataque com Medusa:** Automatização do teste de senhas com base em dicionário.
   ![Executando Medusa](<images/executando medusa e testando senha.jpeg>)

3. **Validação do Acesso:** Confirmação de login com as credenciais identificadas.
   ![Login com Sucesso](<images/testando com senha correta.jpeg>)
   ![Certificação do Teste](<images/certificando rteste.jpeg>)

---

### 4. Cenário 2: Força Bruta contra o Serviço SMB
Nesta etapa, o Medusa foi direcionado ao protocolo de compartilhamento de arquivos SMB:

1. **Construção das Wordlists:** Preparação e verificação dos arquivos contendo usuários e senhas.
   ![Criação dos Arquivos](<images/verificando criaço do arquivo.jpeg>)
   ![Listas de Usuários e Senhas](<images/white list para user e password.jpeg>)
   ![Lista de Usuários SMB](<images/smb user list.jpeg>)

2. **Execução dos Testes no SMB:**
   ![Teste SMB 1](<images/teste smb.jpeg>)
   ![Teste SMB 2](<images/teste smb 2.jpeg>)
   ![Teste SMB 3](<images/teste smb 3.jpeg>)
   ![Teste SMB 4](<images/teste smb 4.jpeg>)
   ![Teste SMB 5](<images/teste smb 5.jpeg>)

3. **Credenciais Encontradas:**
   O Medusa identificou com sucesso o par usuário/senha válido no serviço SMB:
   ![Usuário e Senha Encontrados](<images/encontrando user e password necessario.jpeg>)
   ![Conclusão com Senha Correta](<images/teste realizado e concluido com senha.jpeg>)

## 🎓 Autor
Desenvolvido por **Seu Nome** durante o curso da [DIO](https://dio.me).
