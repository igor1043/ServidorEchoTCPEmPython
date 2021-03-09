
# ServidorEchoTCPEmPython
Lado servidor TCP


Python
## Sobre este repositório

O Python implementa a interface de rede utilizando os fundamentos da API de Socket.
Todo socket pode estar em modo ativo ou passivo.
Quando ele é criado ele esta no modo ativo.
Para o servidor poder ficar “escutando” um porta é necessário colocar o socket do servidor em modo passivo.
Seqüência no Cliente:
Se foi fornecido um nome de hospedeiro converter em endereço IP;
Se foi fornecido um nome de protocolo de transporte converter em número;
Criar o socket (função socket);
Conecta com o servidor (função connect);
Enviar/Receber dados (permanecer nesse passo enquanto tiver dados para enviar/receber);
Fechar o socket.
Seqüência no Servidor:
Se foi fornecido um nome de protocolo de transporte converter em número;
Criar o socket (função socket);
Coloca um endereço local, endereço IP e porta, no socket (função bind);
Instrui o sistema operacional para colocar o socket em modo passivo (função listen);
Aceita uma nova conexão (função accept);
Enviar/Receber dados (permanecer nesse passo enquanto tiver dados para enviar/receber);
Fechar o socket.
Volta ao passo 5 para aceitar outra conexão.
Os passos 4 e 5 do servidor são feito quando utilizamos protocolo de transporte orientado a conexão (TCP).
O servidor tipicamente fica em laço infinito aceitando novas conexões.
Enquanto o servidor atende uma conexão ele fica dedicado a ela. Para evitar isso é possível fazer um passo intermediário entre o 5 e o 6 para criar um novo processo ou thread para tratar da nova conexão que esta chegando. Com isso o processo/thread pai fica somente recebendo as conexões e o processo/thread filho trata das requisições dos clientes.

## Autor

* Igor Vincius Freitas de Souza
