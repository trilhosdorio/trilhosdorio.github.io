# trilhosdorio.github.io
Trilhos do Rio - um mapa de todas as ferrovias do Rio de Janeiro, antigas e atuais

![Trilhos do Rio](https://pbs.twimg.com/profile_images/624678576789581824/8ztuGMT1.png)

## Convenções de arquivo

Todos os arquivos GeoJSON de linhas devem ter as seguintes propriedades:

    {
        "name": "nome atual da ferrovia, ou último nome, quando ferrovia desativada"
        "description": "descrição contando um resumo"
        "type": "railway para ferrovias, tramway para bondes",
        "status": "status atual da ferrovia, uma das palavras a seguir:
                   operational_passengers: em operação com passageiros
                   operational_tourism: em operação turística
                   operational_cargo: em operação de cargas
                   construction: em construção, ainda que paralisada
                   disused: em condições regulares, mas sem operação regular (passa auto de linha)
                   abandoned: abandonada, mas ainda com a via visível
                   razed: totalmente destruída, sem trilhos"
        "gauge": "bitola da ferrovia em mm, somente número (ex: 1600)",
        "ref": "EF-XXX, se for o caso",
        "opening_date": "data no formato YYYY-MM-DD da data de inauguração da ferrovia. pode ser apenas YYYY."
        "closing_date": "data de encerramento de operações comerciais da ferrovia. pode ser apenas YYYY."
        "construction_start_date": "data do começo das obras.",
        "operator": "Operador da ferrovia, como SuperVia, MRS etc.",
        "tracks": "single se for via simples, double se for via duplicada",
        "electrified": "yes ou no",
        "historic": [
            {
                // se este bloco historic for usado, repetir como último elemento o nome atual da ferrovia
                "name": "Nome antigo da ferrovia",
                "begin": "YYYY-MM-DD ou YYYY",
                "end": "YYYY-MM-DD ou YYYY"
            }
        ],
        "historic_gauge": [
            {
                // se este bloco historic_gauge for usado, repetir como último elemento a bitola atual da ferrovia
                "gauge": "XXXX",
                "begin": "YYYY-MM-DD",
                "end": "YYYY-MM-DD"
            }
        ]
    }
