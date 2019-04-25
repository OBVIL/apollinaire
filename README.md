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


# Encodage des données

## Métadonnées 

| Balise | Description | Exemple |  
| <term type="support"></term> | nom du medium dans lequel apparaît le texte | Alcools (recueil, 1913) | 
| <term type="pubPlace"></term> | lieu de publication | Paris |
| <term type="publisher"></term> | éditeur | Mercure de France |
| <term type="pubDate"></term> | date de publication | format jj/mm/aaaa |
| <term type="medium">livre</term> | type de support dans lequel paraît le texte | livre / revue | 
| <term type="recipient"/> | ... | ... | 
| <term type="dedication" key=""></term> | Si le texte est dédicacé, inscrire le nom de la personne + son idref dans "key" | <term type="dedication" key="Dalize, René (1879-1917)"> René Dalize</term> |
| <term type="topTitle"></term> | titre du texte | <term type="topTitle">Zone</term> |
| <term type="seriesTitle"/></term> | nom de série d'un recueil de poème | la série "Ondes" dans le recueil "Calligrammes" | 
| <term type="seriesNumber"/></term> | numéroter le poème de la série | "Fumées" est le poème n°3 dans la série "Etandards" du recueil "Calligrammes |
| <term type="heading"></term> | section d'un ouvrage / d'une revue | "Peintres nouveaux" est une section de l'ouvrage "Méditations esthétiques" | 
| <term type="headingNumber"/> | numéroter l'article / le texte de la section | "Futurisme italien" est l'article numéro 4 paru dans la rubrique "La Vie anecdotique" dans la revue "Mercure de France" |
| <term type="signed"></term> | le signataire du texte (livre, poème, série de poèmes, etc.) | Guillaume Apollinaire | (nb: si pas de signature, on ne note rien)
| <term type="figure"/> | mentionne un dessin / une gravure qui accompagne le texte | calligramme (si le poème encodé est un calligramme) |
| <term type="figureAuthor"/> | auteur du dessin / de la gravure | René Dalize | 
|  <term type="msDesc"/> | ... | ... |

noteAfter: utiliser l'attribut "when" quand on est sûr de la date / attributs "notBefore" et "notAfter" pour un empan de dates / attribut "notAfter" par défaut (année de publication) 
div type="article": le type de texte (article, poem, chapter, section, act, scene)
 

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