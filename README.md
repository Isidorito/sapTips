# sapTips
## Repo de handy notes para SAP

**Prog para desbloquear OT liberadas.**
- RDDIT076 (Pasar a Status D)

**FM para skippear Authority Checks.**
- RS_HDSYS_CALL_TC_VARIANT
  
**Calcular cantidad de entradas de una tabla interna.**
```
variable = lines( itab_name ).
 ```
 
**BatchInput Modes**

- A--> All display
- E--> Errors display
- N--> No display

**Recuperar variables del stack**
```
data: lw_field(30).
FIELD-SYMBOLS <fs> TYPE STANDARD TABL
lw_field = '(SAPLMEPO)POT[]'.
ASSIGN (lw_field) TO <fs>.
```

**Buscar strings en muchos programas**

- RPR_ABAP_SOURCE_SCAN

**Obtener nombre de SAP User**

- Tabla USER_ADDRP

**FM Para agregar entradas en tabla SIN SM30**

- SE16N_INTERFACE
