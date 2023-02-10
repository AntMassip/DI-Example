# DI-Example
Dans cette solution, nous allons voir une architecture en 3 couches avec deux exemples, un avec du code qui est fortement couplé et un autre avec du code faiblement couplé (grace à la DI)

Dans le 1er exemple, le projet UI fait appel aux projets BL et DAL, le projet BL à DAL.

SI l'on veut changer notre projet UI (ASP NET) avec un autre projet UI (WPF par exemple), cela ne pose pas de problème vu qu'aucun autre projet ne dépend de lui.
Par contre si l'on veut changer le projet DAL (Sql Server), cela risque de poser des problèmes vu que les deux autres sont dépendants de lui.

Pour corriger ce problème, partons du principe que l'on ne changera pas notre projet BL, ainsi le projet UI fait référence à BL et le projet DAL à BL.
