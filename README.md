# Maratona 2027 — PWA offline para iPhone

## Publicar gratuitamente no GitHub Pages

1. Entre em https://github.com e crie um repositório público, por exemplo `maratona-2027`.
2. Envie **o conteúdo desta pasta** para a raiz do repositório, mantendo `index.html`, `sw.js`, `manifest.webmanifest`, `.nojekyll` e a pasta `icons/`. Não envie somente o ZIP.
3. Em **Settings → Pages**, escolha **Deploy from a branch**, branch **main**, pasta **/(root)** e clique em **Save**.
4. Aguarde a publicação e abra `https://SEU-USUARIO.github.io/maratona-2027/` no Safari do iPhone.
5. Toque em **Compartilhar → Adicionar à Tela de Início → Adicionar**. Se aparecer **Abrir como App**, mantenha habilitado.
6. Abra o ícone instalado **com internet pelo menos uma vez**. Depois ative o modo avião e teste a abertura e um registro de treino.

## Persistência e backup

- Registros são armazenados no `localStorage` do navegador para o endereço de instalação.
- Use **Backup → Exportar backup JSON** pelo menos uma vez por semana e salve o arquivo no iCloud Drive.
- Para recuperar dados, use **Backup → Importar backup JSON**; isso substitui os registros atuais.
- Instalação em outro endereço, outro aparelho, limpeza de dados do Safari ou reinstalação **não transfere automaticamente os registros**.
- Se você já tem registros no HTML anterior, exporte o JSON da versão anterior e importe no aplicativo publicado. Os dois usam o mesmo formato de backup `maratona2027`.
- Evite mudar o endereço do repositório depois de começar a registrar os treinos.

## Atualizações

Para atualizar o aplicativo, substitua os arquivos do repositório. Se alterar os arquivos do aplicativo, **incremente `CACHE_NAME` em `sw.js`** (`v1` → `v2` etc.) para forçar atualização do cache. Antes de qualquer atualização, exporte um backup. Atualizar arquivos não deve apagar o `localStorage` se o endereço for mantido, mas backups continuam necessários.

## Observações técnicas

- Funciona offline após a primeira instalação bem-sucedida e cache dos arquivos. O iOS pode eliminar dados de sites sob pressão de armazenamento; não é um armazenamento permanente garantido.
- O GitHub Pages publica repositórios públicos. Não coloque dados pessoais ou backups JSON no repositório.
- Não há servidor, conta, sincronização em nuvem nem envio automático dos dados.
- Em algumas versões do iOS, a opção de instalação muda de nome.


## Upgrade v3 — editor de prescrição

A aba **Editar plano** permite editar treinos completos, exportar um modelo JSON e importar prescrições semanais produzidas após análise do feedback. A importação não executa JavaScript e exige confirmação. **Antes de substituir arquivos no GitHub, exporte backup JSON**. Preserve o mesmo endereço do site. O armazenamento `maratona2027_v2` foi mantido para reutilizar registros existentes.

**Importante:** na importação de uma semana já iniciada, os registros permanecem, mas a lista exibida pode mudar. Prefira importar prescrições futuras. As cargas e repetições antigas são indexadas pela posição do exercício; a atualização deve ser feita antes de iniciar a semana.


## Versao 4 - correcao de musculacao
- Cargas, repeticoes, PSE e observacoes sao salvos conforme digitados.
- Marcar exercicio nao recria formulario nem desativa botao Salvar sessao.
- Cache atualizado para v4.
- Faca backup JSON antes de atualizar.
