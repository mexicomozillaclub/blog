# blog
Blog de la comunidad México Mozilla Club

#Pasos para probar tu sitio de github de forma local con Jekyll

Antes de empezar nececitaremos bundler para instalar y correr jekyll. Para instalar jekyll debemos instalar ruby. (https://gorails.com/setup/)

1.- Primero debemos tener git instalado. Si no tienes instalado git, da click aquí https://help.github.com/articles/set-up-git/
2.- Abrimos una terminal
3.- Inicia un nuevo repositiorio de git para el sitio de jekyll
3.- Dirigete al repositorio creado
4.- Si tu nuevo repositorio local es para una pagina de proyecto crea una nueva rama llama gh-pages
5.- Para correr las dependencias de tu sitio, Ruby usará el contenido de tu Gemfile para construir tu sitio. *Si tienes un Gemfile puedes saltarte hasta el paso 8
6.- Si tu no tienes un Gemfile, abre tu editor de textos favorito como Atom, y agrega las siquientes líneas a un nuevo archivo.
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
7.- Nombra al archivo como Gemfile y guárdalo en la carpeta del proyecto de tu repositorio local. Sáltate hasta el paso 9 para instalar Jekyll.
8.- Si ya tienes un Gemfile, abre tu editor de texto y agrega estas líneas a tu Gemfile.
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins.
9.- Instala Jekyll y otras dependencias de la gema de Github Pages:
$ bundle install
Fetching gem metadata from https://rubygems.org/............
Fetching version metadata from https://rubygems.org/...
Fetching dependency metadata from https://rubygems.org/..
Resolving dependencies...
10.- Elimina del Gemfile la siquiente línea:
"jekyll", "3.3.0"
11.- Navega hasta la raíz de la carpeta de tu repositorio y corre tu sitio localmente.
$ bundle exec jekyll serve
Configuration file: /Users/octocat/my-site/_config.yml
           Source: /Users/octocat/my-site
      Destination: /Users/octocat/my-site/_site
Incremental build: disabled. Enable with --incremental
     Generating...
                   done in 0.309 seconds.
Auto-regeneration: enabled for '/Users/octocat/my-site'
Configuration file: /Users/octocat/my-site/_config.yml
   Server address: http://127.0.0.1:4000/
 Server running... press ctrl-c to stop.
12.- Prueba tu nuevo sitio en tu navegador con la dirección localhost://4000.
