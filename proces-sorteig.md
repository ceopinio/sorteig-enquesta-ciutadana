Sorteig de l’Enquesta Ciutadana de Catalunya
================

El nombre total de persones amb dret a participar en el sorteig és
**8.032.**

A continuació es crea en la variable `dataSorteig` la data i hora del
sorteig, que posteriorment s’usa com a llavor per a escollir el número
de tall:

``` r
dataSorteig <- "2022-12-14T10:00:00Z"
dataSorteig <-  as.POSIXct(dataSorteig, tz = "Europe/Madrid", format = "%Y-%m-%dT%H:%M:%OSZ")
```

Assignació de la llavor i extracció del número de tall:

``` r
set.seed(dataSorteig)
( posicio_sorteig <- sample(1:8032, size = 1, replace = F) )
```

    ## [1] 7414

Tal com es pot veure en l’execució del codi, un cop ordenats els
identificadors alfabèticament de les persones amb dret de participar en
el sorteig, el codi que pertany a la posició **7414** és l’identificador
guanyador.

A partir d’aquest número, les 10 primeres persones que hagin contestat
el qüestionari entre els dies 30 de novembre del 2022 i 31 de gener del
2023 i hagin acceptat participar en el sorteig seran les persones
guanyadores.

Per motius de protecció de dades, els identificadors no poden ser
publicats.
