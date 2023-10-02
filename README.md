# Mikrotik hAP ax lite LTE6
Notes on configuring the LTE interface of this router

## LTE Interface Specifications
- Model: FG621-EA
- Rev: 16121.1034.00.01.01.03
  
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/5fdf2a91-6d49-49b8-815d-1e6fd08d6ced)

### Cell Locking 

**Command:**  
`> interface lte at-chat lte1 input="AT+GTCELLLOCK=1,0,0,150,344"`

**Example:**  
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/dae5bd09-f101-4d3d-916e-a31a0c346bc5)

**Primary Band will now be locked:**  
![image](https://github.com/ivanaposdev/mikrotik-hap-ax-lte/assets/113334411/92fb104b-871a-44fc-b31c-90cbe3fb709b)
