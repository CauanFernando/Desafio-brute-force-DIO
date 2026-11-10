# Desafio-brute-force-DIO
entrega do desafio previsto no curso de brute force com medusa

---
## 🧪 Passo a Passo do Laboratório e Evidências

### 1. Configuração do Ambiente Virtual (Lab Setup)
Para simular um ambiente real e seguro, foram configuradas duas máquinas virtuais na mesma rede:
- **Atacante:** Kali Linux
- **Alvo:** Metasploitable 2 (máquina deliberadamente vulnerável para testes)

| Etapa | Evidência |
| :--- | :--- |
| Visão geral das VMs | ![VMs](<Brute Force/VMs.jpeg>) |
| Configuração de rede do Kali Linux | ![Rede Kali](<Brute Force/Config rede kali.jpeg>) |
| Configuração de rede da Metasploitable | ![Rede Metasploitable](<Brute Force/Config rede Metasploitable.jpeg>) |
| Identificação do IP do alvo | ![IP Alvo](<Brute Force/metasploitable ip.jpeg>) |

---

### 2. Reconhecimento e Conectividade
Antes de iniciar o ataque, foi verificada a comunicação entre as máquinas e as portas/serviços abertos no alvo.

| Etapa | Evidência |
| :--- | :--- |
| Verificação de portas abertas e serviços | ![Varredura](<Brute Force/tentando conexão com metasploitable e verificando portas abertas.jpeg>) |
| Diagnóstico e teste de falha de conexão | ![Teste Falho](<Brute Force/teste de conexão (falho).jpeg>) |
| Conexão estabelecida com sucesso | ![Conexão Completa](<Brute Force/conexao completa.jpeg>) |

---

### 3. Cenário 1: Ataque de Força Bruta em Aplicação Web (DVWA)
Simulação de tentativa de autenticação na aplicação DVWA (*Damn Vulnerable Web Application*) usando o Medusa:

1. **Tentativa manual:** Demonstração do erro com credenciais incorretas.
   ![Login Incorreto](<Brute Force/login incorreto dwva.jpeg>)

2. **Ataque com Medusa:** Automatização do teste de senhas com base em dicionário.
   ![Executando Medusa](<Brute Force/executando medusa e testando senha.jpeg>)

3. **Validação do Acesso:** Confirmação de login com as credenciais identificadas.
   ![Login com Sucesso](<Brute Force/testando com senha correta.jpeg>)
   ![Certificação do Teste](<Brute Force/certificando rteste.jpeg>)

---

### 4. Cenário 2: Força Bruta contra o Serviço SMB
Nesta etapa, o Medusa foi direcionado ao protocolo de compartilhamento de arquivos SMB:

1. **Construção das Wordlists:** Preparação e verificação dos arquivos contendo usuários e senhas.
   ![Criação dos Arquivos](<Brute Force/verificando criaço do arquivo.jpeg>)
   ![Listas de Usuários e Senhas](<Brute Force/white list para user e password.jpeg>)
   ![Lista de Usuários SMB](<Brute Force/smb user list.jpeg>)

2. **Execução dos Testes no SMB:**
   ![Teste SMB 1](<Brute Force/teste smb.jpeg>)
   ![Teste SMB 2](<Brute Force/teste smb 2.jpeg>)
   ![Teste SMB 3](<Brute Force/teste smb 3.jpeg>)
   ![Teste SMB 4](<Brute Force/teste smb 4.jpeg>)
   ![Teste SMB 5](<Brute Force/teste smb 5.jpeg>)

3. **Credenciais Encontradas:**
   O Medusa identificou com sucesso o par usuário/senha válido no serviço SMB:
   ![Usuário e Senha Encontrados](<Brute Force/encontrando user e password necessario.jpeg>)
   ![Conclusão com Senha Correta](<Brute Force/teste realizado e concluido com senha.jpeg>)

## 🎓 Autor
Desenvolvido por **Cauan Fernando da Silva** durante o curso da [DIO](https://dio.me).
