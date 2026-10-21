# Detecção personalizada de hipoglicemia em diabetes tipo 1

A proposta é estudar como adaptar um modelo existente a uma pessoa com diabetes tipo 1 usando poucos dados individuais. O modelo usaria sinais de um relógio inteligente, como frequência cardíaca, atividade e sono, para identificar risco de hipoglicemia. Durante a coleta, um CGM (monitor contínuo de glicose) serviria como referência para reconhecer os episódios reais.

A pergunta central é: **quanto de dados de uma pessoa é necessário para adaptar o modelo e melhorar a detecção de hipoglicemia?**

Na prática, compararíamos um modelo geral, um modelo adaptado à pessoa e um modelo treinado apenas com os dados dela. A avaliação consideraria episódios detectados, falsos alertas por dia e, se houver previsão antecipada, o tempo de antecedência. O período necessário de coleta seria investigado, sem assumir previamente que dois meses ou poucos dias bastam.

A contribuição para o mestrado seria avaliar estratégias de personalização com poucos dados e construir um protótipo de alerta no celular, unindo IoT e computação aplicada. O relógio não mediria diretamente a glicose, e o protótipo não substituiria o monitoramento nem as decisões de tratamento.

## Referências principais do documento original

- Mohamed et al. (2025). Modelos personalizados para detecção de hipoglicemia com smartwatch: https://doi.org/10.1371/journal.pone.0325956
- Zhu et al. (2022). Wearables e aprendizado profundo no diabetes tipo 1: https://doi.org/10.1038/s41746-022-00626-5
- Tsichlaki et al. (2022). Revisão de algoritmos de previsão de hipoglicemia: https://doi.org/10.2196/34699
