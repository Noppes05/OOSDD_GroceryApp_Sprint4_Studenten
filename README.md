# Git Flow Workflow

Dit project gebruikt **Git Flow** als branching-strategie. Git Flow helpt ons om features, releases en hotfixes gestructureerd te beheren.

## Branches

In Git Flow zijn er een paar vaste branches:

- **main**  
  Bevat altijd de productierijpe code. Alles op `main` is **stabiel** en kan gedeployed worden.

- **develop**  
  Bevat de laatste ontwikkelstatus. Nieuwe features worden hier samengevoegd.

Daarnaast worden tijdelijke branches gebruikt:

- **feature/**  
  Voor nieuwe functionaliteiten.  
  Naamgeving: `feature/omschrijving`  
  → Gebaseerd op `develop` en wordt terug gemerged in `develop`.

- **release/**  
  Voor het voorbereiden van een nieuwe release (bugfixes, documentatie, kleine aanpassingen).  
  Naamgeving: `release/x.y.z`  
  → Gebaseerd op `develop` en wordt gemerged in zowel `main` als `develop`.

- **hotfix/**  
  Voor urgente fixes op productie.  
  Naamgeving: `hotfix/x.y.z`  
  → Gebaseerd op `main` en wordt gemerged in zowel `main` als `develop`.


# GroceryApp sprint4 Studentversie  

## UC10 Productaantal in boodschappenlijst
Aanpassingen zijn compleet.

## UC11 Meest verkochte producten
Vereist aanvulling:  
- Werk in GroceryListItemsService de methode GetBestSellingProducts uit.  
- In BestSellingProductsView de kop van de tabel aanvullen met de gewenste kopregel boven de tabel. Daarnaast de inhoud van de tabel uitwerken.

## UC13 Klanten tonen per product  
Deze UC toont de klanten die een bepaald product hebben gekocht:  
- Maak enum Role met als waarden None en Admin.  
- Geef de Client class een property Role metb als type de enum Role. De default waarde is None.  
- In Client Repo koppel je de rol Role.Admin aan user3 (= admin).
- In BoughtProductsService werk je de Get(productid) functie uit zodat alle Clients die product met productid hebben gekocht met client, boodschappenlijst en product in de lijst staan die wordt geretourneerd.  
- In BoughtProductsView moet de naam van de Client ewn de naam van de Boodschappenlijst worden getoond in de CollectionView.  
- In BoughtProductsViewModel de OnSelectedProductChanged uitwerken zodat bij een ander product de lijst correct wordt gevuld.  
- In GroceryListViewModel maak je de methode ShowBoughtProducts(). Als de Client de rol admin heeft dan navigeer je naar BoughtProductsView. Anders doe je niets.  
- In GroceryListView voeg je een ToolbarItem toe met als binding Client.Name en als Command ShowBoughtProducts.  


  
