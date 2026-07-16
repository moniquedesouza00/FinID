## FinID: Terminal de Análise Molecular Forense
O **FinID** é uma aplicação web de caráter educacional que simula um *pipeline* de genômica forense. A ferramenta foi projetada para demonstrar a aplicação do DNA Barcoding no combate ao *shark finning* (comércio ilegal de barbatanas de tubarão), operando através da identificação molecular de tecidos degradados interceptados em contexto aduaneiro.

Devido à degradação ou excisão das características morfológicas fenotípicas durante o processamento ilegal da carcaça, a taxonomia clássica torna-se inviável. Esta aplicação fundamenta-se no protocolo de **DNA Barcoding (Código de Barras de DNA)**, adotando como marcador o fragmento do gene mitocondrial **Citocromo C Oxidase Subunidade I (COI)**.

O veredito de embargo ou liberação da carga é processado computacionalmente com base no grau de ameaça da espécie identificada, de acordo com as métricas da **Lista Vermelha da IUCN**.

## Arquitetura do Pipeline Simulado
A interface gamificada orienta o usuário através das etapas essenciais de uma análise pericial:
1. **Extração e Amplificação:** Simulação da lise celular, extração genômica e amplificação *in vitro* (PCR) do *locus* alvo.
2. **Sequenciamento de Nova Geração (NGS):** Geração do *output* bruto de nucleotídeos em formato estruturado (FASTA).
3. **Alinhamento Heurístico:** Execução de alinhamento par a par (*pairwise alignment*) entre a *query* (amostra desconhecida) e *subjects* de um banco de dados de referência (simulando a plataforma *BOLD Systems*).
4. **Veredito Jurídico:** Tomada de decisão fundamentada nos dados moleculares cruzados com a legislação de conservação ambiental.

## Ferramentas
O projeto segue uma arquitetura estática e monolítica no *front-end*, garantindo alta compatibilidade e execução nativa via *browser* sem a necessidade de infraestrutura de servidor:
* **HTML5:** Estruturação semântica e modal de autenticação operacional.
* **CSS3:** Estilização responsiva baseada em paleta de contraste, com tipografia customizada para renderização de dados de sequenciamento.
* **JavaScript:** Lógica condicional, algoritmos de *match* genômico e controle de estado do ambiente interativo.

## Como Executar Localmente
Por ser uma aplicação baseada inteiramente em tecnologias web padrão, a inicialização não requer configuração de ambiente (*setup*).
1. Realize o clone deste repositório:
   ```bash
   git clone [https://github.com/moniquedesouza00/FinID.git](https://github.com/moniquedesouza00/FinID.git)
