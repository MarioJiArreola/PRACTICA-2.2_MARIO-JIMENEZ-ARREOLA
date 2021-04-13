# PRACTICA-2.2_MARIO-JIMENEZ-ARREOLA 
#NOMBRE:MARIO JIMENEZ ARREOLA
#CARRERA:ING INFORMATICA 
#MATERIA: DESARROLLO DE APLICACIONES WEB 
#PRACTICA 2.2

fecha=input("fecha (formato 'dia,  DD/MM'): ") 
fecha=fecha.lower() 
diasemana=fecha [0:fecha.find(',')] 
dianro=int(fecha [fecha.find(' ')+1:fecha.find('/')] ) 
mesnro=int(fecha[fecha.find( '/')+1:])  
if dianro>31 or mesnro>12:
   print("fecha incorrecta")
else: 
    if diasemana in  "lunes, martes , miercoles":
        respuesta=input("¿se tomaron examenes? S/N: ")
        if respuesta.lower()== "s": 
            aprobados=int(input ("cantidad de aprobados:")) 
            reprobados=int(input ("cantidad de reprobados:")) 
            print ("porcentaje de aprobados:" , (aprobados*100)/(aprobados+reprobados) , "%")
    elif diasemana == "jueves": 
        asistencia=int(input("porcentaje de asistencia:")) 
        if asistencia>50:
            print("asistio la mayoria") 
        else:
            print("no asistio la mayoria") 
    elif diasemana == "viernes": 
        if dianro==1 and (mesnro==1 or mesnro==7):
            print("comienzo de nuevo ciclo")  
            alumnos=int(input ("cantidad de alumnos:"))
            arancel=float(input("Arancel: $"))
            print("Ingreso total: $", alumnos*arancel)     
    else:
           print("fecha incorrecta")

print("fin del programa")  

