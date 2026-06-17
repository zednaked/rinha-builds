# rinha — builds

Builds do protótipo. Cada versão é marcada com uma tag `vX.Y.Z` (veja os [releases](https://github.com/zednaked/rinha-builds/tags)).

## Plataformas

- `linux/` — `rinha.x86_64` + `rinha.pck` (mantenha os dois na mesma pasta)
- `windows/` — `rinha.exe` + `rinha.pck` (mantenha os dois na mesma pasta)
- `macos/` — `rinha.zip` (contém `rinha.app`, universal Intel + Apple Silicon, tudo embutido)

## Rodar

**Linux:**
```bash
chmod +x rinha.x86_64
./rinha.x86_64
```

**Windows:** dê dois cliques em `rinha.exe`.

**macOS:** descompacte o `rinha.zip` e abra o `rinha.app`. O app **não é assinado**, então na
primeira vez o Gatekeeper vai bloquear — clique com o botão direito → **Abrir** (e confirme), ou
rode `xattr -dr com.apple.quarantine rinha.app` no terminal. Universal: roda nativo em Intel e
Apple Silicon.

---
Gerado com Godot 4.6.3 (export release — Linux/Windows x86_64, macOS universal).
