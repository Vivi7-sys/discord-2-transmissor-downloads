# Discord 2 Transmissor para Linux

Instalador desktop **1.0.0** para transmitir tela/janela e áudio para salas do [Discord 2](https://discord-2-kuau.onrender.com/). Espectadores assistem pelo navegador, inclusive no celular, sem instalar o aplicativo.

**Compatibilidade validada:** Pop!_OS 24.04, COSMIC/Wayland, processador amd64/x86_64. Outras distribuições e ambientes gráficos **não foram verificados**. Este instalador não atende ARM/ARM64 nem x86 de 32 bits.

## Instalar ou atualizar

Em [Releases](https://github.com/Vivi7-sys/discord-2-transmissor-downloads/releases/latest), baixe os dois arquivos da versão 1.0.0:

- `discord2-transmissor_1.0.0_amd64.deb`
- `SHA256SUMS`

Na pasta dos downloads, abra um terminal:

```sh
sha256sum --check SHA256SUMS
sudo apt install ./discord2-transmissor_1.0.0_amd64.deb
```

Prossiga com a instalação somente se a verificação mostrar `OK`. O apt resolve as dependências declaradas do sistema; pode precisar de acesso à internet. Feche a versão anterior antes de reabrir pelo menu.

## Transmitir

1. Abra **Discord 2 Transmissor** no menu Aplicativos, pelo ícone D2.
2. Crie uma sala no site Discord 2 e cole o convite completo no aplicativo. Informe seu nome.
3. Escolha Tela ou Janela, qualidade e áudio. O monitor validado da saída padrão é oferecido inicialmente; você pode escolher outra saída ou **Sem áudio**.
4. Clique **Selecionar e iniciar** e autorize a seleção no portal do sistema.
5. Compartilhe o convite com os espectadores. Para encerrar e liberar a vaga, clique **Parar** ou feche a janela. Para reiniciar, clique em iniciar novamente.

Perfis: 720p/30, 1080p/30 e 1080p/60. O desempenho efetivo depende do computador; a qualidade escolhida não é reduzida automaticamente. Não há reconexão/captura automática após queda da rede.

## Áudio e privacidade

Nada é capturado antes de iniciar. Microfones não são oferecidos no seletor. A reprodução local é preservada. **Chamadas e outros programas que tocam na mesma saída podem entrar na transmissão**, mesmo ao selecionar somente uma janela. Não há isolamento de eco por aplicativo garantido. Separe as saídas caso precise excluir chamadas; não é necessário silenciar participantes. Evite reproduzir o próprio espectador na saída capturada.

Somente um transmissor pode publicar por sala. O controle da sala e o limite de seis participantes continuam no servidor. Chaves privadas do serviço não são incluídas no instalador.

## Remover

```sh
sudo apt remove discord2-transmissor
```

Diagnósticos salvos explicitamente pelo usuário permanecem em `~/.local/state/discord2-transmissor/diagnostics`.

Este repositório é destinado à distribuição do instalador e documentação; não contém o repositório de desenvolvimento do site/backend. O pacote inclui componentes de execução do cliente em Python e JavaScript, que podem ser extraídos, além das bibliotecas e licenças de terceiros.
