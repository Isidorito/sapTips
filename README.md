# sapTips
## Repo de handy notes para SAP

**Prog para desbloquear OT liberadas.**
- RDDIT076 (Pasar a Status D) [No existe en las nuevas versiones]

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

**Editar datos en tabla SE16N**

- /h
- Estructura: GD
- Colocar X en
  - SAPEDIT
  - EDIT

**Remover caracteres de String**
- Remover letras:
```
  REPLACE ALL OCCURRENCES OF REGEX '([[:alpha:]])' IN string WITH ''.
```
- Remover números:
```
  REPLACE ALL OCCURRENCES OF REGEX '([[0-9]])' IN string WITH ''.
```

**Texto para Pop Up debug**
Crear un .txt con el siguiente código
```
[FUNCTION]
Command=/H
Title=Debugger
Type=SystemCommand
```

**FM para convertir a formato de texto**
Pasa de una tabla con múltiples columnas a una tabla de una sola columna.
```
    DATA: lt_download TYPE truxs_t_text_data.

    CALL FUNCTION 'SAP_CONVERT_TO_TEX_FORMAT'
      EXPORTING
        i_field_seperator    = ','
      TABLES
        i_tab_sap_data       = it_final
      CHANGING
        i_tab_converted_data = lt_download
      EXCEPTIONS
        conversion_failed    = 1
        OTHERS               = 2.
```

**Hacer editable los campos XREF1 - XREF2 - XREF3 en la MIRO**
 - Prog: LMR1MF6Q
 - Form: MODIFY_FI_SCREEN
