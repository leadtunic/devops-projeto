# DevOps Lab

Projeto prático de CI/CD e containerização criado para experimentar um fluxo simples de entrega com **Python, Docker e GitHub Actions**.

## Objetivo

Este repositório funciona como um laboratório de DevOps para validar conceitos de automação de build, lint, pipeline e deploy com runner self-hosted.

## Stack

- Python 3
- Docker
- GitHub Actions
- Self-hosted runner
- Linux

## Pipeline

O workflow em `.github/workflows/main.yml` executa:

1. Checkout do código.
2. Preparação do ambiente Python.
3. Instalação opcional de dependências.
4. Etapa de build/teste.
5. Etapa de lint.
6. Deploy em runner self-hosted identificado com as labels `linux` e `deploy`.

## Estrutura

```text
.
├── .github/workflows/main.yml
├── Dockerfile
├── app.py
└── README.md
```

## Executando localmente

```bash
python app.py
```

Ou via Docker:

```bash
docker build -t devops-lab .
docker run --rm devops-lab
```

## Sobre

Projeto de estudo e experimentação de automação de entrega mantido por [Giovani Ricetto](https://github.com/leadtunic).

Veja também meu portfólio em [benedash.com](https://benedash.com).
