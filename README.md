# Instance Template e Instance Group Load Balancer

## Criar um Instance Template usando a ferramenta <b>'gcloud'</b>:
<table>
	<ol>
		<li>Primeiro, certifique-se de ter o SDK do Google Cloud instalado em sua máquina e faça login na sua conta do GCP.
			<br>
		<li>Abra o terminal ou prompt de comando e execute o seguinte comando para criar um Instance Template:
	</ol>
</table>

	gcloud compute instance-templates create nome-template \
	    --machine-type tipo-maquina \
	    --image-family familia-imagem \
	    --image-project projeto-imagem \
	    --boot-disk-size tamanho-disco-inicial \
	    --network-interface network-tier=PREMIUM

<table>
	<ul>
		<li>Substitua <b>nome-template</b> pelo nome que deseja dar ao seu Instance Template.
			<br>
		<li>Substitua <b>tipo-maquina</b> pelo tipo de máquina que você deseja usar (por exemplo, n1-standard-1).
			<br>
		<li>Substitua <b>familia-imagem</b> e <b>projeto-imagem</b> pela família e projeto da imagem que você deseja usar.
			<br>
		<li>Substitua <b>tamanho-disco-inicial</b> pelo tamanho do disco inicial em GB.
			<br>
		<li>A opção <b>--network-interface network-tier=PREMIUM</b> é opcional e define a camada da rede. Você pode ajustar conforme necessário.
	</ul>
</table>

## Agora, para criar um Instance Group Load Balancer, siga estas etapas:
<table>
	<ol>
		<li>No console do GCP, navegue até a seção "Instance Groups".
			<br>
		<li>Clique em "Criar grupo de instâncias".
			<br>
		<li>Selecione "Criar um novo grupo de instâncias".
			<br>
		<li>Preencha as informações solicitadas, como nome, região/zona, número de instâncias e selecione o Instance Template que você criou anteriormente.
			<br>
		<li>Na seção "Configurações de balanceamento de carga", selecione "Balanceamento de carga de rede" como tipo de balanceamento de carga.
			<br>
		<li>Siga as etapas restantes para configurar opções adicionais, como política de escalonamento automático e firewall, conforme necessário.
			<br>
		<li>Clique em "Criar" para criar o Instance Group Load Balancer.
	</ol>
</table>