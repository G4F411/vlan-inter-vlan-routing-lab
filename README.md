# vlan-inter-vlan-routing-lab
Laboratório de redes no Cisco Packet Tracer com VLANs, trunk 802.1Q e roteamento inter-VLAN (Router-on-a-Stick).

Visão Geral
Projeto prático desenvolvido no Cisco Packet Tracer com o objetivo de segmentar uma rede em múltiplas VLANs, permitir comunicação inter-VLAN por meio de Router-on-a-Stick e validar conectividade utilizando boas práticas de troubleshooting.
________________________________________
Objetivos
•	Criar e configurar VLANs em um switch Layer 2
•	Configurar trunk 802.1Q entre switch e roteador
•	Implementar Router-on-a-Stick para roteamento inter-VLAN
•	Configurar endereçamento IP estático nos hosts
•	Validar conectividade (PC ↔ Gateway ↔ Inter-VLAN)
•	Diagnosticar e corrigir falhas comuns de configuração
________________________________________
 Topologia
•	1 Switch Layer 2 (Cisco)
•	1 Roteador (Cisco)
•	4 PCs
•	VLAN 10 — Administrativo
•	VLAN 20 — Financeiro
________________________________________
Tecnologias e Conceitos
•	VLAN
•	Trunk 802.1Q
•	Router-on-a-Stick
•	Endereçamento IPv4
•	Troubleshooting com comandos show e ping
________________________________________
Configuração (Resumo Técnico)
VLANs no Switch
•	VLAN 10 criada e associada às portas Fa0/2 e Fa0/3
•	VLAN 20 criada e associada às portas Fa0/4 e Fa0/5
Trunk
•	Porta Fa0/1 configurada como trunk 802.1Q
•	VLANs permitidas no trunk: 10,20
Router-on-a-Stick
•	Interface física Gi0/0 ativa
•	Subinterface Gi0/0.10 → 192.168.10.1/24
•	Subinterface Gi0/0.20 → 192.168.20.1/24
Endereçamento dos Hosts
•	VLAN 10
o	PC (Fa0/2): 192.168.10.10/24 — Gateway 192.168.10.1
o	PC (Fa0/3): 192.168.10.11/24 — Gateway 192.168.10.1
•	VLAN 20
o	PC (Fa0/4): 192.168.20.10/24 — Gateway 192.168.20.1
o	PC (Fa0/5): 192.168.20.11/24 — Gateway 192.168.20.1
________________________________________
 Validação e Testes
•	Ping PC ↔ próprio IP (validação local)
•	Ping PC ↔ Gateway em cada VLAN
•	Ping Inter-VLAN (VLAN 10 ↔ VLAN 20)
Resultado: conectividade total validada.
________________________________________
 Troubleshooting Realizado
Durante o desenvolvimento, foram identificadas e corrigidas falhas comuns em ambientes reais:
•	Trunk ativo sem VLANs permitidas (ajuste em switchport trunk allowed vlan)
•	Associação incorreta entre PC e porta do switch
•	Validação de status de interfaces e VLANs com comandos show
Esse processo reforçou a metodologia correta de diagnóstico por camadas.
________________________________________
Resultados Obtidos
•	Rede segmentada corretamente por VLANs
•	Comunicação inter-VLAN funcional
•	Ambiente configurado seguindo boas práticas
•	Consolidação de conceitos fundamentais de redes
________________________________________
 Conclusão
Este projeto demonstra a aplicação prática de conceitos essenciais de redes, indo além da simples configuração, com foco em entendimento, diagnóstico e validação do ambiente.
Projeto desenvolvido para fins de estudo e portfólio profissional.

