# Luana e Adriano · 9 de janeiro de 2027

Site do casamento: convite, confirmação de presença e lista de presentes.
É uma página estática, sem build. O site inteiro está em `index.html`.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | O site: convite, cartão de resposta e lista de presentes |
| `og.png` | Imagem que aparece quando o link é colado no WhatsApp |
| `vercel.json` | Cabeçalhos na Vercel (pede para não indexar no Google) |
| `_headers` | O mesmo, caso seja publicado na Netlify |

## Antes de divulgar

Tudo fica no bloco `CONFIG`, perto do fim do `index.html`:

1. **`whatsapp`**: número dos noivos com DDI e DDD, só dígitos (`5511999999999`). É para onde vão as confirmações de presença.
2. **`pix`**: chave, nome do titular e cidade. Enquanto a chave estiver vazia, os presentes levam para a lista do Casar.com.
3. **`og:image`** (no topo do arquivo): trocar `/og.png` pelo endereço completo, por exemplo `https://SEU-DOMINIO/og.png`. O WhatsApp só mostra a prévia com o endereço completo.

Depois de publicar, testem num celular: uma confirmação de presença de verdade e um Pix de R$ 1 para conferir o nome do recebedor.

## Publicar

Na Vercel, importe este repositório. Não há comando de build nem pasta de saída: a raiz do repositório é o site.

## Atualizar a lista de presentes

Os presentes estão no array `PRESENTES`, dentro do `index.html`, no formato `["nome", valor]`. Basta editar, incluir ou apagar linhas.
