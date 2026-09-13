# Vizualizarea unui depozit privat

După conectarea cu GitHub, puteți citi documentele din depozitele private, limitate la cele la care aveți acces de citire. Lunascape Docs nu are niciodată conturi sau permisiuni proprii.

## Conectați-vă și deschideți

1. Deschideți <https://docs.lunascape.org/>.
   Când indicați un document privat sau când încă nu v-ați conectat, apare ecranul de conectare.
2. Apăsați [Conectare cu GitHub].
   Ecranul de autentificare GitHub se deschide într-o fereastră pop-up.
3. După conectare, apăsați [Deschide documente] în bara de instrumente și alegeți depozitul dorit din [Alegeți dintre depozitele lizibile].

> **Sfat**
>
> - Numele contului conectat este afișat în bara de instrumente. Tot de aici puteți alege [Deconectare] sau [Conectare cu alt cont].
> - Lista afișează depozitele conturilor (organizații sau persoane) unde este instalată aplicația GitHub „Lunascape Docs”, limitate la cele la care aveți acces de citire.

## Configurarea efectuată de proprietarul depozitului

Dacă depozitul dorit nu apare în listă, proprietarul depozitului sau administratorul organizației trebuie să instaleze aplicația GitHub „Lunascape Docs”.

- Permisiunile solicitate sunt Contents (citire și scriere) și Pull requests (citire și scriere). Citirea este pentru vizualizare, iar scrierea este pentru cererile de publicare de pe web (Pull Request). Lunascape Docs nu salvează niciodată conținutul documentelor.
- Aplicația se instalează per cont (organizație sau persoană). Alegeți „All repositories” (care include și depozitele create ulterior) sau doar depozitele selectate.

| Situație | Pași |
|---|---|
| Instalarea într-o organizație sau într-un cont personal nou | Folosiți [pagina de instalare](https://github.com/apps/lunascape-docs/installations/new) |
| Adăugarea unor depozite într-o organizație care o are deja | Settings ale organizației → GitHub Apps → Lunascape Docs → Configure → Repository access |

Chiar dacă aplicația este instalată pentru o întreagă organizație, fiecare membru vede doar depozitele la care are acces de citire și poate trimite o cerere de publicare doar către depozitele la care are acces de scriere.

> **Sfat**
> - La o instalare nouă, permisiunile solicitate sunt afișate ca listă pe ecranul de instalare, iar apăsarea butonului „Install” înseamnă că le-ați aprobat. Nu este nevoie de nicio altă operație.
> - O organizație care a instalat aplicația înainte de adăugarea unei permisiuni primește un e-mail către administratori, iar un buton de aprobare apare în partea de sus a Settings ale organizației → GitHub Apps → Lunascape Docs → Configure. Până la aprobare, organizația respectivă poate doar vizualiza, iar la trimiterea unei cereri de publicare apare mesajul „este necesară acordarea permisiunii de scriere”.
> - Puteți verifica în ce permisiuni sunteți în prezent chiar în ecranul Configure. Pentru un cont personal, acesta este Settings → Applications → Installed GitHub Apps.
> - Dacă ați scos din greșeală depozitul dorit sau ați dezinstalat aplicația, o puteți readuce la starea inițială reinstalând-o din [pagina de instalare](https://github.com/apps/lunascape-docs/installations/new). Mesajul de respingere a cererii de publicare include un link către ecranul de remediere.
> - Dacă din partea depozitului nu doriți să acceptați cereri de publicare, scrieți `"publish": { "enabled": false }` în `lunascape-docs.json`. Vizualizarea rămâne disponibilă ca înainte.

## Subiecte conexe

- [Deschiderea unui depozit GitHub](open-repository.md)
- [Versiunea web nu se poate deschide sau nu vă puteți conecta](../07-troubleshooting/web.md)
