
FUENTE
NPM --HELP

Usage: 

	npm <comando>


Donde <command> es uno de estos:

	add-user, adduser, apihelp, author, bin, bugs, c, cache,                                                             
	completion, config, ddp, dedupe, deprecate, docs, edit,                                                              
	explore, faq, find, find-dupes, get, help, help-search,                                                              
	home, i, info, init, install, isntall, issues, la, link,                                                             
	list, ll, ln, login, ls, outdated, owner, pack, prefix,                                                              
	prune, publish, r, rb, rebuild, remove, repo, restart, rm,                                                           
	root, run-script, s, se, search, set, show, shrinkwrap,                                                              
	star, stars, start, stop, submodule, tag, test, tst, un,                                                             
	uninstall, unlink, unpublish, unstar, up, update, v,                                                                 
	version, view, whoami  


BÁSICO | DETALLE
------ | -------
npm <cmd> -h | quick help con <cmd>
npm -l       | display full usage info
npm faq      | commonly asked questions
npm help <term> | search for help on <term>


NPM INSTALL SYNTAX | EJEMPLO
---------- 				|
npm install 				|
npm install <pkg> 			|
npm install <pkg>@<tag>		|
npm install <pkg>@<version>	|
npm install <pkg>@<version range>	|
npm install <folder>			|                              
npm install <tarball file>|         
npm install <tarball url> |
npm install <git:// url> |
npm install <github username>/<github project> |

Can specify one or more: npm install ./foo.tgz bar@stable /some/folder                                                      
If no argument is supplied and ./npm-shrinkwrap.json is
present, installs dependencies specified in the shrinkwrap.
Otherwise, installs dependencies from ./package.json.


## pendiente:

 - COMANDOS BÁSICOS CHEATSHEET
  	- INSTALAR NPM
    	- INSTALAR PAQUETES
    	- QUE ES PACKAGE.JSON
    	- CREAR PAQUETE
    	- ENLACES DE INTERES

aqui un enlace rápido [video1]

[video1]: https://www.youtube.com/watch?v=uyVXjOsrBTc

Fuentes: 

<https://www.npmjs.org/doc/cli/npm-publish.html>

[Coding from Scratch - 12 - Add README and publish on NPM](https://www.youtube.com/watch?v=uyVXjOsrBTc)

Buen video que explica y recomendable ver todos 

de "Code with David" usuario youtube
