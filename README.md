# Orma Gioielli — sito dimostrativo

**Demo online → https://gxmich.github.io/orma-gioielli-demo/**

> ### Attività di fantasia
>
> **Orma Gioielli non esiste.** Nome, indirizzo a Roverasca (paese inventato), telefono,
> email, orari, collezioni e prodotti sono inventati e servono solo a mostrare come
> funziona il sito.
>
> Telefono `+39 000 000 0000` ed email su `orma-gioielli.example`: `.example` è un dominio
> riservato dallo IANA e non può recapitare posta a nessuno.
>
> Tutte le pagine hanno `<meta name="robots" content="noindex, nofollow">` e il
> `robots.txt` blocca l'intero sito. Su un *project site* di GitHub Pages il `robots.txt`
> non viene letto (i crawler lo cercano alla radice del dominio), quindi la protezione
> effettiva è il `noindex` nelle pagine.
>
> I contatti sono simulati: «Invia l'idea» e «Chiedi disponibilità» copiano il testo negli
> appunti e mostrano un avviso, senza aprire chat né inviare messaggi. La mappa è disattivata.

Sito vetrina per una boutique di gioielli in acciaio e argento che incide i pezzi al banco.
Statico, in **HTML + CSS + JavaScript vanilla**: nessun framework, nessuna build, nessuna
richiesta a servizi esterni (font e librerie sono in locale).

## Cosa mostra la demo

- **Anteprima dell'incisione in tempo reale.** Si sceglie forma (tonda, cuore, barretta,
  piastrina), colore del metallo, carattere e simbolo; la medaglietta è disegnata in SVG
  e il testo si adatta da solo alla larghezza utile. Cinque idee pronte riempiono il modulo
  con un clic.
- **Collezioni a schede** con scheda prodotto laterale (foto, descrizione, finiture,
  pulsante «Prova l'incisione» che porta il gioiello nell'anteprima).
- **Idee regalo** per destinatario: ogni card imposta l'anteprima con un testo già pronto.
- **Stato della boutique** calcolato sull'ora italiana («Aperto ora, fino alle 19:30»).
- Intro alla prima visita, scorrimento morbido (Lenis), comparse e parallasse, tutto
  spento con `prefers-reduced-motion`.
- Su telefono: menu a schermo intero, barra di azione in basso e anteprima compatta
  dell'incisione che resta visibile mentre si compilano le opzioni.

## Struttura

```
index.html            Pagina unica: hero, collezioni, incisione, selezione,
                      manifesto, idee regalo, boutique, feed di esempio
privacy.html          Informativa di esempio (struttura, non testo legale definitivo)
robots.txt            Disallow: /
assets/site.css       Stili
assets/app.js         Anteprima incisione, schede, contatti simulati, stato boutique
assets/ui.js          Menu, scheda prodotto, ancore, barra mobile
assets/motion.js      Intro, scorrimento morbido, comparse, parallasse
assets/fonts/         Bodoni Moda, Jost, Pinyon Script, Josefin Sans, Courier Prime (woff2)
assets/vendor/        Lenis
assets/media/         Foto (WebP), elenco e licenze in CREDITI-FOTO.md
```

I testi e le foto dei prodotti sono in un unico blocco JSON in fondo a `index.html`
(`#products-data`).

## Come avviarla

Non serve installare niente. Basta aprire `index.html` nel browser, oppure servire la
cartella con un server statico qualsiasi:

```
npx serve .
```

## Foto

Tutte le foto vengono da [Unsplash](https://unsplash.com) (Unsplash License, uso
commerciale consentito). Autori e link in [CREDITI-FOTO.md](CREDITI-FOTO.md).

---

Sito dimostrativo realizzato da [Michele Modica](https://www.modicamichele.it).
