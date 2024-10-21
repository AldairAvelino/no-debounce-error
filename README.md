# Botão Sem Erro De Debounce

Debounce é o processo de eliminar ou reduzir os efeitos de oscilações elétricas que podem ocorrer quando um botão de pressão é pressionado ou liberado. Essas oscilações são causadas pela natureza mecânica dos botões, que podem saltar ou vibrar por um curto período de tempo antes de fazerem um contato elétrico sólido.

## Problemática
Quando você liga um botão a um pino digital do Arduino e tenta ler seu estado, se o botão foi (**pressionado** ou **não pressionado**) diretamente, você pode enfrentar problemas de **instabilidade**. 

> [!TIP]
> O Arduino é tão rápido em ler os estados que pode capturar essas oscilações momentâneas como múltiplos pressionamentos ou liberações do botão, levando a resultados inconsistentes.

## Solução
Existem várias maneiras de resolver esse problema:

1. **Hardware debounce:** você pode usar componentes eletrônicos, como resistores de _pull-up_ ou _pull-down_ e _capacitores_, para poder criar um circuito de **debouncer no hardware**. Isso filtra as oscilações antes mesmo de chegarem ao Arduino.

> [!NOTE]
> O uso de um capacitor em paralelo ao botão é uma técnica comum para criar esse filtro.</li>

2. **Software debounce:** isso envolve a escrita de código que ignora leituras de botões que ocorrem muito rapidamente após uma mudança de estado inicial.

> [!WARNING]
> Você pode implementar o debounce no teu código _Arduino_.

3. **Bibliotecas de debounce:** existem bibliotecas prontas disponíveis para Arduino, como a **Bounce2**, que facilitam a implementação do debounce de software.

Lidar com o problema de debounce é importante, sempre que você estiver trabalhando com botões de pressão para garantir a precisão das leituras. 

> [!TIP]
> A abordagem que você escolher dependerá das necessidades do seu projeto e da sua preferência pessoal.
