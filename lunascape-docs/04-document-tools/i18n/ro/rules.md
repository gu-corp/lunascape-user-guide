# Modificarea regulilor de verificare

Puteți schimba nivelul de notificare (eroare, avertisment, informații) al fiecărei verificări sau puteți dezactiva o verificare. Modificările sunt salvate în `docs-lint.config.json` din rădăcina documentației și sunt partajate cu echipa.

## Modificarea unui nivel de notificare

1. Apăsați [Instrumente pentru documente] în bara de instrumente și deschideți fila [Verificare].
2. Apăsați [Verifică și modifică regulile].
   Lista verificărilor se extinde în interiorul aceluiași card. Fiecare verificare afișează scopul său și sursa setării actuale (Project, Profile, Pack sau Default).
3. Alegeți nivelul de notificare al verificării pe care doriți să o modificați.
4. Apăsați [Salvează și verifică din nou].
   Setarea este salvată și întreaga rădăcină a documentației este verificată din nou cu noua configurație.

| Opțiune | Semnificație |
|---|---|
| [Setare standard (…)] | Elimină suprascrierea și revine la setarea standard, stabilită în ordinea: profil, Standard Pack, valoare implicită |
| [Dezactivat] | Nu execută această verificare |
| [Informații] / [Avertisment] / [Eroare] | Raportează la acest nivel |

> **Notă**
>
> - Salvarea necesită un spațiu de lucru de încredere.
> - Se salvează doar nivelul de notificare al fiecărei verificări. Opțiunile fiecărei verificări sunt păstrate ca atare. Standard Pack și profilul în sine nu se modifică din acest ecran.
> - Dacă `docs-lint.config.json` a fost modificat din exterior chiar înainte de salvare, salvarea este anulată. Reîncărcați starea cea mai recentă și încercați din nou.
> - Dacă `docs-lint.config.json` nu există, acesta este creat la salvare.

## Editarea directă a fișierelor de configurare

- Apăsați [Deschide setările detaliate] pentru a deschide `docs-lint.config.json` în VS Code.
- Deschideți [Sursa regulilor și setările documentelor] și apăsați [Editează setările documentelor] pentru a deschide `lunascape-docs.json` în VS Code. Standard Pack și profilul se aleg aici.

Pentru ambele fișiere sunt disponibile completarea automată și descrierile oferite de schemele JSON Schema incluse în extensie.

## Standard Pack și profiluri

Standard Pack este un standard de documentație care reunește tipurile de documente necesare, structura capitolelor, terminologia și șabloanele. Îl alegeți din `documentStandards` în `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Pachetul inclus `builtin:gu-corp-software` oferă profilurile `base`, `web-application`, `api-service`, `regulated-financial-product` și `smart-contract`.

## Subiecte conexe

- [Verificarea documentelor](check.md)
- [Configurarea proiectului](project-configuration.md)
