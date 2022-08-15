# Prueba
Espacio donde estare practicando el proceso para el GITHUB
# POR FAVOR LEA TODAS LAS INDICACIONES SUMINISTRADAS EN EL 
# ENUNCIADO ANTES DE EMPEZAR A IMPLEMENTAR SU SOLUCIÓN

# NO MODIFICAR LOS NOMBRES, PARÁMETROS DE ENTRADA NI RETORNOS DE LAS FUNCIONES
# USE LOS MISMOS NOMBRES DE LOS RETORNOS PARA NOMBRAR LOS RESULTADOS QUE SU FUNCIÓN DEBE GENERAR

def veterinaria(nombres, tipos, edades, pesos):
    # ACÁ INICIA LA FUNCIÓN VETERINARIA
    # (En este espacio debe poner el código necesario para crear los diccionarios y promedios pedidos)
    diccionario={}
    beneficiarios_can_fel={}
    beneficiarios_equ_bov={}
    promedio_can_fel=0
    promedio_equ_bov=0
    j=0
    k=0
            
    for i in range(0,len(nombres)):
        diccionario[str(i+1)]=nombres[i],tipos[i],edades[i],pesos[i]
        
    for i in range(0,len(nombres)):
        if tipos[i]=="canino" or tipos[i] == "felino" and edades[i]>=9:
            j=j+1
            beneficiarios_can_fel[str(j)]=nombres[i],tipos[i],edades[i],pesos[i]
            promedio_can_fel=promedio_can_fel+edades[i]
                
    for i in range(0,len(nombres)):
        if tipos[i]=="equino" or tipos[i] == "bovino" and edades[i]>=16:
            k=k+1
            beneficiarios_equ_bov[str(k)]=nombres[i],tipos[i],pesos[i],edades[i]
            promedio_equ_bov=promedio_equ_bov+edades[i]

    if len(beneficiarios_can_fel)!=0:    
        promedio_can_fel=promedio_can_fel/len(beneficiarios_can_fel)
    else:
        promedio_can_fel=None

    if len(beneficiarios_equ_bov)!=0:       
        promedio_equ_bov=promedio_equ_bov/len(beneficiarios_equ_bov)
    else:
        promedio_equ_bov=None
    return diccionario, beneficiarios_can_fel, beneficiarios_equ_bov, promedio_can_fel, promedio_equ_bov   
# ACÁ TERMINA LA FUNCIÓN VETERINARIA
# NO MODIFIQUE LA SIGUIENTE LÍNEA
