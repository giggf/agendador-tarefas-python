# 📅 Agendador de Tarefas Master (Python)

Uma aplicação Desktop para o **agendamento e automação da execução de programas no Windows**, desenvolvida em Python com interface gráfica e persistência local.

O projeto surgiu da necessidade de tornar a execução recorrente de tarefas mais simples e previsível, permitindo configurar horários, intervalos e executáveis por meio de uma interface, além de manter histórico e logs das execuções.

A aplicação foi desenvolvida utilizando majoritariamente recursos da **biblioteca padrão do Python**, sem dependências externas para sua execução a partir do código-fonte.
## ✨ Funcionalidades Principais

- **Interface Gráfica com Tkinter:** criação, edição e exclusão de tarefas sem necessidade de alterar o código.
- **Preservação do horário de referência:** uma tarefa configurada para executar às 14h a cada 24 horas mantém esse horário como referência entre as execuções.
- **Histórico de Execução:** Visualização na tabela de quando foi a última vez que a tarefa rodou.
- **Edição de Tarefas:** Permite alterar horários e caminhos de tarefas já cadastradas.
- **Execução Visível:** Os programas agendados abrem uma janela do CMD identificada, permitindo monitorar o status e logs do script em tempo real.
- **Persistência local:** configurações das tarefas são armazenadas em JSON e recuperadas ao iniciar a aplicação.
- **Logs de Auditoria:** gera um arquivo `log_execucao.txt` registrando todas as tentativas de execução e erros.
- **Portabilidade:** Salva os dados em JSON na própria pasta, facilitando o transporte via Pen Drive ou rede.

## 🛠️ Tecnologias Utilizadas

Bibliotecas utilizadas:

- `tkinter` - Interface gráfica
- `datetime` & `timedelta` - Controle e cálculo dos agendamentos
- `subprocess` (Gerenciamento de processos do Windows)
- `threading` - Execução paralela para não travar a interface
- `json` - Persistência local das tarefas

**Não é necessário instalar bibliotecas externas (como pandas ou schedule) para rodar o código fonte.**

---

## 🚀 Como Rodar (Código Fonte)

### Pré-requisitos
- Python 3.x
- Windows

### Passo a Passo
1. Clone este repositório:
   ```bash
   git clone <URL-DO-REPOSITÓRIO>
   ```
2. Entre na pasta do projeto :
   ```bash
   cd <NOME-DO-REPOSITÓRIO>
   ```
3. Execute o programa.
   ```bash
   python agendador.pyw
   ```
---

# 📦 Como criar um exectável para a aplicação (.exe)

Para transformar este script em um software standalone (que funciona em computadores sem Python), utilizamos o **PyInstaller**.

## 1. Instalar o PyInstaller
   ```bash
   pip install pyinstaller
   ```
## 2. Gerar o executável
   ```bash
   pyinstaller --noconsole --onefile --clean agendador.pyw
   ```
## 3. Onde está o arquivo?
O executável final estará na pasta `dist`.

---

# 📂 Estrutura de Arquivos
Ao rodar, o programa gerará automaticamente dois arquivos na mesma pasta:
- `tarefas.json`: Banco de dados das suas tarefas.
- `log_execucao.txt`: Histórico de erros e sucessos.

**Nota:** Mantenha o tarefas.json junto do .exe se mover o programa de lugar, para não perder seus agendamentos.

# 🧠 Conceitos Aplicados
O desenvolvimento deste projeto envolver conceitos de:
- Programação orientada a eventos
- Interface gráfica desktop
- Manipulação de procesos
- Concorrência co threads
- Persistência de dados em JSON
- Tratamento de erros e logging
- Manipulação de datas e intervalos de tempo
- Empacotamento de aplicações Python



