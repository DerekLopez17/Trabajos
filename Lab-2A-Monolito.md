# Lab 2A — Monolito (JSP/Servlet)
## Objetivos
- Ejecutar un monolito JSP/Servlet.
- Añadir una funcionalidad de negocio sin romper el despliegue.
- Practicar mapeo de servlets, parámetros y salida segura en JSP.

## Setup
1) Importa el proyecto **monolito-jsp** (Jakarta).  
2) `mvn clean package` y despliega `target/monolito-jsp.war` en Tomcat 10+.  
3) Verifica:  
   - `http://localhost:8080/monolito-jsp/`  
   - `http://localhost:8080/monolito-jsp/hello`

## Tareas
1. **Nuevo servlet `CalcServlet` (GET /calc)**  
   - Parámetros: `x`, `y`, `op` ∈ {sum, sub, mul, div}.  
   - Devuelve HTML con el resultado y error controlado si `op` inválida o `div` por 0.
2. **JSP `calc.jsp`** con formulario hacia `/calc`, escapando la salida.  
3. **Navegación**: enlaces desde `index.jsp` a `calc.jsp` y retorno.

## Pruebas mínimas
- (2,3,sum)=5; (7,2,sub)=5; (4,0,div)=error.

## Entregables
- Código fuente modificado (ZIP o repo).
- 3 capturas con casos de prueba.
- Reflexión (5–8 líneas): ventajas/desventajas del monolito al agregar funcionalidad.

## Criterios de aceptación
- `web.xml` mapea `/calc` y responde 200 OK.
- Validación de parámetros y manejo de errores.
- JSP accesible desde la portada.

## Bonus
- Filtro (`Filter`) que loguee tiempo de ejecución y User-Agent en `/calc`.
