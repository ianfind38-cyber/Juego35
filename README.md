|# Juego35
 MANUNACHOBENJAIAN
 DOCUMENTO DE GOOGLE: 
 https://docs.google.com/document/d/1GFsjViJiPnZ1obTiey-AY4Ti4-jejEsQxB0f-Myzk28/edit?usp=sharing
https://godotengine.org/download/windows/
Como hacerlo: 
1. Creá un repositorio compartido
Uno del grupo crea un repo en GitHub (o GitLab), gratis y sencillo.
Invita al resto como colaboradores (Settings → Collaborators, en GitHub).
2. Instalá Git en tu máquina
Descargalo de git-scm.com si no lo tenés.
Podés usarlo por consola o con una interfaz gráfica como GitHub Desktop (más fácil para arrancar) o Sourcetree.
3. Configurá el proyecto de Godot para Git

Godot ya guarda los proyectos como archivos de texto (.tscn, .tres, .gd), lo cual es ideal para Git porque se pueden comparar cambios línea por línea. Pero hay que evitar subir carpetas de caché:

Creá un archivo .gitignore en la raíz del proyecto con esto:

.godot/
.import/
export.cfg
export_presets.cfg
*.translation
4. Flujo básico de trabajo
git clone <url-del-repo> — cada uno se baja el proyecto.
git pull — antes de empezar a trabajar, para traer los cambios de los demás.
git add . / git commit -m "mensaje" / git push — para subir tus cambios.
Punto importante: evitar conflictos

Git es genial con código y archivos de texto, pero cuidado con editar la misma escena (.tscn) al mismo tiempo que un compañero — ahí sí puede haber conflictos difíciles de resolver a mano. Lo ideal es dividirse el trabajo por escenas o sistemas distintos (uno hace el jugador, otro el nivel, otro la UI) para minimizar choques.

También existe Godot's built-in "Plugins" o herramientas colaborativas en la nube pero Git sigue siendo el estándar de la industria, así que además les sirve como práctica para el futuro.
