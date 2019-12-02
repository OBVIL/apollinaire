# LABEX OBIL, Apollinaire

* [apollinaire_11000-verges](xml/apollinaire_11000-verges.xml)
* [apollinaire_alcools](xml/apollinaire_alcools.xml)
* [apollinaire_articles-divers](xml/apollinaire_articles-divers.xml)
* [apollinaire_articles-inedits](xml/apollinaire_articles-inedits.xml)
* [apollinaire_bestiaire](xml/apollinaire_bestiaire.xml)
* [apollinaire_calligrammes](xml/apollinaire_calligrammes.xml)
* [apollinaire_contes-posthumes](xml/apollinaire_contes-posthumes.xml)
* [apollinaire_contes-publies](xml/apollinaire_contes-publies.xml)
* [apollinaire_couleur-du-temps](xml/apollinaire_couleur-du-temps.xml)
* [apollinaire_enchanteur-pourrissant](xml/apollinaire_enchanteur-pourrissant.xml)
* [apollinaire_excelsior](xml/apollinaire_excelsior.xml)
* [apollinaire_exploits-jeune-don-juan](xml/apollinaire_exploits-jeune-don-juan.xml)
* [apollinaire_fin-de-babylone](xml/apollinaire_fin-de-babylone.xml)
* [apollinaire_heresiarque-et-cie](xml/apollinaire_heresiarque-et-cie.xml)
* [apollinaire_intransigeant](xml/apollinaire_intransigeant.xml)
* [apollinaire_mamelles-de-tiresias](xml/apollinaire_mamelles-de-tiresias.xml)
* [apollinaire_meditations-esthetiques](xml/apollinaire_meditations-esthetiques.xml)
* [apollinaire_mercure-de-france](xml/apollinaire_mercure-de-france.xml)
* [apollinaire_paris-journal](xml/apollinaire_paris-journal.xml)
* [apollinaire_poete-assassine](xml/apollinaire_poete-assassine.xml)
* [apollinaire_prefaces](xml/apollinaire_prefaces.xml)
* [apollinaire_trois-don-juan](xml/apollinaire_trois-don-juan.xml)
* [apollinaire_vitam-impendere-amori](xml/apollinaire_vitam-impendere-amori.xml)


# Situation actuelle

D'après le document `Rapport de stage du projet HyperApollinaire` :
## Ce qui a été fait
###  Section poésie
- le recueil Alcools.
- le recueil Calligrammes.
- le recueil Bestiaire.
- le recueil Vitam Impendere Amori.
- la collection “Poèmes Publiés”.

### Section prose
- le fichier Mercure de France est terminé.
- le fichier Méditations esthétiques est terminé.

## Ce qui reste à faire
### Section propose
- les articles de journaux
    - articles divers
    - articles inédits
    - paris journal
    - l’intransigeant
    - l’excelsior
- les romans et contes
    - 11000 verges
    - l’enchanteur pourrissant
    - les exploits d’un jeune Don Juan
    - la fin de Babylone
    - les trois Don Juan
    - Hérésiarque et Cie.
    - préfaces
    - le poète assassiné
    - contes publiés
    - contes posthumes
- théâtre
    - les mamelles de Tirésias
    - couleurs du temps


# Encodage des données



## Métadonnées 



###  ! Bon à savoir avant de commencer la lecture de ce document !
* les balises et attributs sont toujours encodés en anglais. 
* ce document donne le modèle d'encodage des métadonnées récemment validé. 
* des documents annexes appuient celui-ci pour aider à l'encodage des métadonnées: 
1. Tutos Github et XML/TEI créés par Anne-Laure: pour maîtriser le dépôt des fichiers et s'adapter aux nouveaux schémas d'encodage des données.  
2. Notes de fin de stage : document PDF qui contient des détails concernant les métadonnées.
3. Le tableau Excel du projet HyperApollinaire: mine de renseignements pour les fichiers travaillés! Ne pas hésiter à les consulter aussi souvent que nécessaire! 
4. Pour connaître la signification d'une balise non-listées dans ce document, se référer au document PDF "index" rangé dans le fichier "Teinte". 
5. Des livres sur les correspondances et les oeuvres du poètes Apollinaire sont accessibles dans le bureau D408: ne pas hésiter à les consulter en cas de doute sur une donnée! 
6. Les formateurs eux-mêmes sont une mine d'or d'informations ! (Motasem, Eric, Anne-Laure)


