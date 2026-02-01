# Deployment - KSeF Blog

## Krok 1: Stwórz repozytorium GitHub

1. Wejdź na https://github.com/new
2. Nazwa repozytorium: `ksef-blog`
3. Ustaw jako **Public**
4. Kliknij **Create repository**

## Krok 2: Podłącz lokalne repo do GitHub

```bash
cd /home/stan/.openclaw/workspace/ksef-blog
git remote add origin https://github.com/TWOJ_USERNAME/ksef-blog.git
git branch -M main
git push -u origin main
```

## Krok 3: Włącz GitHub Pages

1. W repozytorium GitHub → **Settings** → **Pages**
2. **Source**: Deploy from a branch
3. **Branch**: main / root
4. Kliknij **Save**

## Krok 4: Poczekaj 2-5 minut

Blog będzie dostępny pod:
`https://TWOJ_USERNAME.github.io/ksef-blog`

## Automatyczne publikowanie nowych artykułów

1. Writer pisze artykuł w `_posts/`
2. Developer commituje i pushuje na GitHub
3. GitHub Pages automatycznie publikuje (30 sekund)

## Status

- ✅ Struktura Jekyll gotowa
- ✅ Pierwszy artykuł dodany
- ✅ Layouty skonfigurowane
- 🔄 Czeka na push do GitHub
