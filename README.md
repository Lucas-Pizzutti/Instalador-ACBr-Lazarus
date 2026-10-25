# Instalador-ACBr-Lazarus
Instalador paralelo gratuito de componentes ACBr para Lazarus no Windows, com suporte a 32 e 64 bits.

# ACBrInstaller 1.0 — Beta

Instalador gratuito de componentes ACBr para Lazarus no Windows, com suporte a IDEs de 32 e 64 bits. Instala na IDE principal selecionada, reconstruindo seu executável e registrando os pacotes no perfil escolhido.

Projeto independente, sem vínculo oficial com o Projeto ACBr ou o Lazarus.

Encontrando qualquer erro, me avise que procurarei uma correção.

## Requisitos

- Windows com .NET Framework 4.8.
- Lazarus completo com fontes e compilador FPC correspondente à arquitetura da IDE.
- Fontes ACBr completos, contendo Fontes e Pacotes/Lazarus.
- Permissão de gravação nas pastas selecionadas e espaço para backup (se desejar).

## Alguns LPKs requerem partes de outros fora do ACBr, como o PowerPDF, instale eles no Gerenciador de Pacotes Online diretamente no Lazarus.
--- FCFortes, LazReport e outros precisam desse PowerPDF em algumas bibliotecas, como a de boleto.

## Como usar

1. Extraia todos os arquivos do ZIP numa pasta. Mantenha ACBrInstaller.exe.config junto do executável.
2. Abra o Lazarus uma vez, conclua sua configuração inicial, dê CTRL + F9 para compilar qualquer projeto pelo menos uma vez e feche a IDE antes de usar o instalador.
3. Execute ACBrInstaller.exe e selecione a pasta do Lazarus, a raiz dos fontes ACBr e o perfil usado normalmente pela IDE.
4. O perfil costuma ficar em %LOCALAPPDATA%\lazarus e deve conter environmentoptions.xml. Se o atalho usa --primary-config-path, selecione a pasta indicada nele.
5. Selecione uma pasta separada para backups e logs. Informe também os fontes de outros componentes já instalados, quando solicitado.
6. Analise os pacotes, selecione os componentes desejados, revise e simule. Se houver pacotes registrados, escolha Atualizar ou Manter conforme sua necessidade.
7. Mantenha o backup ativado e confirme a instalação. Aguarde o resultado.
8. Ao concluir, use Abrir Lazarus e finalizar. Confira a paleta de componentes e compile um projeto de teste.

Mantenha a pasta dos fontes ACBr no mesmo local após instalar.

## Backup e problemas

O backup vem ativado. Desativá-lo impede a recuperação automática em caso de falha. Não feche o programa à força durante a instalação.

Se ocorrer um erro, consulte os logs na pasta execucao-... dentro da pasta de backups escolhida. O destino padrão é %LOCALAPPDATA%\ACBrInstaller\Backups. Use Restaurar backup, quando necessário e disponível.

Ao relatar um problema, informe a versão do Windows, do Lazarus, do FPC e a arquitetura. Anexe instalacao.log após conferir se contém dados pessoais.

## Limites desta versão

Versão beta: valide primeiro em uma VM ou numa instalação de teste. A compatibilidade com todas as versões e combinações de componentes ainda não foi validada.

Não inclui ACBr, Lazarus, compilador, DLLs fiscais, schemas ou certificados. Esses arquivos e as credenciais da aplicação devem ser obtidos/configurados separadamente.

## Licença

O código próprio do instalador é disponibilizado sob a licença MIT, incluída em LICENSE.txt. O programa é distribuído gratuitamente e sem garantia, conforme a licença.

ACBr, Lazarus e demais componentes mantêm suas próprias licenças; a licença do instalador não substitui as deles. Os fontes do instalador não estão incluídos neste pacote.
