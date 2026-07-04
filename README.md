# Espaço Renascer

Landing page de página única para o **Espaço Renascer** — podologia, estética integrativa e Beauty Academy em Parnaíba, PI.

## Sobre

`index.html` é um site estático e autônomo (sem build, sem dependências). Basta abrir o arquivo no navegador ou servi-lo com qualquer servidor estático:

```bash
python3 -m http.server 8000   # depois abra http://localhost:8000
```

Foi implementado a partir de uma fonte do **Claude Design** (`Espaço Renascer.dc.html`), convertendo os elementos de design (`<x-dc>`, `<x-import>`, bindings `{{ }}`, `style-hover`, script `DCLogic`) em HTML/CSS/JS padrão:

- Os bindings de WhatsApp foram resolvidos para links `wa.me` reais.
- Os `style-hover` viraram regras `:hover` via seletores de atributo no `<style>`.
- Os slots de imagem (`<x-import>`) viraram placeholders `.img-slot` com a descrição da foto — troque por `<img>` quando as fotos estiverem prontas.
- A animação de reveal ao rolar foi reescrita em JS puro com `IntersectionObserver`.

## Personalizar

- **WhatsApp:** número exibido `(86) 99521-2345` e links `https://wa.me/5586995212345?...`. Procure por `wa.me` e por `99521-2345` para atualizar.
- **Endereço / horário:** buscar por "Nossa Senhora de Fátima" e "9h às 20h".
- **Fotos:** substituir cada `<div class="img-slot">…</div>` por uma tag `<img>` mantendo as dimensões do `style`.
