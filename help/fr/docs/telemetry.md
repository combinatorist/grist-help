---
title: Overview of telemetry
---

# Aperçu de la Télémétrie

Le développement de Grist est guidé par la télémétrie : un ensemble de mesures visant à quantifier les aspects de l'utilisation de Grist. Une installation autogérée de Grist ne fait par défaut aucune télémétrie. Lorsque la télémétrie est activée, les données d'utilisation sont envoyées à un service maintenu par Grist Labs.

La télémétrie peut être configurée par des variables d'environnement optionnelles :

  * `GRIST_TELEMETRY_LEVEL`. Cela peut être `off`, `limited` ou `full`. La valeur par défaut est `off`. Un réglage de `limited` ou `full` entraîne l'envoi de données à un service opéré par Grist Labs. Nous encourageons les utilisateurs à régler la télémétrie sur `limited` afin que leur utilisation soit prise en compte et guide le développement de Grist. Nous ne recommandons un réglage `full` que si vous avez utilisé `GRIST_TELEMETRY_URL` pour rediriger la télémétrie vers un service que vous contrôlez. Cela inclut des identifiants internes à votre installation que nous préférerions ne pas connaître.
  * `GRIST_TELEMETRY_URL`. Cela contrôle où la télémétrie est envoyée. Par défaut, elle est envoyée à un service opéré par Grist Labs. Si vous gérez un grand service hébergé, vous pouvez souhaiter diriger la télémétrie vers un service que vous contrôlez.

La télémétrie peut également être configurée de manière interactive par le propriétaire d'une installation Grist, voir [Comment contrôler la télémétrie ?](self-managed.md#how-do-i-control-telemetry) pour plus de détails.

Le réglage `limited` entraîne une télémétrie à gros grain. Ce niveau est destiné à une installation de Grist qui a choisi de fournir de la télémétrie. L'objectif est de comprendre comment Grist est utilisé "dans la nature" en termes d'utilisation des fonctionnalités et de comptage des ressources, sans partager de données commerciales ou d'informations personnelles identifiables. Voir [télémétrie limitée](telemetry-limited.md) pour les détails de ce qui est exactement envoyé.

Le réglage `full` donne une télémétrie relativement fine. Ce niveau est destiné aux grands services hébergés, tels que celui géré par Grist Labs. Plus d'informations sont enregistrées, pour faciliter la gestion du service et le développement du produit. Aucune information personnelle identifiable n'est incluse. Des identifiants opaques sont inclus qui, en cas de besoin (par exemple en cas de panne de service), pourraient être liés à des informations personnelles via des magasins non télémétriques. Voir [télémétrie complète](telemetry-full.md) pour les détails de ce qui est exactement envoyé.