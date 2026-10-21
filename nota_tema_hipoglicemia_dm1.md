# Nota de pesquisa — mestrado profissional

## Alerta personalizado de risco de hipoglicemia em diabetes tipo 1

Proposta de software embarcado/IoT com dados de relógio inteligente e CGM durante a calibração.

| Aspecto | Descrição |
| --- | --- |
| Recorte | Personalização com poucos dados para cada pessoa. |
| Aplicação | Alerta antecipado de risco; não substitui medição de glicose. |
| Artefato | Protótipo de coleta, inferência local e avaliação experimental. |
| Aderência | Computação aplicada, IoT, IA embarcada, privacidade e saúde digital. |

## Resumo rápido

Tema sugerido: investigar como adaptar um modelo de aprendizado de máquina a uma pessoa com diabetes tipo 1 usando poucos dias de dados de um relógio inteligente e de um CGM. O sistema aprende padrões individuais de frequência cardíaca/variabilidade, atividade, sono e contexto para emitir um alerta antecipado de risco de hipoglicemia.

O ponto central não é medir glicose sem sensor. O CGM funciona como referência e rótulo durante uma fase curta de calibração; o produto de pesquisa é a estratégia de personalização e a execução local do alerta. Assim, uma necessidade real vira um problema de computação aplicada avaliável.

## O que já existe — e onde está a oportunidade

| Evidência existente | Limite atual | Espaço de pesquisa |
| --- | --- | --- |
| Previsão com CGM | Há modelos consolidados a partir de séries de glicose. | Comparar adaptação global, local e por transferência com poucos dados. |
| Relógio + CGM | Há estudo personalizado com Apple Watch e CGM, em escala pequena. | Testar sistematicamente 1, 3, 7, 14 e 30 dias de calibração. |
| IA embarcada | Há demonstrações de previsão executada em celular. | Projetar pipeline simples, local e com dados minimizados na nuvem. |

**Síntese:** o tema é promissor porque combina um problema clínico concreto com uma lacuna computacional clara: personalizar modelos multimodais com poucos dados, preservando privacidade e utilidade prática.

## Pergunta de pesquisa e hipótese

**Pergunta:** qual estratégia de adaptação individual produz alertas mais úteis de risco de hipoglicemia quando há apenas poucos dias de dados de uma nova pessoa?

**Hipótese:** um modelo multimodal pré-treinado, ajustado com 3–14 dias de dados pessoais, pode superar um modelo global e um modelo treinado do zero, reduzindo falsos alertas sem perder sensibilidade a eventos.

## Desenho de pesquisa viável

- **Base inicial:** usar bases públicas antes de qualquer coleta própria. A OhioT1DM reúne CGM, insulina, alimentação, exercício, sono, estresse, trabalho e sinais de wearable; HUPA-UCM oferece um conjunto adicional para validação.
- **Comparação:** baseline global; modelo local treinado do zero; ajuste fino/transfer learning; e, se o volume permitir, meta-learning. Separar pessoas e períodos no treino/teste para evitar vazamento.
- **Métricas orientadas ao uso:** sensibilidade por evento, falsos alertas por dia, antecedência do alerta, AUROC/precisão e calibração da probabilidade.
- **Protótipo:** aplicativo Android ou serviço local no celular, com coleta autorizada do relógio, inferência leve no dispositivo e tela de explicação simples dos sinais de risco.

## Delimitação e cuidado ético

O sistema deve ser apresentado como apoio à pesquisa e alerta de risco. Não deve orientar dose de insulina, substituir CGM/glicosímetro nem ser usado como dispositivo médico sem validação clínica e regulatória. Coleta própria com participantes exige aprovação ética, consentimento e apoio de profissional de saúde.

## Aderência ao PPGCA

A proposta entrega um artefato mensurável: pipeline de sensores, modelo de personalização, inferência embarcada e protocolo de avaliação. Ela conversa diretamente com sistemas embarcados, IoT, desempenho/confiabilidade e inteligência artificial aplicada — perfil adequado a um mestrado profissional. A orientação pode ser buscada com docentes de IoT/redes ou sistemas embarcados/robótica; a aderência final depende da disponibilidade e do edital vigente.

## Referências principais para começar

1. Mohamed, Y. M. et al. (2025). *Personalized machine learning models for noninvasive hypoglycemia detection in people with type 1 diabetes using a smartwatch*. PLOS ONE, 20(6), e0325956. [https://doi.org/10.1371/journal.pone.0325956](https://doi.org/10.1371/journal.pone.0325956)
2. Zhu, T. et al. (2022). *Enhancing self-management in type 1 diabetes with wearables and deep learning*. npj Digital Medicine, 5, 78. [https://doi.org/10.1038/s41746-022-00626-5](https://doi.org/10.1038/s41746-022-00626-5)
3. Zhu, T. et al. (2023). *Personalized Blood Glucose Prediction for Type 1 Diabetes Using Evidential Deep Learning and Meta-Learning*. IEEE Transactions on Biomedical Engineering, 70. [PubMed](https://pubmed.ncbi.nlm.nih.gov/35776825/)
4. Tsichlaki, E.; Koumakis, L.; Tsiknakis, M. (2022). *Type 1 Diabetes Hypoglycemia Prediction Algorithms: Systematic Review*. JMIR Diabetes, 7(3), e34699. [https://doi.org/10.2196/34699](https://doi.org/10.2196/34699)
5. Marling, C.; Bunescu, R. (2020). *The OhioT1DM Dataset for Blood Glucose Level Prediction: Update 2020*. [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC7881904/)
6. [OhioT1DM Dataset — documentação e dados](https://webpages.charlotte.edu/rbunescu/data/ohiot1dm/OhioT1DM-dataset.html).
7. [HUPA-UCM diabetes dataset — Mendeley Data](https://data.mendeley.com/datasets/3hbcscwz44/1).
8. Shao, Y. et al. (2024). *Generalization of a Deep Learning Model for Continuous Glucose Monitoring-Based Hypoglycemia Prediction*. JMIR Medical Informatics, 12, e56909. [https://doi.org/10.2196/56909](https://doi.org/10.2196/56909)
9. Brasil. [Plataforma Brasil — submissão ética de pesquisas envolvendo seres humanos](https://www.gov.br/pt-br/servicos/submeter-na-plataforma-brasil-de-projetos-de-pesquisa-envolvendo-seres-humanos-para-avaliacao-etica).
10. U.S. FDA (2024). [Do not use smartwatches or smart rings to measure blood glucose levels](https://www.fda.gov/medical-devices/safety-communications/do-not-use-smartwatches-or-smart-rings-measure-blood-glucose-levels-fda-safety-communication).

**Leitura sugerida:** as referências 1–3 tratam diretamente de wearable, personalização ou execução móvel; as 4–8 sustentam revisão, dados e avaliação; as 9–10 ajudam a manter o escopo ético e de segurança bem delimitado.
