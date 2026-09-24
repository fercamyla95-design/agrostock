# AgroStock
**Controle e rastreabilidade de estoque de insumos agrícolas**

Projeto AgroStock para controle de movimentação de insumos agrícolas desenvolvido e utilizado em uma Fazenda Triângulo para registrar **entradas e saídas de estoque** por meio de um formulário acessado via **QR Code**.
> Este repositório apresenta a solução como projeto de portfólio. Os arquivos públicos são exemplos anonimizados; dados operacionais reais, nomes de pessoas, localização de talhões e links privados não devem ser publicados.

## 🎯 Problema
O controle manual de retirada e devolução de produtos dificultava a rastreabilidade das movimentações. A proposta foi criar um fluxo simples, rápido e acessível pelo celular, sem exigir que o responsável precisasse abrir uma planilha.

## 💡 Solução
1. O responsável escaneia o QR Code disponível no local de armazenamento.
2. O QR Code abre um Google Forms.
3. O responsável informa:
   - entrada ou saída;
   - produto e quantidade;
   - destino/talhão ou outra fazenda;
   - nome do responsável;
   - observação, quando necessário.
4. A data e hora são registradas automaticamente pelo formulário.
5. As respostas ficam armazenadas em uma planilha.
6. Os dados são organizados em uma planilha operacional de estoque.
7. O estoque pode ser consultado a partir das entradas e saídas registradas.

## 🔄 Fluxo do projeto
```text
[QR Code no galpão]
        ↓
[Google Forms]
        ↓
[Registro automático de data/hora]
        ↓
[Planilha de respostas]
        ↓
[Tratamento / organização]
        ↓
[Controle de entradas e saídas]
        ↓
[Consulta do estoque]
```

## 🧪 Validação
A solução foi utilizada durante aproximadamente **5 meses**, incluindo período de safra/colheita de soja.
Durante a implantação, o formulário e o fluxo de dados passaram por alterações e ajustes para melhorar a usabilidade e adequar o registro à rotina dos responsáveis pela pulverização.
Isso é importante no projeto: as primeiras versões não foram tratadas como definitivas. O sistema foi **iterado a partir do uso real**.

## 📊 Dados de exemplo
`data/sample/movimentacoes_exemplo.csv` contém uma amostra anonimizada e normalizada das respostas.
Campos:
| Campo | Descrição |
|---|---|
| `data_hora` | Data e hora do registro |
| `movimentacao` | Entrada ou saída |
| `produto` | Produto movimentado |
| `quantidade_litros` | Quantidade registrada |
| `talhao` | Destino da aplicação |
| `outra_fazenda` | Outra origem/destino, quando aplicável |
| `responsavel` | Responsável pelo movimento, anonimizado |

## 📱 Formulário utilizado na operação
O AgroStock utilizava um **Google Forms acessado por QR Code** no local de armazenamento. O formulário foi desenvolvido para que os responsáveis pela pulverização pudessem registrar a movimentação diretamente pelo celular, sem precisar acessar a planilha de controle.

O formulário coletava informações como:
- entrada ou saída do produto;
- produto e quantidade;
- destino da aplicação/talhão;
- outra fazenda, quando aplicável;
- responsável pela movimentação;
- observação, quando necessária;
- data e hora, registradas automaticamente.

O formulário atualmente está **desativado e não é mais utilizado na operação**. Ele pode ser consultado como documentação da interface que fez parte do projeto.
**Formulário original:** https://docs.google.com/forms/d/e/1FAIpQLSd4kLj-qIPZHM1EBU2Z3mxC2kzrUFxL_1G3LjtcpoJHr_Fh9Q/viewform?usp=header

### 📊 Visualização das respostas
Além da coleta, o próprio Google Forms disponibilizava, para os **administradores**, uma prévia dos dados registrados por meio de gráficos e resumos das respostas.
Essas visualizações permitiam observar rapidamente informações como:
- distribuição dos destinos/talhões;
- movimentações para outras fazendas;
- quantidade de respostas;
- informações registradas no campo de observações.

![Exemplo da visualização das respostas do formulário](docs/images/graficos-respostas-formulario.png)
> **Observação:** os gráficos apresentados acima são uma documentação da interface administrativa do formulário. O acesso às respostas era restrito aos administradores do formulário.

## 🗂️ Estrutura
```text
agrostock/
├── data/
│   └── sample/
│       └── movimentacoes_exemplo.csv
├── docs/
│   └── fluxo.md
├── src/
│   └── transformar_respostas.py
├── tests/
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## 🛠️ Tecnologias e ferramentas
- Google Forms
- QR Code
- Google Sheets / Excel
- Python
- Pandas
- Git / GitHub

## 🚀 Evolução planejada
O projeto pode evoluir de uma solução baseada em formulário + planilha para uma aplicação de controle de estoque:
- normalização automática dos produtos;
- validação de quantidade;
- saldo por produto;
- histórico de movimentações;
- alertas de estoque mínimo;
- dashboard em Power BI ou Streamlit;
- banco de dados SQL;
- autenticação de usuários;
- trilha de auditoria;
- integração com APIs;
- geração de relatórios.

## 📌 Aprendizados
Este projeto demonstra uma aplicação prática de tecnologia no agronegócio, principalmente em:
- levantamento de problema no ambiente rural;
- automação de coleta de dados;
- estruturação e limpeza de dados;
- rastreabilidade de movimentações;
- melhoria de processo;
- análise de dados;
- integração entre operação de campo e controle administrativo.

## 🔐 Privacidade
Não publicar no GitHub:
- respostas completas do formulário;
- nomes reais de funcionários;
- localização detalhada de talhões;
- informações comerciais ou de estoque real;
- links de formulários operacionais privados;
- credenciais, tokens ou chaves de API.

Para demonstração pública, utilize dados fictícios ou anonimizados.
## 📄 Licença
MIT License




