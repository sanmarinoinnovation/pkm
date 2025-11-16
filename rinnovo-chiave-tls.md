# START
- Verifica che il terminale sia sul repo desiderato:
  - PROD
  - UAT
  - DEV
- Dal terminale lancia i comandi git necessari.

## Impostare user e mail (Per verificare è lo stesso comando senza i dati)

`git config user.name "sanmarinoinnovation"`

`git config user.email "blockchain@sanmarinoinnovation.com"`


Per impostare chiave:

`git config user.signingkey 6FA0A144B444C1F5`

## Lista tutti i tag

`git tag`

## Create il TAG

## Tag annotato (con messaggio - CONSIGLIATO)
`git tag -a v1.12 -m "Release version 1.12"`

## Push di un tag specifico
`git push origin v1.12`

--------------
4-nov-2025
--------------
Procedura di rinnovo della chiave TLS

Dalla cartella PROD/scripts/
./gen_tls_certs.sh DN_template.cnf
