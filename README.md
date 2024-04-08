**Peut on prédire le prix de sa maison ?**
================
Prévision des prix des maisons à Ames,OH à l'aide d'un modèle de régression linéaire


---------------



*Par: Diallo,Dzietchueng, Liard, Ngayap, Savoye*

## Résumé

  Notre étude visait à prédire le prix des maisons dans la ville d'Ames en utilisant les variables disponibles dans un dataset. 

  Pour ce faire, nous avons créé des modèles de régression linéaire avec l'aide de R. Cependant, notre dataset comprenait 82 variables, ce qui était largement trop pour notre modèle de régression linéaire. Nous avons donc cherché à réduire notre éventail de variables pour n'en avoir que 20. La seconde étape a donc été de créer un premier modèle linéaire et de voir les résultats que nous pouvions en tirer. 

  Cependant, après de brèves vérifications, nous avons constaté que notre modèle était défaillant en simplement lisant la répartition des résidus.Il est important de noter que la repartition des résidus es laclef pour valider ou non la véracité d'un modèle lineaire. On peut aussi utiliser un test de shapiro pour valider un modèle de regression linéaire mais nous avons préféré suivre les examples des cours.

Nous avons donc été confrontés au premier problème : modifier les paramètres de notre modèle de régression linéaire pour qu'il soit utilisable. Cette étape a été la plus difficile car nous pensions que le problème venait de la loi de distribution du prix des maisons, ce qui nous a compliqué la tâche. Mais finalement, un simple logarithme sur les variables que nous cherchions à expliquer a suffit pour rendre la distribution des résidus du modèle de régression linéaire valide.

  L'étape suivante était donc de trouver un moyen d'optimiser les variables dans notre modèle de régression linéaire. Pour ce faire, nous avons effectué des recherches en ligne et l'une des méthodes qui nous convenait était d'optimiser l'AIC (information criterion).C'est une méthode de calcul d'optimisation qui prend en compte à la fois la simplicité du modèle et sa performance afin de trouver un équilibre.En effet l'optimisation d'un modèle de regression lineaire peut être très utile. dans certains cas cela peut tout simplement améliorer la performance de prédictabilité du modèle. Mais il est aussi important qu'un modèle soit optimisé dans les ressources qu'il consome afin d'éviter de faire ralentir son programme.

  Nous avions donc un modèle composé de 11 variables explicatives (LotArea, BldgType, OverallQual, OverallCond, YearBuilt, YearRemodAdd, TotalBsmtSF, Heating, CentralAir, GrLivArea, FullBath, HalfBath, BedroomAbvGr, GarageArea, PoolArea, YrSold).

  Avec un R2 et un R2 ajusté d'environ 85%, ce qui est un résultat assez correct. Le score de l'AIC était de -5330.49, ce qui est également un bon résultat. 

Est-il possible de prédire avec exactitude le prix de sa maison ? Il est évident que non. En effet, ces résultats ne sont valables que dans le contexte où les données ont été collectées, c'est-à-dire à Ames, dans l'Ohio, entre 2006 et 2010. Cependant, le modèle est capable de prédire le prix des maisons dans ce contexte. Mais la méthode utilisée prouve qu'elle est efficace. Pour pouvoir l'appliquer à sa propre maison, il faudrait disposer d'un dataset similaire dans la ville où vous habitez. Même si cela reste pour l'instant une utopie, grâce au code que nous avons mis en place, il est très simple de créer un modèle de régression linéaire semblable à celui-ci adapté à un autre dataset, même s'il est différent.


# Présentation

Notre présentation est disponible [ici](presentation/presentation.html).

## Données

Dean De Cock, *Ames, IA Real Estate Data*,electronic dataset, Department of Mathematics and Computer Science, Truman State University, <http://jse.amstat.org/jse_data_archive.htm> (cherchez "AmesHousing" avec Ctrl+f pour trouver la description du dataset).

## Références

[Source des données](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)

[Ressource sur les modèles linéaire dans R](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)

[Ressource Parsnip](https://parsnip.tidymodels.org/reference/linear_reg.html)


