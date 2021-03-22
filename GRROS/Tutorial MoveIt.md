# Objetivos

O objetivo desse tutorial é mostrar o passo a passo da instalação da versão MoveIt1 - Kinetic 
e a execução da trajetoria de um ponto de início até um local desejado.

# Instalação dos requisitos

### ROS e Catkin

1. [Seguir os passos de instalação do ROS Kinetic para UBUNTU](http://wiki.ros.org/kinetic/Installation/Ubuntu)
2. [Seguir os passos para instalação do MoveIt e a criação de um espaço de trabalho Catkin](http://docs.ros.org/en/kinetic/api/moveit_tutorials/html/doc/getting_started/getting_started.html)

# Introdução do MoveIt no RViz

Usar o plugin RViz é a maneira mais rápida de introdução para uso do MoveIt.

### Passos para um primeiro contato e configuração do ambiente

#### 1. Iniciando a demonstração

```shell
roslaunch panda_moveit_config demo.launch rviz_tutorial:=true
```

![image](https://user-images.githubusercontent.com/32770973/111983853-5c91bc80-8ae9-11eb-9844-afbba18186af.png)

essa é a imagem que deverá aparecer na primeira execução.

#### 2. No "Displays Tab" apertar o botão "Add"

![image](https://user-images.githubusercontent.com/32770973/111984944-c65e9600-8aea-11eb-9308-8acf3a6efdb9.png)

#### 3. Selecionar da pasta "moveit_ros_visualization" a opção “MotionPlanning” e pressionar "OK".

![image](https://user-images.githubusercontent.com/32770973/111985753-cdd26f00-8aeb-11eb-9561-199f09f7db53.png)

Agora você consegue ver um braço robótico aparecendo na tela do RViz como na imagem abaixo

![image](https://user-images.githubusercontent.com/32770973/111986089-3e798b80-8aec-11eb-8f18-f8b08b70a275.png)

#### 4. Setar o campo "Fixed Frame" para "/panda_link0"

![image](https://user-images.githubusercontent.com/32770973/111986927-4ede3600-8aed-11eb-8bfd-3861fb69f182.png)

#### 5. Configurações do Plugin

* Assegurar que o campo "Robot Description" esta setado em  "robot_description"

![image](https://user-images.githubusercontent.com/32770973/111987585-2acf2480-8aee-11eb-8797-20efd64e4ff7.png)

* Assegurar que o campo " Planning Scene Topic" esta setado em "/planning_scene"

![image](https://user-images.githubusercontent.com/32770973/111988249-032c8c00-8aef-11eb-8dcb-ebef450391e1.png)

* Na pasta "Planning Request" mudar o campo "Planning Group" para "panda_arm"

![image](https://user-images.githubusercontent.com/32770973/111988636-7d5d1080-8aef-11eb-9768-2c3be72b04ff.png)

* Na pasta "Planned Path" mude o campo "Trajectory Topic" para "/move_group/display_planned_path"

![image](https://user-images.githubusercontent.com/32770973/111989268-54894b00-8af0-11eb-9796-435c7880e4e4.png)

#### 6. Interação com o Panda

* Na pasta "Planned Path" marque a opção "Show Robot Visual"

![image](https://user-images.githubusercontent.com/32770973/111989938-2ce6b280-8af1-11eb-9265-093b922541ba.png)

* Na pasta "Scene Robot" desmarque a opção "Show Robot Visual"

![image](https://user-images.githubusercontent.com/32770973/111990236-ec3b6900-8af1-11eb-8692-1c4411674647.png)

* Na pasta "Planning Request" marque a opção "Query Goal State"

![image](https://user-images.githubusercontent.com/32770973/111991010-987d4f80-8af2-11eb-89fa-bd2d651d103b.png)

* Na pasta "Planning Request" marque a opção "Query Start State"

![image](https://user-images.githubusercontent.com/32770973/111991299-ea25da00-8af2-11eb-846e-ac03e862d86c.png)

A partir desse momento você pode interagir com a posição de começo e fim do robô clicando e arrastando nas setas
e circulos ao redor de cada garra, como visto na imagem abaixo

![image](https://user-images.githubusercontent.com/32770973/111991743-65878b80-8af3-11eb-8b34-432823b0def4.png)

