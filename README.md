# Instance Template e Instance Group Load Balancer

## Criar um Instance Template usando a ferramenta <b>'gcloud'</b>:
<table>
	<ol>
		<li>Primeiro, certifique-se de ter o SDK do Google Cloud instalado em sua máquina e faça login na sua conta do GCP.
		<br>
		Abra o terminal ou prompt de comando e execute o seguinte comando para criar um Instance Template:
		<li>
	</ol>
</table>

	gcloud compute instance-templates create nome-template \
	    --machine-type tipo-maquina \
	    --image-family familia-imagem \
	    --image-project projeto-imagem \
	    --boot-disk-size tamanho-disco-inicial \
	    --network-interface network-tier=PREMIUM
