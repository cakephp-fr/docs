Shells
######

AclExtras
=========

Croogo bundles a modified version of AclExtras plugin. The plugin provides
a facility to manage/synchronize or recover your acl tables. The following
commands are available:

**aco_update**

    Add new ACOs for new controllers and actions. Does not remove nodes from        the ACO table.

**aco_sync**

    Perform a full sync on the ACO table.Will create new ACOs or missing
    controllers and actions.Will also remove orphaned entries that no longer
    have a matching controller/action

**aco_sync_contents**

    Perform a full content sync on the ACO table. Will create new ACOs or
    missing contents. Will also remove orphaned entries that no longer have a
    matching contents.

    You need to run this first after activating "Row Level Access Control"

**verify**

    Verify the tree structure of either your Aco or Aro Trees

**recover**

    Recover a corrupted Tree

Install Shell
=============

La plupart des extensions que vous trouverez sur Github.com. Pour installer
l'extension du plugin megamenu à partir de github, tapez::

    $ ./Console/cake install plugin https://github.com/rchavik/megamenu

Ou::

    $ ./Console/cake install plugin rchavik megamenu

Les themes peuvent aussi être installés de la même façon::

    $ ./Console/cake install theme https://github.com/fahad19/themes

Si vous avez un fichier zip localisé ailleurs, tapez::

    $ ./Console/cake install theme http://example.com/mytheme.zip

Ext Shell
=========

Vous pouvez activer/désactiver les plugins et themes à partir de la console.
Pour activer l'extension Megamenu installé précedemment::

    $ ./Console/cake ext activate plugin Megamenu

Pour désactiver::

    $ ./Console/cake ext deactivate plugin Megamenu

Settings Shell
==============

Le plugin Settings fournit quelques utilitaires de commandes pour manipuler
les valeurs de configuration:

- Lire une configuration::

    $ ./Console/cake settings.settings read Site.title

- Ecrire une valeur de configuration::

    $ ./Console/cake settings.settings write Site.title "My Awesome Site"

- Effacer une valeur de configuration::

    $ ./Console/cake settings.settings delete Custom.settingValue

- Mettre à jour une information de la version après un upgrade::

    $ ./Console/cake settings.settings upgrade_version_info

Users Shell
===========

Vous pouvez réinitialiser un mot de passe de l'utilisateur à partir du shell::

    $ ./Console/cake users.users reset admin password
