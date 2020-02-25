Upload instructions

Integrator  >  Integrator Name: 
FNDLOAD apps/<<password>> 0 Y UPLOAD $BNE_TOP/patch/115/import/bneintegrator.lct XXFND_USR_RESPONSIBILITY.ldt UPLOAD_MODE=REPLACE CUSTOM_MODE=FORCE

Function    > Function Name:  XX ADI User Responsibility
FNDLOAD apps/<<password>>  0 Y UPLOAD $FND_TOP/patch/115/import/afsload.lct XXINTEGRATOR_FUNC.ldt

Function → Responsibility Assignment
Assign function created above to responsibility of your choice.



Download Instructions after modifications

Intergrator & Layouts
FNDLOAD apps/<<password>> 0 Y DOWNLOAD $BNE_TOP/patch/115/import/bneintegrator.lct XXFND_USR_RESPONSIBILITY.ldt BNE_INTEGRATORS INTEGRATOR_ASN="SYSADMIN" INTEGRATOR_CODE="XXFND_USR_RESPONSIBILITY"
  
Oracle Function
FNDLOAD apps/apps 0 Y DOWNLOAD $FND_TOP/patch/115/import/afsload.lct XX_CUSTOM_FUNC.ldt FUNCTION FUNCTION_NAME="XX_FND_USR_RESP_ADI"
