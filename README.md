# Otimização de rotas e tomada de decisão com Pyomo e mapas reais 

Nos últimos dias, desenvolvi um projeto integrando mapas reais (OpenStreetMap) com modelagem matemática no Pyomo para resolver um problema clássico de logística: como distribuir produtos de um Centro de Distribuição (CD) para diferentes locais de forma ótima, respeitando demandas, capacidades e distâncias reais.

A ideia foi trazer um problema de transporte realista, semelhante ao que empresas de logística, varejo e supply chain enfrentam todos os dias e, aplicar técnicas de Pesquisa Operacional para encontrar a melhor forma de entrega.

# Tecnologias utilizadas:
Pyomo (para a formulação e solução do modelo de otimização);
OSMnx + NetworkX (para obtenção e análise de mapas reais);
Folium (para visualização interativa das rotas);
Python como linguagem principal de integração e análise.

# Resultados: 
 O modelo identifica as melhores rotas e quantidades a enviar de cada CD para cada local, minimizando os custos de transporte e garantindo que todas as restrições logísticas sejam satisfeitas. Sabendo apenas a localização dos locais a serem abastecidos, o modelo também identifica o melhor local para colocar um CD. Esse tipo de abordagem mostra o poder da Ciência de Dados aplicada à Logística, unindo teoria, programação e tomada de decisão, exatamente o tipo de solução que impulsiona a eficiência nas operações do mundo real.
