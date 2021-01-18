## 11 de novembro, 2020
criação do arquivo
## 23 de novembro, 2020
revisão básica do ROS
- Criação e configuração do ambiente;
- Criação e construção de packages;
- ROS Nodes;
- ROS Topics;
-  ```rqt``` visualização de dados e debug e  uso do roslaunch para inciar varios nodes;
## 24 de novembro, 2020

**arquivos msg (message file)**

Arquivos de texto que contem tipos e nomes de variáveis.

**arquivos srv (service file)**

Serviços são como msg files porém dividem as variáveis em solicitação e resposta.

---
Sempre usar ```. ~/catkin_ws/devel/setup.bash``` no terminar apos iniciar a maquina para iniciar o ambiente e os comandos direcionado ao ROS (```roscd```, ```rospack```, etc) funcionarem.

Para criar srv e msg é necessario alterar partes do ```package.xml``` e do ```CMakeLists.txt```.

Erro no catkin_make causado pela falta do package em python ```empy```.

## 12-16 de Janeiro, 2021
-Incompatibilidade do ROS com biblioteca em Python de Speech Recognition DeepSpeech
-Estudo mais aprofundado dos packages do ROS, versões e incopatibilidades.
No ROS Kinetic Kame o ```catkin_make``` usa python2.7/c++ para montar os packages, portanto nodes criados em outras versões python podem causar problemas na criação dos packages
-O suporte a python2.7 acabou em 31/12/2020
