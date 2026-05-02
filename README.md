# 🖥️ GLPI via Docker

Projeto de implantação do **GLPI** (Gestão de Chamados e Inventário de TI) utilizando Docker e Docker Compose, com banco de dados MariaDB e persistência de dados via volumes.

---

## 🚀 Tecnologias utilizadas

- [GLPI](https://glpi-project.org/) — Sistema de gestão de helpdesk e inventário
- [Docker](https://www.docker.com/) — Containerização da aplicação
- [Docker Compose](https://docs.docker.com/compose/) — Orquestração dos containers
- [MariaDB 10.7](https://mariadb.org/) — Banco de dados relacional

---

## 📋 Pré-requisitos

- [Docker Desktop](https://www.docker.com/products/docker-desktop) instalado (Windows/Mac)
- Ou Docker + Docker Compose instalado (Linux)

---

## ▶️ Como rodar o projeto

**1. Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

**2. Suba os containers:**
```bash
docker compose up -d
```

**3. Acesse no navegador:**
```
http://localhost:8080
```

---

## 🗄️ Configuração do banco de dados

Na primeira execução, o assistente de instalação do GLPI será exibido. Use as credenciais abaixo:

| Campo          | Valor           |
|----------------|-----------------|
| Servidor SQL   | `db`            |
| Usuário        | `glpi_user`     |
| Senha          | `glpi_password` |
| Base de dados  | `glpidb`        |

---

## 💾 Persistência de dados

O projeto utiliza volumes Docker para garantir que os dados não sejam perdidos ao reiniciar os containers:

- `db_data` — Dados do banco MariaDB
- `glpi_data` — Arquivos e configurações do GLPI

---

## 🛑 Parar o projeto

```bash
docker compose down
```

> Os dados ficam preservados nos volumes. Para apagar tudo inclusive os dados, use `docker compose down -v`.

---

## 📁 Estrutura do projeto

```
.
├── docker-compose.yml
└── README.md
```

---

## 💡 Motivação

Esse projeto nasceu de uma atividade da faculdade onde eu poderia escolher entre várias ferramentas para implantar: Zabbix, Zimbra, PROXMOX Backup, GitLab, CRUD e GLPI. Optei pelo GLPI por ser um sistema muito presente em ambientes reais de suporte de TI.

Ao pesquisar como rodar o GLPI, me deparei com a abordagem tradicional via XAMPP — e achei o processo trabalhoso demais. Fui buscar alternativas e foi pesquisando e consultando diferentes fontes, incluindo IA, que descobri o Docker e o Docker Compose como alternativa mais prática. Como era minha primeira vez com Docker, usei essas ferramentas também para aprender a instalar e configurar tudo do zero.

---

## 🧠 Aprendizados

- Como orquestrar múltiplos containers com Docker Compose
- Configuração de variáveis de ambiente para integração entre serviços
- Uso de volumes para persistência de dados em containers
- Como tornar um projeto local facilmente compartilhável entre diferentes sistemas operacionais (Linux e Windows)

---

## 🔗 Referências

- [Imagem oficial do GLPI — Docker Hub (elestio/glpi)](https://hub.docker.com/r/elestio/glpi)
- [Imagem oficial do MariaDB — Docker Hub](https://hub.docker.com/_/mariadb)
- [Documentação oficial do GLPI](https://glpi-project.org/)
- [Documentação do Docker Compose](https://docs.docker.com/compose/)

---

## 👤 Autor

Feito por **FRANCISCO EDUARDO GOMES GONCALVES** — [GitHub](https://github.com/franciscoggoncalves)
