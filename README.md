# Botão Sem Erro De Debounce

Debounce é o processo de eliminar ou reduzir os efeitos de oscilações elétricas que podem ocorrer quando um botão de pressão é pressionado ou liberado. Essas oscilações são causadas pela natureza mecânica dos botões, que podem saltar ou vibrar por um curto período de tempo antes de fazerem um contato elétrico sólido.

## Problemática
Quando você liga um botão a um pino digital do Arduino e tenta ler seu estado (pressionado ou não pressionado) diretamente, você pode enfrentar problemas de instabilidade. O Arduino é tão rápido em ler os estados que pode capturar essas oscilações momentâneas como múltiplos pressionamentos ou liberações do botão, levando a resultados inconsistentes.

## Como Resolver o Problema de Debounce:
<p>Existem várias maneiras de resolver esse problema:</p>

<ol>
  <li><strong>Hardware debounce:</strong> Você pode usar componentes eletrônicos, como resistores de pull-up ou pull-down e capacitores, para criar um circuito de debounce no hardware. Isso filtra as oscilações antes mesmo de chegarem ao Arduino. O uso de um capacitor em paralelo ao botão é uma técnica comum para criar esse filtro.</li>

  <li><strong>Software debounce:</strong> Você pode implementar o debounce no código do Arduino. Isso envolve a escrita de código que ignora leituras de botões que ocorrem muito rapidamente após uma mudança de estado inicial.</li>

  <li><strong>Bibliotecas de debounce:</strong> Existem bibliotecas prontas disponíveis para Arduino, como a "Bounce2", que facilitam a implementação do debounce de software.</li>
</ol>

<p>Lidar com o problema de debounce é importante sempre que você estiver trabalhando com botões de pressão para garantir a precisão das leituras. A abordagem que você escolher dependerá das necessidades do seu projeto e da sua preferência pessoal.</p>
