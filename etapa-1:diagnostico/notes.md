Buscar:
- variáveis de observação.
- Coletar dados em horários de pico.
- Tecnologias de coleta de dados.
	- Monitores de Hardware
	- Monitores de Software

## Monitores de Software

### RMF
- Registra tudo que passa no Software
	- Altamente preciso.
- Pecam em overhead - chegado a impactar 15% do CPU.
	- Memória, Disco, Processador, 
- Devem ser orientados quando se busca precisão.

### SMF
- O sistema é observado de tempos em tempos.
- Não são exatos e podem ser redundantes.
- Comercialmente mais utilizados.

### Tempo de observação (T0)
- qual o período em que se observa

### Período de amostragem (Ts)
- qual a frequência em que se observa.

#### Dicotomia 
Diagnóstico vs Modelagem Matemática de Sistema

##### Para diagnóstico
- Não existem fortes restrições (T0 = 30min, 1h, etc) e Ts = 2,3 e 5s.
- Se o sistema está ruim, não abaixar demais o Ts.
- Recomendações:
	- Não extrapolar o horário de pico para não abaixar a média.
	- Respeitar sempre que possível a **Hipótese do Equilíbrio de Fluxo**.
		- O que entra deveria ser igual ao que sai. **
			- O que significa sair?
		- Sobrecarga:
			- Falta de memória
			- Falta de processamento
			- Natureza da aplicação
		- E se o tempo de equilíbrio demorar:
			- Criar janelas deslizantes um obtenção de equiíbrio de fluxo hábil.
			- Criar tolerância de 10% de equilíbrio.
				- Não tem problema - podem já estar no sistema.

#### Para fim de diagnóstico
- Diagrama de sequenciamento.
	- Quantidade total de requisições.
- Nada pode ser definido previamente.
- Ajustes dos parâmetros precisam respeitar Equilibro de Fluxo (HEF) e TransiçÕes Unitárias (HTU)
	- Se gráfico de sequenciamento não apresenta trasações unitárias, Ts está mto alto.

#### Visualização e Análise de Dados coletados
Tempo de resposta: acompanha carga
utilização: 100% próximo de acompanhar o sistema.
paginação: ir para disco -> 10Mx mais lentos

Sistemas não pode ficar à mercê da carga de trabalho.

TODO: resposta para infra-estrutura local.
Offline: solicitações online - run job.
Horário batch -> processamento offline.

Nuvem: On-line é cobrado conforme a natureza.

Manter estruturas separadas para isso.

Carga online: gera receita para empresa

Manter estabilidade do sistema.

Gráfico mensal: é possível de avaliar batches vs online.

##### Dicotomia de comprar vs otimizar hardware **
- se as métricas estão ruins, otimização.
- se as métricas estão boas, hora de investir em hardware.

##### Graus de incerteza
- Será que a otimização está no máximo valor.

##### Comunicação com Empresa
- Transparência sobre o método de diagnóstico.

## Próxima Etapa: Identificação de horário de pico.

