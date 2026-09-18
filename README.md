# Simulador de Escalonamento de Tarefas — Grupo XX

## Integrantes

- João Andrade
- Roger Rocha
- Samar Victor

## Como executar

Clique duas vezes em `Simulador.exe`.

Não é necessário instalar nada.

## Descrição

Este projeto é um simulador de algoritmos de escalonamento de processos desenvolvido em Python[cite: 2]. Ele foi construído para reproduzir numericamente cenários de referência e expor fenômenos complexos de concorrência, como a inversão de prioridades e seus respectivos mecanismos de correção.

A arquitetura do código foi estruturada com base na separação estrita entre o mecanismo de simulação e a política de escalonamento. O sistema interage com o usuário por meio de uma interface gráfica.

## Estrutura do repositório

```text
simulador-escalonamento/
├── README.md          Documentação inicial do projeto
├── Simulador.exe      Programa pronto para executar
├── main.py            Ponto de entrada do código-fonte
├── simulador/         Código-fonte do simulador
├── cenarios/          Conjuntos de tarefas em JSON
└── docs/              Tutoriais e documentação técnica
```

## Arquivos de código

- `simulador/modelo.py` — estrutura de uma tarefa
- `simulador/motor.py` — laço de simulação (mecanismo)
- `simulador/politicas.py` — os seis algoritmos (política)
- `simulador/metricas.py` — cálculo de tt, tp e tw
- `simulador/interface.py` — janela do programa

## Funcionalidades

| O que faz | Onde |
|-----------|------|
| Os seis algoritmos | `simulador/politicas.py` |
| Métricas por tarefa | `simulador/metricas.py` |
| Recurso de uso exclusivo | `simulador/motor.py` |
| Herança e teto | `simulador/motor.py` |
| Envelhecimento | `simulador/politicas.py` |
| Sorteio de cenários | `simulador/gerador.py` |

## Documentação

- [Tutorial de execução](./docs/tutorial_execucao.pdf)
- [Tutorial de uso](./docs/tutorial_uso.pdf)
- [Documentação técnica](./docs/documentacao_projeto.pdf)

## Requisitos de ambiente

- Python 3.10+[cite: 2]
- Bibliotecas: Nenhuma biblioteca externa é necessária (apenas biblioteca padrão do Python).

## Por onde começar

1. Abra o programa e siga o tutorial de execução
2. Reproduza um cenário de exemplo pelo tutorial de uso
3. Consulte a documentação técnica para entender o código

## Uso de assistentes de programação

Os assistentes de programação foram utilizados para:
- Auxiliar na estruturação do `README.md` e da documentação técnica.
- Explicar a implementação de algoritmos específicos e mecanismos, como a herança de prioridade.
- Fornecer auxílio com o código-fonte base para o mecanismo de simulação e as políticas de escalonamento (arquivo `src/simulador.py`).
- Fornecer auxílio com ocódigo para a suíte de testes normativos (`tests/test_normativos.py`).
- Fornecer orientações sobre a implementação da interface com `tkinter`.