### Encoder les métadonnées au début d'un fichier XML/TEI 

Il n'y a que deux cartouches à encoder dans cette partie du fichier, mais il est nécessaire de connaître chacune des balises pour comprendre la structure du document. 
La présentation de ces données est détaillée dans le document PDF "Notes de fin de stage".
Les balises à encoder sont celles contenant l'identifiant du fichier et son intitulé. 
Voici leur emplacement au début du fichier: 

```xml

<TEI xml:lang="fre" xmlns="http://www.tei-c.org/ns/1.0" xml:id="apo-P_1913-04-20_alcools_p007">
    <teiHeader>
        <fileDesc>
            <titleStmt>
                <title>Zone</title>

``` 

*exemple tiré du fichier "apo-P_1913-04-20_alcools_p007"(Zone)*

Voici le tableau explicatif de ces métadonnées: 

| balise                                 | description                                 | exemple                        |
| ---------------------------------------| --------------------------------------------|  ------------------------------|
| xml:id="apo-P_1913-04-20_alcools_p007" |  identifiant xml = nom du fichier travaillé |  apo-P_1913-04-20_alcools_p007 |
| <title>Zone</title>                    |   intitulé du fichier travaillé             |  Zone                          |

__Remarques:__ 
* Anne-Laure a formaté dans son document explicatif XML/TEI un nouveau modèle de nommage de fichier mais, dans le cas d'HyperApollinaire, il faut conserver la forme originelle telle qu'elle est montrée dans cet exemple. En cas de question, voir avec les formateurs. 
* Le nom de la balise <title> correspond également à celui des balises <topTitle> et <head>, présentés plus loin dans ce document. Dans le cas où l'intitulé de topTitle est différent voir avec les formateurs (en cas de plusieurs éditions dispersées et renommées, par exemple).



### La date de création du texte encodé 

Elle est enregistrée au format suivant dans chaque fichier XML: 

```xml

<creation><date notAfter="1913"/></creation>

``` 

En fonciton du fichier trois types d'encodage sont possibles:
* attribut "notAfter" par défaut (année de publication). 
* notAfter: utiliser l'attribut "when" quand on est sûr de la date.
* attributs "notBefore" et "notAfter" pour un empan de dates (en cas de doute sur la date précise, on donne une période).



### Tableau des métadonnées à remplir dans la balise <textClass>

 Elles décrivent les données bibliographies du texte encodés (lieu et date de publication, éditeur, auteur, etc.)
 Voici à quoi ressemble l'encodage des métadonnées dans cette balise: 

```xml

 <textClass>
                <keywords>
                    <term type="id"/>
                    <term type="support">Méditations esthétiques. Les peintres cubistes</term>
                    <term type="pubPlace">Paris</term>
                    <term type="publisher">Figuière</term>
                    <term type="pubDate">01/03/1913</term>
                    <term type="medium">livre</term>
                    <term type="recipient"/>
                    <term type="dedication"/>
                    <term type="topTitle">Picasso</term>
                    <term type="seriesTitle"/>
                    <term type="seriesNumber"/>
                    <term type="heading">Peintres nouveaux</term>
                    <term type="headingNumber">1</term>
                    <term type="signed">Guillaume Apollinaire</term>
                    <term type="figure"/>
                    <term type="figureAuthor"/>
                    <term type="msDesc"/>
                </keywords>
            </textClass>

```
*exemple tiré du fichier "meditations-esthetiques_peintresnouveaux_1"(Picasso)*

Voici le tableau explicatif de ces métadonnées:

