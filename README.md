# dio-lab-AzureAI-LanguageStudio

O Processamento de Linguagem Natural (PNL) é um ramo da IA ​​que lida com a linguagem escrita e falada. Você pode usar a PNL para construir soluções que extraiam significado semântico de texto ou fala, ou que formulem respostas significativas em linguagem natural.

Por exemplo, suponha que a agência de viagens fictícia Margie's Travel incentive os clientes a enviar avaliações sobre estadias em hotéis. Você pode usar o serviço de idiomas para identificar frases-chave, determinar quais avaliações são positivas e quais são negativas ou analisar o texto da avaliação em busca de menções a entidades conhecidas, como locais ou pessoas.

O Azure AI Language Service inclui análise de texto e recursos de PNL. Isso inclui a identificação de frases-chave no texto e a classificação do texto com base no sentimento.

## Objetivo
O propósito deste exercício foi explorar os recursos da linguagem do Microsoft Azure AI (Azure AI Language Service) analisando um exemplo de avaliação de hotel. Nele utilizamos o Language Studio para entender se as avaliações são em sua maioria positivas ou negativas.


## Descrição das etapas
Os testes foram realizados de acordo com o lab fornecido pela Microsoft e disponível no seguinte link: [text-analysis](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/06-text-analysis.html).

A texto utilizado como entrada na análise é o mesmo apresentado no guia do laboratório e também foi disponibilizado no arquivo textoAnalizado.md adicionado ao diretório "inputs" deste repositório.

## Resultados
Os resultados em formato JSON obtidos da análise do texto são os apresentados a seguir:

```
{
    "documents": [
        {
            "id": "id__1066",
            "sentiment": "negative",
            "confidenceScores": {
                "positive": 0,
                "neutral": 0.03,
                "negative": 0.96
            },
            "sentences": [
                {
                    "sentiment": "negative",
                    "confidenceScores": {
                        "positive": 0,
                        "neutral": 0.01,
                        "negative": 0.98
                    },
                    "offset": 0,
                    "length": 219,
                    "text": " Tired hotel with poor service  The Royal Hotel, London, United Kingdom  5/6/2018  This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. ",
                    "targets": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0.01,
                                "negative": 0.99
                            },
                            "offset": 7,
                            "length": 5,
                            "text": "hotel",
                            "relations": [
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/0/assessments/0"
                                }
                            ]
                        },
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0.01,
                                "negative": 0.99
                            },
                            "offset": 23,
                            "length": 7,
                            "text": "service",
                            "relations": [
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/0/assessments/1"
                                }
                            ]
                        }
                    ],
                    "assessments": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0.01,
                                "negative": 0.99
                            },
                            "offset": 1,
                            "length": 5,
                            "text": "Tired",
                            "isNegated": false
                        },
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0.01,
                                "negative": 0.99
                            },
                            "offset": 18,
                            "length": 4,
                            "text": "poor",
                            "isNegated": false
                        }
                    ]
                },
                {
                    "sentiment": "negative",
                    "confidenceScores": {
                        "positive": 0,
                        "neutral": 0.01,
                        "negative": 0.99
                    },
                    "offset": 219,
                    "length": 102,
                    "text": "The internet didn't work and had to come to one of their office rooms to check in for my flight home. ",
                    "targets": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0,
                                "negative": 1
                            },
                            "offset": 223,
                            "length": 8,
                            "text": "internet",
                            "relations": [
                                {
                                    "relationType": "assessment",
                                    "ref": "#/documents/0/sentences/1/assessments/0"
                                }
                            ]
                        }
                    ],
                    "assessments": [
                        {
                            "sentiment": "negative",
                            "confidenceScores": {
                                "positive": 0,
                                "negative": 1
                            },
                            "offset": 239,
                            "length": 4,
                            "text": "work",
                            "isNegated": true
                        }
                    ]
                },
                {
                    "sentiment": "negative",
                    "confidenceScores": {
                        "positive": 0.01,
                        "neutral": 0.08,
                        "negative": 0.91
                    },
                    "offset": 321,
                    "length": 76,
                    "text": "The website says it's close to the British Museum, but it's too far to walk.",
                    "targets": [],
                    "assessments": []
                }
            ],
            "warnings": []
        }
    ],
    "errors": [],
    "modelVersion": "2022-11-01"
}


```
