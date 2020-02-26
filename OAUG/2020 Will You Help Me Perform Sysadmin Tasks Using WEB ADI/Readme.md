# Upload instructions

### Integrator  >  Integrator Name: 
FNDLOAD apps/<<password>> 0 Y UPLOAD $BNE_TOP/patch/115/import/bneintegrator.lct XXFND_USR_RESPONSIBILITY.ldt UPLOAD_MODE=REPLACE CUSTOM_MODE=FORCE

### Function    > Function Name:  XX ADI User Responsibility
FNDLOAD apps/<<password>>  0 Y UPLOAD $FND_TOP/patch/115/import/afsload.lct XXFND_USR_RESP_ADI_FUNC.ldt


### Lookup for Action Type Lovs
FNDLOAD apps/<<password>> O Y DOWNLOAD $FND_TOP/patch/115/import/aflvmlu.lct XX_ACTION_RESP_USR_CREATE_LOOKUP.ldt FND_LOOKUP_TYPE APPLICATION_SHORT_NAME="SYSADMIN" LOOKUP_TYPE="XX_ACTION_RESP_USR_CREATE"

### Function → Responsibility Assignment
Assign function created above to responsibility menu of your choice.
 


# Download Instructions after modifications

### Intergrator & Layouts

FNDLOAD apps/<<password>> 0 Y DOWNLOAD $BNE_TOP/patch/115/import/bneintegrator.lct XXFND_USR_RESPONSIBILITY.ldt BNE_INTEGRATORS INTEGRATOR_ASN="SYSADMIN" INTEGRATOR_CODE="XXFND_USR_RESPONSIBILITY"
  
### Oracle Function

FNDLOAD apps/<<password>> 0 Y DOWNLOAD $FND_TOP/patch/115/import/afsload.lct XXFND_USR_RESP_ADI_FUNC.ldt FUNCTION FUNCTION_NAME="XX_FND_USR_RESP_ADI"


### Lookup for Action Type Lovs
FNDLOAD apps/<<password>> O Y UPLOAD $FND_TOP/patch/115/import/aflvmlu.lct XX_ACTION_RESP_USR_CREATE_LOOKUP.ldt UPLOAD_MODE=REPLACE CUSTOM_MODE=FORCE