| Balise                                 | Description                                                                     | Exemple                                                                                                                 | 
| ---------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <term type="support"></term>           | nom du medium dans lequel apparaît le texte                                     | Alcools (recueil, 1913)                                                                                                 | 
| <term type="pubPlace"></term>          | lieu de publication                                                             | Paris                                                                                                                   |
| <term type="publisher"></term>         | éditeur                                                                         | Mercure de France                                                                                                       |
| <term type="pubDate"></term>           | date de publication                                                             | format jj/mm/aaaa                                                                                                       |
| <term type="medium">livre</term>       | type de support dans lequel paraît le texte                                     | voir liste des media dans document PDF "Projet HyperApollinaire"                                                        | 
| <term type="recipient"/>               | destinataire d'un poème épistolaire ou d'origine épistolaire                    | poème dédié à André Rouvère dans "Calligrammes"                                                                         | 
| <term type="dedication" key=""></term> | si le texte est dédicacé, inscrire le nom de la personne + son idref dans "key" | <term type="dedication" key="Dalize, René (1879-1917)"> René Dalize</term>                                              |
| <term type="topTitle"></term>          | titre du texte                                                                  | <term type="topTitle">Zone</term>                                                                                       |
| <term type="seriesTitle"/></term>      | nom de série d'un recueil de poème                                              | la série "Ondes" dans le recueil "Calligrammes"                                                                         | 
| <term type="seriesNumber"/></term>     | numéroter le poème de la série                                                  | "Fumées" est le poème n°3 dans la série "Etandards" du recueil "Calligrammes                                            |
| <term type="heading"></term>           | rubrique d'une revue / nom de chapitre d'un ouvrage                             | "Peintres nouveaux" est une section de l'ouvrage "Méditations esthétiques"                                              | 
| <term type="headingNumber"/>           | numéroter l'article de la rubrique/ le texte du chapitre                        | "Futurisme italien" est l'article numéro 4 paru dans la rubrique "La Vie anecdotique" dans la revue "Mercure de France" |
| <term type="signed"></term>            | le signataire du texte (livre, poème, série de poèmes, etc.)                    | Guillaume Apollinaire (nb: si pas de signature, on ne note rien)                                                        |
| <term type="figure"/>                  | mentionne un dessin / une lithographie qui accompagne le texte                  | calligramme (si le poème encodé est un calligramme)                                                                     |
| <term type="figureAuthor"/>            | auteur du dessin / de la lithographie                                           | René Dalize                                                                                                             | 
|  <term type="msDesc"/>                 | description du manuscrit (si le medium en est un)                               | demander à Eric ou à Motasem                                                                                            |

__Remarques:__ 
* pour plus d'informations détaillées sur les métadonnées, consulter le document "Projet HyperApollinaire" 
* voir notamment le cas topTitle! 



### l'encodage du texte 

Il suffit de copier/coller le texte du fichier depuis le fichier d'origine (voir document PDF "Notes de fin de stage).
MAIS: il faut penser à encoder le type du texte ainsi que son titre dans les balises correspondantes! 
Ces balises apparaissent dans la balise <body> dans laquelle est également encodé le texte: 

