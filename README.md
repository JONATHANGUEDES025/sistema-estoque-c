# Sistema de Estoque em C

Aplicação de terminal para cadastrar produtos, registrar quantidades e preços e calcular o valor total do estoque informado.

## Funcionalidades

- Cadastro do nome, quantidade e preço unitário de cada produto.
- Leitura de preços com vírgula ou ponto como separador decimal.
- Cálculo e exibição do subtotal de cada produto.
- Listagem dos itens e do valor total do estoque.
- Alocação dinâmica de memória conforme a quantidade de produtos.

## Como executar

É necessário um compilador C com suporte a C11. Abra o terminal na pasta do repositório.

### Windows com GCC/MinGW

```powershell
New-Item -ItemType Directory -Force build
gcc -std=c11 -Wall -Wextra -Wpedantic src/main.c -o build/estoque.exe
.\build\estoque.exe
```

### Linux ou macOS com compilador C

```bash
mkdir -p build
cc -std=c11 -Wall -Wextra -Wpedantic src/main.c -o build/estoque
./build/estoque
```

## Exemplo

| Produto | Quantidade | Preço unitário | Subtotal |
| --- | --- | --- | --- |
| Caderno | 3 | R$ 12,50 | R$ 37,50 |
| Caneta | 10 | R$ 2,00 | R$ 20,00 |

O valor total desse estoque é **R$ 57,50**.

## Organização

```text
sistema-estoque-c/
├── src/
│   └── main.c
├── .gitignore
└── README.md
```

A pasta `build/` é criada localmente para os executáveis e não faz parte dos arquivos-fonte.

## Escopo

Projeto de estudo de estruturas, laços e alocação dinâmica em C. Os registros existem apenas durante a execução; não há persistência em arquivo ou banco de dados. A entrada exige quantidades inteiras e preços numéricos válidos.

Autor: **Jonathan Guedes**.
