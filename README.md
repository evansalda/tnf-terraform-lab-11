# CREATION DE L'ENVIRONNEMENT DE RECETTE

On considère que l'infrastructure que vous venez de finaliser est l'environnement de **développement** de votre application.

- Créez maintenant l'environnement de **recette** en utilisant un nouveau fichier de variable nommé **recette.tfvars**

- Le tfstate de cet environnement devra s'appeler **terraform-XX-rec.tfstate** (en remplaçant XX par votre digit).

- L'environnement de recette sera similaire à l'environnement de développement à l'exception des éléments suivants :

    - Le serveur web est de type t2.medium
    - Le serveur web est positionné dans un sous-réseau public différent de celui utilisé en développement
    - La variable **environnement** a pour valeur **rec**

N'oubliez pas de vous servir de la [configuration partielle du backend](https://developer.hashicorp.com/terraform/language/backend#partial-configuration) pour pouvoir gérer vos différents environnements avec le même code.

- Générez un plan d'exécution sur l'environnement de **développement** : Terraform ne devrait rien avoir à faire.