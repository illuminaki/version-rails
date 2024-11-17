Instalar rvm https://rvm.io/rvm/install

Opción 1: Usar Gemsets con RVM
Los gemsets de RVM te permiten gestionar gemas de Ruby de forma aislada, de modo que se pueda tener gemsets diferentes para cada versión de Rails.
Para usar rails 7 se puede usar ciertas versiones de ruby y de igual manera para rails 8 asegurate de tenerlas instaladas con rvm

Crea un gemset para Rails 7:
```bash
rvm gemset create rails7
```

Cambia al gemset de Rails 7:

```bash
rvm use ruby-3.2.2@rails7 --create
```

Instala Rails 7: Ahora, con el gemset rails7 activo, instala la versión específica de Rails 7:

```bash
gem install rails -v 7.0.8.3
```
Crear la aplicación con Rails 7: Ahora puedes crear una aplicación con Rails 7 en cualquier directorio:

```bash
rails _7.0.8.3_ new mi_app_rails7
```

Crea un gemset para Rails 8 (opcional, si no lo has hecho ya): Si no lo has hecho, también puedes crear un gemset específico para Rails 8 para mantener todo separado:
```bash
rvm gemset create rails8
rvm use ruby-3.2.2@rails8 --create
gem install rails --pre
```

Cambiar entre gemsets y versiones de Ruby
Cuando trabajes con gemsets y diferentes versiones de Ruby, simplemente puedes usar el siguiente comando para cambiar al entorno adecuado:

```bash
rvm use ruby-3.2.2@rails7
```
Esto seleccionará la versión de Ruby 3.2.2 junto con el gemset llamado rails7, donde tienes instalada la versión de Rails 7.ç

Del mismo modo, si quieres cambiar al entorno donde tienes Rails 8, debes hacer:

```bash
rvm use ruby-3.2.2@rails8
```

De este modo, todas las gemas (incluyendo la versión de Rails) serán gestionadas de forma aislada en cada gemset, y no tendrás problemas de compatibilidad.


