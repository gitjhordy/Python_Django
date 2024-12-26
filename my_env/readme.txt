Seleccionar una carpeta donde estara el proyecto
se recomienda crear el propio entorno virtual con lo siguiente:  " python -m venv my_env" se creara el entorno virtual
Activar el entorno virtual con lo siguiente: " .\my_env\Scripts\activate "

Posterior a ello si se tiene el siguiente error: No se puede cargar el archivo D:\django\my_env\Scripts\Activate.ps1 porque la ejecución de scripts está deshabilitada en este sistema. Para 
obtener más información, consulta el tema about_Execution_Policies en https:/go.microsoft.com/fwlink/?LinkID=135170.
En línea: 1 Carácter: 1
+ .\my_env\Scripts\activate
+ ~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess

"SE SOLUCIONA CON LO SIGUIENTE EN POWER SHELL:"

1: Get-ExecutionPolicy
2: Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
3: Vuelves a ejecutar: .\my_env\Scripts\activate
4: pip install django
5: "Crear" proyecto: django-admin  startproject firstcrud (firstcrud-nommbre del proyecto)
6: Visualizar tu proyecto en el server local dirigete a la ruta y ejecuta lo siguiente: " pyhton manage.py runserver "
7: Para migrar la base de datos se debe ejecutar el siguiente comando: " python manage.py migrate"
8: Si deseas ver la base de datos de SQLite mas amigable puede instalar SQLite Viewer del VisualStudiCode
9: Creación de crud: para iniciar a crear un crud: podemos ejecutar el siguiente miniproyecto: " python manage.py startapp crud"
esto creara un directorio en la raiz principal

Una vez configurado y creado el codigo para crud: se debe ejecutar la migración correspondiente:
" python manage.py makemigrations crud " y python manage.py migrate

