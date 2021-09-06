# 1- CREACION-DE-GRUPOS-Y-USUARIOS
# Describe el proceso de crear grupos y usuarios en linux. 
# el proceso lo haremos desde el usuario root

# 1-  Crear un grupo llamado casa
    sudo groupadd CASA 
# Consultamos si el grupo fue creado 
    cat /etc/group
    
# 2- Dentro del grupo CASA crear 2 usuarios, uno con el
# nombre de su papá o mamá y el otro usuario seria su
# nombre.
    sudo useradd MARTINA -g CASA 
    sudo useradd JUAN -g CASA
    passwd MARTINA 
    12345 
    passwd JUAN 
    12345 
# verificar los usuarios agregados al grupo.
    cut -d: -f1,4 /etc/passwd
    
# 3- Luego cambiar el nombre del grupo casa a Familia.
    sudo groupmod -n FAMILIA CASA 
# Verificamos si se ha efectuado el cambio 
    sudo cat /etc/group 

        



