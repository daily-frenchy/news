# Daily-frenchy news

<hr/>

-  [Fichiers-et-dossier](#Fichiers-et-dossier)
-  [Premiers-pas](#Premiers-pas)
-  [Prochaines-étapes](#Prochaines-étapes)

<hr/>


## Fichiers-et-dossier

Étant donné que GitHub utilise Jekyll pour afficher les pages, il est essentiel d'utiliser une structure de répertoires que Jekyll comprend. Ce modèle contient le minimum de fichiers dont vous avez besoin pour qu'un site Web soit opérationnel.

<pre>
- _layouts        # dossier pour contenir les modèles HTML
  -- default.html # fichier qui régit la mise en page des pages
- css             # dossier contenant les feuilles de style
  -- main.css     # fichier qui régit l'apparence et la convivialité des pages
- topics          # dossier pour contenir les pages du site Web
  -- page1.html   # une page du site
  -- page2.md     # une autre page
  -- page3.md     # encore une autre
- _config.yml    # informations de configuration de base
- index.html     # page d'accueil du site Web
</pre>

## Premiers-pas

1. Faites défiler vers le haut, localisez le bouton **Utiliser ce modèle** et cliquez dessus.

2. Spécifiez un nom de référentiel. Le nom que vous choisissez sera utilisé dans l'URL de votre site Web, comme ceci : `https://_yourGithubID_.github.io/_repositoryName_`.

3. Cliquez sur **Créer un référentiel à partir d'un modèle**. Les fichiers et dossiers de ce référentiel sont copiés pour vous vers un nouveau référentiel.

4. Dans le nouveau référentiel que vous venez de créer, localisez le bouton **Paramètres** et cliquez dessus. Faites défiler jusqu'à la section intitulée **Pages GitHub** et, dans la liste **Source**, assurez-vous que **branche principale** est sélectionnée.

5. Dans le fichier `_config.yml`, indiquez votre propre nom et remplacez la valeur de `baseurl` par le nom de votre référentiel. Ce nom est le même que celui que vous avez spécifié à l'étape 2 précédemment.

6. Accédez à `https://_yourGithubID_.github.io/_repositoryName_`. Ce que vous voyez sur les pages Web est à peu près le même que ce que vous avez vu sur https://aninditabasu.github.io/jekyll-github-starter-pack. Vous disposez désormais d’un point de départ avec lequel travailler.

7. Revenez à la page **Code** sur l'interface Web de GitHub et modifiez les fichiers afin qu'ils correspondent à votre vision de votre site Web :
   1. Dans le dossier « sujets », modifiez les fichiers « .html » et « .md » comme bon vous semble. Utilisez simplement les balises HTML ou Markdown comme vous le feriez normalement, mais conservez le texte des lignes 1 à 4 tel quel. Ne les touchez pas :slightly_smiling_face: N'hésitez pas à changer quoi que ce soit à partir de la ligne 5.
   2. Dans le dossier racine, modifiez le fichier « index.html », qui est la page de destination de votre site Web, comme bon vous semble. Encore une fois, _ne touchez pas_ les lignes 1 à 4.
6. (Facultatif) Supprimez les fichiers `LICENSE` et `README.md`. Ils sont agréables à avoir pour un dépôt GitHub, mais vous n'en avez pas vraiment besoin pour que votre site Web soit opérationnel.
7. Accédez à `https://_yourGithubID_.github.io/_repositoryName_`. Vous devriez maintenant voir votre propre contenu sur le site Web.

## Prochaines-étapes

1. Ouvrez un fichier dans le dossier `topics` et jouez avec les lignes 1 à 4 :slightly_smiling_face : Cette partie s'appelle `Front Matter` dans le langage Jekyll-Liquid. Les fichiers `topics` > `.html` ou `topics` > `.md` dans ce modèle n'ont que deux entrées pour la présentation :
   - `layout`, dont la valeur dans ce cas est `default`. Cela indique au moteur de construction d'utiliser un fichier appelé « default » du dossier « _layouts » pour afficher la page.
   - `title`, dont la valeur dans ce cas est `page1`. Il s'agit du texte affiché comme titre dans les onglets du navigateur.
   
    Cette introduction est en fait un bloc de code « YAML » et, pour que vos fichiers s'affichent correctement, doit toujours être placé tout en haut du fichier. Vous pouvez spécifier vos propres variables ici et appeler la valeur de ces variables sur la page ultérieurement. Par exemple, vous pouvez définir une variable comme celle-ci : `hit_list : ['Cruella', 'Villanius', 'Voldemort']`, puis choisir chaque élément de cette liste et l'utiliser quelque part sur la page.
  
2. Modifiez le fichier `_layouts` > `default.html` pour jouer avec l'apparence de votre site Web. Si vous avez renommé l'un des fichiers du dossier « topic », n'oubliez pas d'utiliser ces noms dans la section « <nav> » du fichier.
> N'oubliez pas, cependant, que vos fichiers dans le dossier « sujets » sont affichés sous la forme « .html » sur votre site Web. Par conséquent, même si vous avez un fichier nommé « page2.md », si vous l'appelez (le référencez) dans le fichier « default.html », appelez-le comme « page2.html ».

Utilisez le dossier `css` pour placer vos informations de style. Si nécessaire, créez les dossiers `image` et `js` au niveau racine (le même niveau que `css` et `topics`) pour vos images et fichiers JavaScript. Vous pouvez, bien sûr, avoir tous les JavaScript, images et feuilles de style directement au niveau racine (au lieu de les conserver dans des dossiers spéciaux), mais avoir des dossiers séparés pour eux semble un peu moins encombré.

3. Renommez les dossiers « topic » et « css » (et « images » et « js » si vous en avez) et utilisez n'importe quel nom pour tous les fichiers que vous placez dans ces dossiers. Ne renommez simplement pas « _layouts » car ce nom est nécessaire au moteur de construction. De plus, ne renommez ni « _config.yml » ni « index.html ».

À mesure que vous vous familiariserez avec ces fichiers, vous pourrez explorer la documentation de Jekyll pour plus d'informations sur les fichiers et dossiers supplémentaires que vous pouvez utiliser pour votre site Web. Voici quelques ressources :

- Liquide [introduction](https://shopify.github.io/liquid/tags/comment/)
- Jekyll [variables](https://jekyllrb.com/docs/variables/) et [inclut](https://jekyllrb.com/docs/includes/)
