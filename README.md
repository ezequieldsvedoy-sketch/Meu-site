# FS20 Editor — Protótipo 0.1

## O que funciona neste protótipo
- Visualizador 3D interativo com um caminhão demonstrativo construído com primitivas.
- Arrastar para girar e zoom.
- Ajustes demonstrativos de raio do pneu, largura, aro, posição e cor do aro.
- Ajustes simples de escala/altura de algumas peças do modelo demonstrativo.
- Importação local de ZIP no navegador, listagem de arquivos e análise inicial da sintaxe XML.
- Exportação de ZIP com os arquivos importados preservados e arquivos de relatório/parâmetros.

## Limitações importantes
- O modelo 3D exibido é demonstrativo; não é um modelo real do Farming Simulator.
- Ainda não importa nem interpreta modelos `.i3d`/`.i3d.shapes` do jogo.
- Os controles de rodas alteram o modelo demonstrativo, mas não gravam as mudanças dentro de um modelo I3D.
- Não reescreve scripts Lua, não converte formatos 3D proprietários e não garante compatibilidade com FS20.
- A exportação é um pacote de análise/protótipo, não um mod convertido pronto para o jogo.
- A biblioteca Three.js e JSZip são carregadas de CDN; é necessária conexão à internet na primeira abertura e para carregar essas bibliotecas.

## Testar rápido no Android
1. Extraia `fs20-editor-prototype.zip`.
2. Para testar sem instalar nada, publique a pasta em um host estático HTTPS (por exemplo, GitHub Pages) e abra o endereço no Chrome Android.
3. No Chrome, menu `⋮` > **Adicionar à tela inicial** ou **Instalar app**, se a opção aparecer.
4. Para desenvolvimento local no Termux, instale Python e rode um servidor na pasta:
   ```bash
   pkg update
   pkg install python -y
   cd /caminho/para/fs20-editor-prototype
   python -m http.server 8080
   ```
   Depois abra `http://127.0.0.1:8080` no navegador do mesmo celular. A interface funciona em HTTP local; a instalação PWA completa pode exigir HTTPS.

## Próximos passos
- Importador real de I3D usando uma biblioteca/ferramenta compatível.
- Conversores específicos para XML e texturas com regras por versão.
- Histórico de alterações e validação de referências de arquivos.
- Empacotamento Android (APK) depois de validar a experiência web.
