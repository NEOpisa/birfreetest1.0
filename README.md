# Birfree — teste 1.0

Instalador da **Birfree**, a área de trabalho da Neovanguard (Wayland, sobre
KWin). Pré-release de teste: ainda não é a 1.0 final.

Esta versão traz o **Terminal Birfree**, uma cópia do Terminal do macOS
(perfil Pro de vidro, abas no estilo do Mac, botões de nova aba e de dividir
na faixa da janela, abre no último tamanho usado).

## Instalar

Em Arch Linux x86_64, como usuário normal (o pacman pede a senha):

```sh
curl -fL -O https://github.com/NEOpisa/birfreetest1.0/releases/download/v1.0.0-test.6.2/Birfree-1.0.0-x86_64.tar.gz
curl -fL -O https://github.com/NEOpisa/birfreetest1.0/releases/download/v1.0.0-test.6.2/SHA256SUMS
sha256sum --check SHA256SUMS
tar -xf Birfree-1.0.0-x86_64.tar.gz
cd Birfree-1.0.0-x86_64
./instalar-birfree --mostrar   # confere e lista os pacotes, sem instalar
./instalar-birfree
```

O pacman vai pedir para trocar o `konsole` pelo `birfree-terminal`:
responda S. Depois, salve o trabalho, saia e entre na sessão **Birfree** pelo
SDDM.

Pacotes prontos, nada é compilado no seu computador:

- `birfree 1.0.0.r131.g4cb8a049-1`
- `birfree-icons 1.0.0.r20.g0c84132e-1`
- `birfree-terminal 26.08.1.r8.g66eb0863e-1`

Compilados contra KWin 6.7.5-1 e Qt 6.11.2-3.

SHA-256 do arquivo: `f64db5448ecff10c318310c1a8958d759f7426dfcfa75d3c021e67f7e12d931a`

## Atualizar

Quem já tem a Birfree instalada atualiza pelo canal de testes
[NEOpisa/test](https://github.com/NEOpisa/test):

```sh
curl -fLO https://raw.githubusercontent.com/NEOpisa/test/main/atualizar-birfree
chmod +x atualizar-birfree
./atualizar-birfree
```

O `atualizar-birfree` deste repositório faz a mesma coisa.

## Outras opções do instalador

- `./instalar-birfree --atualizar`: só atualiza os pacotes da Birfree.
- `./instalar-birfree --migrar`: migração antiga, que mexe no sistema
  (`--simular` para ver antes, `--desfazer` para reverter).

Fontes (GPL) dentro do arquivo, em `fontes/Birfree-fontes.tar.gz`.