```xml

<text>
        <body>
            <div type="poem">
                <head>Le Pont Mirabeau<!--<note resp="editor" n="34" place="bottom"> Pré-originale <hi rend="i"
              >Les Soirées de Paris</hi>, n°1, février 1912, avec <hi rend="i">Per te praesentit
              aruspex</hi> Dans la pré-originale, le poème compte quatre tercets de décasyllabes
            suivis, chacun, du refrain. Apollinaire rompt le vers et le schéma rimique, le deuxième
            décasyllabe de chaque tercet étant scindé en un tétrasyllabe et un hexasyllabe, Le
            refrain se trouve dans une ébauche de la partie III, strophe 1, de <hi rend="i">A la
              Santé</hi> (septembre 1911) (voir <hi rend="i">Marie, note</hi> 0, p. 000). Dans 
              <hi rend="i">Souvenir d’Auteuil</hi>, Apollinaire évoque rapidement le pont Mirabeau
            construit en 1895 : « Mais descendons vers la Seine. C’est un fleuve adorable. On ne se
            lasse point de le regarder. Je l’ai chantée bien souvent en ses aspects diurnes et
            nocturnes. Après le pont Mirabeau la promenade n’attire que les poètes, les gens du
            quartier et les ouvriers endimanchés. » (<hi rend="i">Le flâneur des deux rives</hi>,
            Paris, Gallimard, L’Imaginaire, (1928), 1975, p. 22). Le lien qui unit 
            <hi rend="i>Zone</hi> et <hi rend="i">Le Pont Mirabeau</hi> est donc spatial</note>--></head>
                <lg>
                    <l>Sous <placeName>le pont Mirabeau</placeName> coule <placeName>la Seine</placeName></l>
                    <l><space> </space> Et nos amours</l>
                    <l> Faut-il qu’il m’en souvienne</l>
                    <l>La joie venait <term type="time" subtype="frequence">toujours</term> après la peine</l>
                </lg>
                <lg>
                    <l><space> </space> Vienne <term type="time">la nuit</term> sonne <term type="time"
                        subtype="hour">l’heure</term></l>
                    <l><space> </space> <term type="time">Les jours</term> s’en vont je demeure <!--<note
              resp="editor" n="35" xml:id="note35" place="bottom"> Voir François Villon, <hi
                rend="i">Testament</hi> : “Allé s’en est, et je demeure” (XXIII, v. 177) Sur ce
              refrain, voir <hi rend="i">Marie</hi>, note 0, p. 000.</note>--></l>
                </lg>
                <lg>
                    <l>Les mains dans les mains restons face à face</l>
                    <l><space> </space> <term type="time" subtype="simultaneous">Tandis que</term> sous</l>
                    <l> Le pont de nos bras passe</l>
                    <l>Des éternels regards l’onde si lasse</l>
                </lg>
                <lg>
                    <l><space> </space> Vienne <term type="time">la nuit</term> sonne <term type="time"
                        subtype="hour">l’heure</term></l>
                    <l><space> </space> <term type="time">Les jours</term> s’en vont je demeure</l>
                </lg>
                <lg>
                    <l>L’amour s’en va comme cette eau courante</l>
                    <l><space> </space> L’amour s’en va</l>
                    <l> Comme la vie est lente</l>
                    <l>Et comme <persName>l’Espérance</persName> est violente</l>
                </lg>
                <lg>
                    <l><space> </space> Vienne <term type="time">la nuit</term> sonne <term type="time"
                        subtype="hour">l’heure</term></l>
                    <l><space> </space> <term type="time">Les jours</term> s’en vont je demeure</l>
                </lg>
                <lg>
                    <l>Passent <term type="time">les jours</term> et passent <term type="time">les
                        semaines</term>
                        <!--<note resp="editor" n="36" place="bottom"> Voir Retté, <hi rend="i">L’Archipel en
                fleurs, Chanson d’hiver</hi> : Passent les jours, passent les mois, / Les chevaliers
              sont morts à la croisade.(1895) (p. 36)</note>--></l>
                    <l><space> </space> Ni <term type="time">temps passé</term></l>
                    <l> Ni les amours reviennent</l>
                    <l>Sous <placeName>le pont Mirabeau</placeName> coule <placeName>la Seine</placeName></l>
                </lg>
                <lg>
                    <l><space> </space> Vienne <term type="time">la nuit</term> sonne <term type="time"
                        subtype="hour">l’heure</term></l>
                    <l><space> </space> <term type="time">Les jours</term> s’en vont je demeure</l>
                </lg>
            </div>      
        </body>
    </text>

```xml

*exemple tiré du fichier "apo-P_1913-04-20_alcools_p018"(Le Pont Mirabeau)* 

Voici le tableau explicatif de ces métadonnées:

| balise              | description              | exemple                                    | 
| --------------------|------------------------- | -------------------------------------------| 
| <div type="article">| décrit le type de texte  | article, poem, chapter, section, act, scene|             
| <head>              | intitulé du texte encodé | *Le Pont Mirabeau*                         |

__Remarques:__ 
* l'intitulé de la balise <head> correspond à celui des balises <title> et <topTitle>. Sauf où, dans le cas  mentionné plus haut, l'intitulé de <topTitle> est différent de <title>: dans ce cas demander Eric / Motasem, ou se référer au tableau du fichier Github. 
* les balises <note resp="editor"></note> sont toujours en commentaire pour l'instant! On les place entre les balises vertes <!-- --!> Elles sont donc enregistrées dans le fichier mais n'apparaissent pas dans la visualisation de celui-ci. 
* dans le cas d'un poème comme cet exemple, les balises <lg> sont très importantes pour la structure du texte! Elles permettent de diviser le poème en strophe. Si besoin, se référer toujours au lien ref qui renvoie à la publication d'origine (présenté au début de ce document). 
* ne pas hésiter à se référer aux documents "Note de fin de stages" ainsi qu'aux tutos d'Anne-Laure pour plus d'infos !
