# Instalacion de Alpine y Docker
## 1.Instalacion de Alpine
### 1. Nada mas entrar antes de empezar a instalar nos pedira que asignemos un usuario y una contraseña al equipo .

[![imagen-2022-05-01-013930440.png](https://i.postimg.cc/Dw6NGT08/imagen-2022-05-01-013930440.png)](https://postimg.cc/21qTpg4D)

### 2. Mediante el comando *setup-alpine* elegimos el layout de teclado que deseamos y la Zona horaria.

[![imagen-2022-05-01-030415688.png](https://i.postimg.cc/5yzMwNkw/imagen-2022-05-01-030415688.png)](https://postimg.cc/0K93vxvQ)

[![imagen-2022-05-01-030655842.png](https://i.postimg.cc/yxmb1Jbr/imagen-2022-05-01-030655842.png)](https://postimg.cc/N204b0Y1)

### 3. Nos pedira las 3 siguientes cosas que *mirror* queremos, el *ssh* que deseamos y el *disco duro* al cual queremos instalarle alpine.

[![imagen-2022-05-01-031913822.png](https://i.postimg.cc/nV3dkJtm/imagen-2022-05-01-031913822.png)](https://postimg.cc/c68MxPC1)

### 4. Ya tendremos instalado Alpine.

[![imagen-2022-05-01-033137719.png](https://i.postimg.cc/7PC5h3X2/imagen-2022-05-01-033137719.png)](https://postimg.cc/4ngfFhDf)

## 2. Instalacion de Docker
### 1. Cambiamos el adaptador de red de nuestra maquina virtual a adaptador puente.

[![imagen-2022-05-01-164320046.png](https://i.postimg.cc/L59k8C7d/imagen-2022-05-01-164320046.png)](https://postimg.cc/ftPSHKD5)

### 2. Para poder interconectar nuestras maquinas debemos hacer los siguientes pasos.
#### 1. Mediante el comando *vi /etc/ssh/sshd_config* accederemos a la configuracion del ssh.

[![imagen-2022-05-01-165419354.png](https://i.postimg.cc/50Rvf4wz/imagen-2022-05-01-165419354.png)](https://postimg.cc/MM1XD83Z)

#### 2. Nos situaremoe en el 27% de la pagina y cambiaremos *#PermitRootLogin prohibit password* a *PermitRootLogin yes*.

[![imagen-2022-05-01-165810678.png](https://i.postimg.cc/TwgLvVYz/imagen-2022-05-01-165810678.png)](https://postimg.cc/tZRChV6k)

#### 3. Mediante el comando *service sshd restart* reiniciaremos el sshd.

[![imagen-2022-05-01-170242884.png](https://i.postimg.cc/HLZDWRj5/imagen-2022-05-01-170242884.png)](https://postimg.cc/jW7kZ8Hd)

#### 4. Mediante el comando *ip a* comprobaremos la ip que tenemos. 

[![imagen-2022-05-01-170930837.png](https://i.postimg.cc/tCWs1t37/imagen-2022-05-01-170930837.png)](https://postimg.cc/PPfX9DFk)

### 3. Abrimos git e introducimos el comando *ssh root@"nuestra correspondiente ip"* en mi caso sera *ssh root@192.168.1.146*  y la correspondiente contraseña.

[![imagen-2022-05-01-185213418.png](https://i.postimg.cc/W4JwWYxj/imagen-2022-05-01-185213418.png)](https://postimg.cc/f3DdkCwg)

### 4. Mediante el comando *vi /etc/apk/repositories* entraremos a donde estan guardados los repositorios y retiraremos los # que estan escritos excepto el primero de todos.

[![imagen-2022-05-01-190301697.png](https://i.postimg.cc/J46FSgYB/imagen-2022-05-01-190301697.png)](https://postimg.cc/rK4grhk8)

### 5. Mediante el comando *apk add docker* instalaremos docker.

[![imagen-2022-05-01-190638900.png](https://i.postimg.cc/vB07cRVr/imagen-2022-05-01-190638900.png)](https://postimg.cc/LYZgbbv5)

### 6. Mediante el comando *service docker start* iniciaremos el servicio de docker.

[![imagen-2022-05-01-190957601.png](https://i.postimg.cc/G26FkFXt/imagen-2022-05-01-190957601.png)](https://postimg.cc/R6QJmH5x)

### 7. Para finalizar usaremos el comando *docker run hello-world* lo cual realizara un pull que al acabar nos mostrara el siguente mensaje que nos afirmara que nuestra instalacion se ha realizado correctamente:

[![imagen-2022-05-01-191515350.png](https://i.postimg.cc/J4fF1Jm1/imagen-2022-05-01-191515350.png)](https://postimg.cc/LnVDDJn7)
