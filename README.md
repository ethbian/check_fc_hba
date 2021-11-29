# check_fc_hba
Nagios/Icinga plugin that checks FC HBA (Fibre Channel Host Bus Adapter) status and speed.

It's a simple bash script that makes sure all your HBA ports are working fine:


```
Usage: 
 ./check_fc_hba
   -s (speed in Gbit, default: 8)
   -n (number of FC ports, default: 2)
   -o (number of Online FC host, default = number of FC ports)

   example: expecting 2 FC ports with 16 Gbit speed, all should be Online:
   ./check_fc_hba -n 2 -s 16

   output: CRITICAL when wrong number of FC ports or port state not being Online
           WARNING when speed different from expected

```

