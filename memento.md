# Memento Pandas

Voir aussi [le memento sur Python](PDF/Python3_reference_cheat_sheet_day_2.pdf) (en anglais)

## Importer le module
`import pandas as pd`

## Charger un fichier

`df = pd.read_csv('mon-fichier.csv')`

`df = pd.read_excel('mon-tableur-excel.xls')`

### Sauter des lignes

On utilise le paramètre **skiprows**:<br>
`pd.read_csv('fichier.csv', skiprows=5)`

### Spécifier le séparateur

Avec le paramètre **sep**:<br>
`pd.read_csv('fichier.csv', sep=';')`

### Spécifier l’encodage

Avec le paramètre **encoding**:<br>
`pd.read_csv('fichier.csv', encoding='latin-1')`

## Afficher…

### Afficher les premières lignes
`df.head()`

### Afficher le nom des colonnes
`df.columns`

### Afficher des colonnes spécifiques
`df[['colonne-1', 'colonne-2']]`

## Filtrer
On glisse une condition «if» dans notre dataframe:<br>
`condition = df['colonne-1'] == 0`
`df[ condition ]`

ou plus simplement:<br>
`df[ df['colonne-1'] == 0 ]`