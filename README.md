# Productos
Crud de una tabla de Producto, se utilizó .net 7 para la api y la aplicacion web de ASP.NET Core 
Se utilizó EntityFramework en CodeFirst para las migraciones a la BD

luego de crear el dbcontext se genera la coneccion con la bd desde el archivo Program.cs

builder.Services.AddDbContext<ProductoDbContext>(o =>
{
    o.UseSqlServer(builder.Configuration.GetConnectionString("conexion"));
});

En la consola del Administrador de paquetes
add-migration {nombre} -Context {contexto}
remove-migration
update-database {nombre} -Context {contexto}(solo en caso de tener más de un context)
drop-database -Context {contexto}

En el terminal de PowerShell
migrations add {nombre} -c {contexto}
migrations remove
database update {nombre} -c {contexto}(solo en caso de tener más de un context)
database  drop -c {contexto}


