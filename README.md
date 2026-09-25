# harangozobalint.hu

Szakmai oldal és blog. Hugo (extended) + [PaperMod](https://github.com/adityatelange/hugo-PaperMod) téma (git submodule).

## Új poszt

1. `hugo new content posts/2026-10-cim.md` – vázlatként (`draft: true`) jön létre.
2. Töltsd ki a front mattert (`title`, `slug`, `description`, `tags`), írd meg a szöveget.
3. Ha kész: `draft: false`. Az URL `/irasok/<slug>/` lesz.

## Lokális futtatás

```bash
git submodule update --init --recursive   # első klónozás után
hugo server -D                            # http://localhost:1313, vázlatokkal és jövőbeli posztokkal
hugo --gc --minify                        # éles build → public/
```

## Kimenet

Push a `main` ágra → a `.github/workflows/hugo.yml` (GitHub Actions) buildel és kiteszi GitHub Pages-re.
Vázlatok (`draft: true`) és jövőbeli dátumú posztok élesben nem jelennek meg.
