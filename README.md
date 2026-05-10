# ClassNotes JSON API

Backend fake com `json-server` para demo e testes do app mobile `ClassNotes`.

## Rodar localmente

```bash
npm install
npm run start:local
```

Endpoints:

- `http://localhost:3001/classes`
- `http://localhost:3001/observations`

## Subir no Railway

1. Crie um repositório novo no GitHub e suba esta pasta.
2. No Railway, crie um projeto com `Deploy from GitHub repo`.
3. Adicione um volume persistente.
4. Monte o volume em:

```txt
/data
```

5. Faça o deploy.

O script `start` já faz o bootstrap:

- se `/data/db.json` não existir, ele copia o `db.json` do repositório
- depois sobe o `json-server` usando o arquivo persistente

## URL no app

Depois do deploy, copie a URL pública do Railway e use no app React Native:

```env
API_BASE_URL=https://seu-projeto.up.railway.app
```

## Observação

Esse backend é ótimo para:

- demo
- testes em celular físico
- mock de staging

Não é a melhor opção para produção real.
