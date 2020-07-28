---
layout: cheat-sheet
redirect_to: false
title: Apunts clau de GitHub Git
byline: Git és el sistema de control de versions distribuït de codi obert que facilita l'activitat a GitHub en el vostre portàtil o equip de sobretaula. Aquest full d'apunts resumeix les instruccions de línia d'ordres de Git més habituals per a una referència ràpida.
leadingpath: ../../
---

{% capture colOne %}
## Instal·lació

### GitHub d'escriptori
[desktop.github.com](https://desktop.github.com)

### Git per a totes les plataformes
[git-scm.com](https://git-scm.com)

## Configuració de les eines
Configuració de la informació d'usuari per a tots els repositoris locals

```$ git config --global user.name "[nom]"```

Estableix el nom que voleu associar a totes les accions de comissió

```$ git config --global user.email "[adreça electrònica de correu]"```

Estableix l'adreça electrònic que voleu associar a les accions de comissió

```$ git config --global color.ui auto```

Activa l'acoloriment de la sortida de la línia d'ordres

## Branques

Les branques són una part important del treballa amb Git. Qualsevol comissió que feu es farà en la branca en què hàgiu fet «check out» prèviament. Useu `git status` per a veure quina és branca.

```$ git branch [nom-de-branca]```

Crea una branca nova

```$ git checkout [nom-de-branca]```

Canvia a la branca indicada i actualitza el directori de treball

```$ git merge [branca]```

Combina l'historial de la branca indicada en la branca actual. Això habitualment es fa amb els peticions de baixada, però és una operació important de Git.

```$ git branch -d [nom-de-branca]```

Suprimeix la branca indicada

{% endcapture %}
<div class="col-md-6">
{{ colOne | markdownify }}
</div>


{% capture colTwo %}

## Creació de repositoris

En iniciar un repositori nou, només cal que ho feu una vegada; o bé localment, i després ho pugeu a GitHub, o bé clonant un repositori existent.

```$ git init```

Després d'usar l'ordre `git init`, enllaceu el repositori local amb un repositori buit de GitHub amb l'ordre següent:

```$ git remote add origin [url]```

Converteix un directori existent en un repositori Git

```$ git clone [url]```

Clona (baixa) un repositori que ja existeix en GitHub, incloent-hi tots els fitxers, branques i comissions

## El fitxer .gitignore

De vegades, pot ser una bona idea excloure fitxers del seguiment de Git. Això habitualment es fa amb un fitxer especial anomenat `.gitignore`. Podeu trobar plantilles per a fitxers `.gitignore` en [github.com/github/gitignore](https://github.com/github/gitignore).

## Sincronització de canvis

Sincronitzeu el repositori local amb el repositori remot en GitHub.com

```$ git fetch```

Baixa tot l'historial de les branques de seguiment remotes

```$ git merge```

Combina les branques de seguiment remotes en la branca local actual

```$ git push```

Puja totes les comissions de la branca local a GitHub

```$ git pull```

Actualitza la branca local de treball actual amb les noves comissions des de la corresponent branca remota en GitHub. `git pull` és una combinació de `git fetch` i `git merge`

{% endcapture %}
<div class="col-md-6">
{{ colTwo | markdownify }}
</div>
<div class="clearfix"></div>

{% capture colThree %}

## Canvis

Navegeu i inspeccioneu l'evolució dels fitxers del projecte

```$ git log```

Llista l'historial de versions de la branca actual

```$ git log --follow [fitxer]```

Llista l'historial de versions d'un fitxer, incloent-hi els canvis de nom

```$ git diff [primera-branca]...[segona-branca]```

Mostra les diferències de contingut entre dues branques

```$ git show [comissió]```

Mostra les metadades i els canvis de contigut de la comissió indicada

```$ git add [fitxer]```

Captura el fitxer en preparació per a versionar

```$ git commit -m "[missatge descriptiu]"```

Enregistra permanentment les captures de fitxers en l'historial de versions

## Redo commits

Supressió d'errors i elaboració d'un historial de substicions manual

```$ git reset [commit]```

Desfà totes les comissions després de `[commit]`, i preserva els canvis locals

```$ git reset --hard [commit]```

Descarta tot l'historial i canvis fins a la comissió indicada

> ATENCIÓ! Canviar l'historal pot tenir efectes secundaris desagradables. Si heu de canviar comissions que existeixen en un GitHub (el remot), procediu amb cura. Si us cal ajuda, visiteu github.community o contacteu amb l'assitència.

{% endcapture %}
<div class="col-md-6">
{{ colThree | markdownify }}
</div>

{% capture colFour %}

## Glossari

- **git**: un sistema de control de versions distribuït, de codi obert
- **GitHub**: una plataforma per a hostatjar i treballar de forma col·laborativa amb els repositoris Git
- **comissió**, en anglès *commit*: un objecte de Git, una captura completa del repositori comprimida en un codi SHA
- **branca**, en anglès *branch*: un punter a lightweight movable pointer a una comissió
- **clon**, en anglès *clone*: una versió local d'un repositori, incloent-hi totes les comissions i branques
- **remot**, en anglès *remote*: un repositori comú en GitHub que usen tots els membres d'un equip per a intercanviar els canvis
- **fork**: una còpia d'un repositori en GitHub propietat d'un altre usuari
- **sol·licitud de baixada**, en anglès *pull request*: un lloc per a comparar i discutir les diferències introduïdes en una branca amb revisions, comentaris, proves integrades i altres coses
- **HEAD**: representació del vostre directori de treball actual, el punter HEAD es pot moure a diferents branques, etiquetes o comissions amb `git checkout`

{% endcapture %}
<div class="col-md-6">
{{ colFour | markdownify }}
</div>
<div class="clearfix"></div>
