# Discord 2 Transmissor 1.0.0 — Linux amd64

Primeira versão estável do aplicativo GTK para compartilhar tela/janela e áudio com salas do Discord 2 público. Os espectadores continuam assistindo pelo navegador, sem instalação.

- Instalação `.deb`, ícone D2 e abertura pelo menu Aplicativos.
- GTK, captura autorizada pelo portal Wayland/PipeWire, GStreamer e SDK nativo LiveKit.
- Perfis 720p30, 1080p30 e 1080p60, sem reduzir silenciosamente a qualidade escolhida.
- Seleção de monitores válidos de saída, nomes amigáveis, atualização dos dispositivos e preferência pela saída padrão. Sem seleção automática de microfone.
- Iniciar, Parar e encerramento da janela com liberação de recursos e controle exclusivo de transmissão.
- Uso dos convites e autenticação existentes, sem chaves privadas no cliente.

**Validado manualmente:** instalação e abertura pelo menu no Pop!_OS; imagem e áudio reais recebidos no celular pelo site público; parada, reinício e encerramento funcionando. Integrações automatizadas também verificaram exclusividade e recuperação da vaga após queda abrupta em sala isolada.

**Compatibilidade validada:** Pop!_OS 24.04, COSMIC/Wayland, amd64/x86_64. **Windows ainda não é compatível.** Outras distribuições não verificadas. FPS efetivo, latência e capacidade de 1080p60 dependem do hardware; não se promete uma taxa medida universal.

**Áudio:** reprodução local preservada; chamadas na mesma saída podem ser capturadas. Compartilhar uma janela não restringe o áudio àquela janela. Não há isolamento de eco por aplicativo garantido.

Arquivos para download:

- `discord2-transmissor_1.0.0_amd64.deb`
- `SHA256SUMS`

SHA-256 do instalador:

```text
b0e2ad6b4b5356aca469a1e39e1cf799c4d53d275c204d782d2704438c12a1c9
```

Instalação/atualização, após baixar os dois arquivos na mesma pasta:

```sh
sha256sum --check SHA256SUMS
sudo apt install ./discord2-transmissor_1.0.0_amd64.deb
```

O instalador inclui componentes de execução Python/JavaScript do cliente; sua distribuição não inclui o site/backend. Licenças dos componentes de terceiros acompanham o pacote.
