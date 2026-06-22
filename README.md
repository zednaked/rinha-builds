# rinha — builds

Builds do protótipo. **Os binários ficam nos [Releases](https://github.com/zednaked/rinha-builds/releases)** — baixe o pacote da sua plataforma na versão mais recente (`vX.Y.Z`).

## Download

Cada release tem três arquivos:

- `rinha-linux-vX.Y.Z.tar.gz` — `rinha.x86_64` + `rinha.pck`
- `rinha-windows-vX.Y.Z.zip` — `rinha.exe` + `rinha.pck`
- `rinha-macos-vX.Y.Z.zip` — `rinha.app` (universal Intel + Apple Silicon, tudo embutido)

> Em Linux/Windows, mantenha o executável e o `.pck` **na mesma pasta**.

## Rodar

**Linux:**
```bash
tar xzf rinha-linux-vX.Y.Z.tar.gz
chmod +x rinha.x86_64
./rinha.x86_64
```

**Windows:** descompacte e dê dois cliques em `rinha.exe`.

**macOS:** descompacte o `.zip` e abra o `rinha.app`. O app é assinado **ad-hoc** (não notarizado),
então na primeira vez o Gatekeeper pode bloquear — clique com o botão direito → **Abrir** (e
confirme). Se aparecer **"is damaged and can't be opened"**, rode no terminal:

```bash
xattr -cr rinha.app
codesign --force --deep --sign - rinha.app
```

e abra de novo. Universal: roda nativo em Intel e Apple Silicon.

---
Gerado com Godot 4.6 (export release — Linux/Windows x86_64, macOS universal).
