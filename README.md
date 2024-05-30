#Utilize o serviço nip.io para não mexer no arquivo hosts

#Crie um diretório cert, e gere um certificado
openssl req -newkey rsa:4096 -nodes -sha256 -keyout 192.168.10.40.crt

#Faça os apontamentos em volumes para os diretórios que serão necessários para subir os serviços
´´html, nginx e cert´´

#Copie o arquivo default.conf do nginx para ssl.conf, e o edite.  Após isso, ao subir o compose, o SSL já estará ativo.

#Foram adicionadas algumas linhas no arquivo ssl.conf, a fim de aumentar a segurança, registrando o endereço e o protocolo de utilizados nas requisições.