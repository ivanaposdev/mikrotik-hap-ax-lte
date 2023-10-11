# Mikrotik hAP ax lite LTE6
Notes on configuring the LTE interface of this router

## LTE Interface Specifications
- Model: FG621-EA
- Rev: 16121.1034.00.01.01.03

### Cell Locking 

**Command:**  
```
AT+GTCELLLOCK=<mode>[,<rat>,<type>,<earfcn>[,<PCI>]]

where

< mode >: integer type; 0 Disable this function 1 Enable this function 2 Add new cell to be locked

<rat>: integer type; 0 LTE 1 WCDMA

<type>: integer type; 0 Lock PCI 1 Lock frequency

<earfcn>: integer type; the range is 0-65535.

<PCI>: integer type; If the second parameter value is 0, the range is 0-503 for LTE If the second parameter value is 1, the range is 0-512 for WCDMA
```

Reference: https://help.mikrotik.com/docs/display/ROS/LTE#LTE-UsingCelllock

**Example:**  

`> interface lte at-chat lte1 input="AT+GTCELLLOCK=1,0,0,150,344"`
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/72d3b23e-f9d7-475b-a51f-7b4f78351bef)

**Primary Band will now be locked to the desired cell:**  
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/72b00da4-3ea9-459e-b20c-bd9f75ec7cd6)

