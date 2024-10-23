Estrutura do EA baseado no TTrades OSOK Model

## 1. Identificação do Swing (Swing High/Low):❗️
      - O EA deve identificar swings no gráfico, baseado em três velas consecutivas (Candle 1, Candle 2, Candle 3).
      - Um Swing High ocorre quando a Candle 2 forma uma máxima maior que a Candle 1 e 3.
      - Um Swing Low ocorre quando a Candle 2 forma uma mínima menor que a Candle 1 e 3.
   
## 2. **Confirmação do Swing (CISD)**:❌
      - Após a formação do Swing High ou Low, o EA deve validar uma mudança de estrutura (Change in State of Delivery, CISD) na timeframe inferior (por exemplo, Swing em 1H -> CISD em 5M).
      - Essa confirmação acontece com a quebra de uma série de velas de fechamento opostas.
   
## 3. **Projeção de Alvos**:❌
      - A partir da perna de manipulação, o EA deve projetar alvos de expansão. Isso é feito usando projeções padrão, como -2R e -4R (múltiplos de risco), e outras zonas de liquidez identificadas.
   
## 4. **Entradas**:❌
      - O EA deve realizar entradas após a confirmação de um CISD, usando o preço de abertura da vela seguinte após a confirmação.
      - O Stop Loss (SL) deve ser definido no Swing High ou Swing Low mais recente.
      - O Take Profit (TP) deve ser baseado em um múltiplo de risco mínimo de 2:1.
   
## 5. **Trailing Stop**:❌
      - O EA deve implementar uma lógica de trailing stop, movendo o SL para cima ou para baixo conforme o preço se desloca a favor da posição, usando a estrutura de candles opostos (opposing close candles) e swings confirmados.
   
## 6. **Gerenciamento de Notícias**:❌
      - O EA deve evitar abrir trades em dias com notícias de alto impacto, especialmente notícias relacionadas ao USD (como NFP e CPI), seguindo as regras descritas no documento para o calendário econômico.
   
## 7. **Perfis Semanais e Diários**:❌
      - O EA deve operar preferencialmente nos dias de maior expansão, evitando segundas-feiras (segundo a regra do modelo OSOK) e focando em confirmações durante as sessões de Londres e Nova York.
   
## 8. **Regras de Confirmação de Entrada**:❌
      - As entradas só devem ser feitas após a confirmação do Swing e do CISD em timeframes mais baixos, com preferência por reversões durante as sessões relevantes (como a reversão de Nova York).
   
   Com esses pontos como base, o próximo passo seria codificar essa lógica em MQL5 (linguagem usada no MetaTrader 5). Posso ajudar a construir esse código passo a passo ou ajustar um código existente, caso você tenha algo que gostaria de modificar.
