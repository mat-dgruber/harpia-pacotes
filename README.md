# harpia-pacotes

Índice oficial de pacotes da linguagem [Harpia](https://github.com/mat-dgruber/Harpia), consumido por `harpia instalar <nome>`.

## Formato

```json
{
  "pacotes": {
    "nome-do-pacote": {
      "versoes": {
        "1.0.0": {
          "url": "https://github.com/mat-dgruber/<repo>/releases/download/v1.0.0/pacote.zip",
          "sha256": "<hash hexadecimal do .zip>"
        }
      }
    }
  }
}
```

## Regras

- `sha256` é obrigatório em toda versão; sem ele a CLI recusa a instalação.
- `url` precisa ser um arquivo de *release* em `https://github.com/mat-dgruber/`.
- Nomes: `^[A-Za-z0-9_][A-Za-z0-9._-]*$`.
- Versões publicadas não são editadas: uma correção vira uma nova versão.
- Para usar outro índice (espelho ou registro privado): `HARPIA_REGISTRO=<url do pacotes.json>`.
