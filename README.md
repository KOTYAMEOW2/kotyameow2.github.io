# Единый справочник SCP/ГОК

Самодостаточный одностраничный сайт (всё внутри `index.html`, изображения вшиты, без сервера и сборки).

## Деплой на GitHub Pages

1. Создай репозиторий на GitHub (например `scp-spravochnik`). Можно публичный.
2. Загрузи в него все файлы из этой папки (кнопка **Add file → Upload files**, перетащи всё и **Commit**):
   - `index.html`, `404.html`
   - `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`, `icon-512.png`
   - `site.webmanifest`, `robots.txt`, `.nojekyll`
3. Открой **Settings → Pages**.
4. В разделе **Build and deployment → Source** выбери **Deploy from a branch**.
5. **Branch:** `main`, папка `/ (root)` → **Save**.
6. Через ~1 минуту вверху страницы появится адрес вида
   `https://ИМЯ.github.io/scp-spravochnik/` — это твой сайт.

> Файл `.nojekyll` уже включён, чтобы GitHub не обрабатывал сайт через Jekyll.
> Главная страница берётся из `index.html` автоматически.

## Свой домен (необязательно)

1. В **Settings → Pages → Custom domain** впиши домен (например `spravochnik.example`).
2. У регистратора домена добавь DNS-записи:
   - `CNAME` для `www` → `ИМЯ.github.io`
   - или `A`-записи апекса на IP GitHub Pages (185.199.108.153, .109.153, .110.153, .111.153).
3. Вернись на страницу Pages и включи **Enforce HTTPS**.

## Обновление

Чтобы обновить сайт — просто залей новый `index.html` поверх старого (Add file → Upload files → Commit). Изменения появятся через ~минуту.
