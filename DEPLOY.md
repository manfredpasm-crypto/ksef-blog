# 🚀 Wdrożenie KSeF Blog na GitHub Pages

## Krok 1: Utwórz repozytorium na GitHub

1. Wejdź na https://github.com/new
2. **Repository name:** `ksef-blog`
3. **Visibility:** Public (darmowe GitHub Pages)
4. **Initialize:** NIE zaznaczaj (mamy już lokalne repo)
5. Kliknij **Create repository**

## Krok 2: Podłącz lokalne repozytorium

Skopiuj poniższe komendy i wklej do terminala (w folderze ksef-blog):

```bash
cd /home/stan/.openclaw/workspace/ksef-blog

# Dodaj zdalne repozytorium
git remote add origin https://github.com/TWOJ_USERNAME/ksef-blog.git

# Wypchnij kod
git branch -M main
git push -u origin main
```

## Krok 3: Włącz GitHub Pages

1. W repozytorium na GitHub: **Settings** → **Pages**
2. **Source:** Deploy from a branch
3. **Branch:** main / root
4. Kliknij **Save**

## Krok 4: Poczekaj na wdrożenie

- GitHub zbuduje stronę w ciągu 1-2 minut
- Adres: `https://TWOJ_USERNAME.github.io/ksef-blog/`

## Krok 5: Własna domena (opcjonalnie)

Jeśli chcesz użyć `ksef-blog.pl`:

1. Kup domenę (np. na OVH, nazwa.pl, AfterMarket)
2. W DNS ustaw rekord A na:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
3. W GitHub Pages: dodaj domenę w sekcji "Custom domain"
4. Utwórz plik `CNAME` w repo z zawartością: `ksef-blog.pl`

---

## 📝 Automatyczne publikowanie nowych artykułów

Gdy Writer napisze nowy artykuł:

```bash
cd /home/stan/.openclaw/workspace/ksef-blog

# Dodaj nowy post
git add _posts/nowy-artykul.md
git commit -m "Add: Nowy artykuł o KSeF"
git push origin main
```

GitHub Pages automatycznie zbuduje i opublikuje nową wersję (30-60 sekund).

---

## ✅ Status

Lokalne repo gotowe. Czeka na wypchnięcie do GitHub.

**Następny krok:** Utwórz repozytorium na GitHub i wypchnij kod.
