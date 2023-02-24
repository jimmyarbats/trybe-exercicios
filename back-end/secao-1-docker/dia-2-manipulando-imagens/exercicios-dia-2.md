<!--
1. Crie um Dockerfile utilizando a imagem chuanwen/cowsay.
2. Defina um ENTRYPOINT para a execução do comando.
3. Utilize o CMD para definir uma mensagem padrão.
4. Gere uma build e execute um container baseado em sua imagem sem passar nenhum comando.
5. Execute um novo container passando sua mensagem para testar. Além da mensagem você pode utilizar a opção -l para listar outros personagens disponíveis e então executar algo como docker container run cowsay -f dragon-and-cow "VQV TRYBE", para exibir um dragão junto com a vaquinha. -->

1:
FROM chuanwen/cowsay:latest
2:
ENTRYPOINT [ "/usr/games/cowsay" ]
3:
CMD [ "#VQV Trybe" ]
4:
docker image build ./ -t cowsay
5:
docker container run cowsay