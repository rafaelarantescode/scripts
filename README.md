Instalando o Typebot com Dominio
 
#======================= Instalação Typebot simplificada com dominio

Link para pegar 2 meses com 200 dolares de crédito na Digital Ocean
https://m.do.co/c/4c3958677512

Registre um dominio (qualquer provedora)

Dominio .fun custa 5 reais


Transfira o dominio para a Cloudflare (altere os nameservers para os fornecidos pela Cloudflare)
https://www.cloudflare.com/



Espere o apontamento ser concluido (leva algumas horas), faça as seguintes alterações na Cloudflare:
Edge Certificates (Certificados de borda) --> Marcar Always use HTTPS (Sempre use HTTPS)
SSL/TLS --> Flexible



Crie os seguintes registros A em DNS na Cloudflare e desative o Proxy Reverso:
typebot.seudominio seu_ip_vps
bot.seudominio seu_ip_vps
storage.seudominio seu_ip_vps



Vamos agora para a sua VPS
sudo apt update
sudo apt install git -y
git clone https://github.com/JohnnyLove777/typebotrelampagossh.git
cd typebotrelampagossh
chmod +x installtypessh.sh
./installtypessh.sh

