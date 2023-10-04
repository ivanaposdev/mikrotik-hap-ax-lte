# Mikrotik hAP ax lite LTE6
Notes on configuring the LTE interface of this router

## LTE Interface Specifications
- Model: FG621-EA
- Rev: 16121.1034.00.01.01.03
  
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/5fdf2a91-6d49-49b8-815d-1e6fd08d6ced)

### Cell Locking 

**Command:**  
```
AT+GTCELLLOCK=<mode>[,<rat>,<type>,<earfcn>[,<PCI>]]

where

< mode >: integer type; 0 Disable this function 1 Enable this function 2 Add new cell to be locked

<rat>: integer type; 0 LTE 1 WCDMA

<type>: integer type; 0 Lock PCI 1 Lock frequency

<earfcn>: integer type; the range is 0-65535.

<PCI>: integer type; If second parameter value is 0, the range is 0-503 for LTE If second parameter value is 1, the rang is 0-512 for WCDMA
```

Reference: https://help.mikrotik.com/docs/display/ROS/LTE#LTE-UsingCelllock

**Example:**  

`> interface lte at-chat lte1 input="AT+GTCELLLOCK=1,0,0,150,344"`
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/dae5bd09-f101-4d3d-916e-a31a0c346bc5)

**Primary Band will now be locked to the desired cell:**  
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/92fb104b-871a-44fc-b31c-90cbe3fb709b)
