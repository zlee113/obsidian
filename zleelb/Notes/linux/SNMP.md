Date: 2024-08-15
Hub: [[networking]]
Tags: #web 
URL/Title: https://www.datadoghq.com/knowledge-center/network-monitoring/snmp-monitoring/#what-is-snmp

Simple standardized network monitoring with several components:
1. SNMP Manager: Server or process polling network devices
2. SNMP Agent: Software client stores device status and relay when polled.
3. Managed Device: Network device that has an snmp agent
4. Management Information base (MIB): Dictionary of info for each device, with each object identifier and its human readable definition.
5. Object Identifier (OID): Address on device that specifies a specific piece of info, ie fan speed or temperature. Allows network engineer to extract useful info.

Common SNMP commands:
- Get: Queries SNMP Agent based on OID
- Response: Agent retrieves requested OID and sends to manager
- GetNext: Gets value of next OID in MIB tree