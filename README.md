# Fuel Calculator

Aplicativo Android desenvolvido em Kotlin para estimar o custo de uma viagem com base no preço do combustível, no consumo médio do veículo e na distância percorrida.

## Como funciona

O usuário percorre estas etapas:

1. Informa o preço do combustível por litro.
2. Informa o consumo médio do veículo em km/L.
3. Informa a distância da viagem em quilômetros.
4. Confere o custo estimado, o preço por litro, o consumo e a distância.

As telas permitem voltar à etapa anterior pela seta da barra superior. Na tela final, o botão **Calcular Novamente** retorna ao início.

## Cálculo

O código calcula primeiro os litros necessários dividindo a distância pelo consumo e, em seguida, multiplica esse valor pelo preço por litro:

```text
Litros necessários = distância ÷ consumo
Custo estimado = litros necessários × preço por litro
```

O resultado monetário é exibido em reais, com formatação brasileira (`pt-BR`).

> **Precisão do cálculo:** atualmente, distância e consumo são tratados como números inteiros. A divisão também é inteira, então a fração de litro é descartada antes do cálculo do custo. Por isso, o resultado pode ficar abaixo do custo calculado com casas decimais.

## Tecnologias

- Kotlin
- Android SDK
- Android Studio
- Gradle com arquivos de configuração Kotlin DSL
- Material Components para a barra de navegação

## Estrutura principal

```text
app/src/main/java/com/example/fuelcalculator/
├── MainActivity.kt
├── PrecoCombustivelActivity.kt
├── ConsumoPorLitroActivity.kt
├── DistanciaActivity.kt
└── ResultadoActivity.kt

app/src/main/res/layout/
├── activity_main.xml
├── activity_preco_combustivel.xml
├── activity_consumo_por_litro.xml
├── activity_distancia.xml
└── activity_resultado.xml
```

## Como abrir e executar

1. Clone o repositório ou baixe o código-fonte.
2. No Android Studio, escolha **File → Open** e selecione a pasta do projeto.
3. Aguarde a sincronização do Gradle.
4. Selecione um emulador Android ou conecte um celular com a depuração USB ativada.
5. Clique em **Run** para compilar e executar o aplicativo.

## Exemplo

Com combustível a R$ 5,00/L, consumo de 12 km/L e distância de 600 km:

```text
Litros necessários = 600 ÷ 12 = 50
Custo estimado = 50 × R$ 5,00 = R$ 250,00
```

## Projeto acadêmico

Projeto criado para praticar o desenvolvimento de aplicativos Android com Kotlin.
