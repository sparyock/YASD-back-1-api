# Semana 1 - Historias de Usuario

## Proyecto: Gestión de Citas Inteligente  
## Repositorio: YASD-back-1-api  
## Responsable: YASD  
## Área trabajada: Backend de usuarios y API Gateway  

---

## HU-01 - Registro de usuario

### Historia de usuario
Como cliente, quiero registrarme en el sistema, para poder acceder a la plataforma de gestión de citas.

### Descripción
Esta historia permite que una persona pueda crear una cuenta dentro del sistema de Gestión de Citas Inteligente.  
El registro es necesario para que posteriormente el usuario pueda iniciar sesión, solicitar turnos y consultar su información.

### Criterios de aceptación
- El sistema debe permitir registrar un usuario con nombre, correo, contraseña y rol.
- El correo del usuario debe ser único.
- El rol debe ser válido dentro del sistema.
- Los roles permitidos son `CLIENTE` y `ADMIN`.
- El usuario debe quedar almacenado en la base de datos correspondiente.
- El endpoint debe funcionar desde el microservicio `users-service`.
- El endpoint debe funcionar desde el `api-gateway`.

### Endpoint principal

**Directo del microservicio:**
`POST http://localhost:8080/users`

**Vía API Gateway:**
`POST http://localhost:8081/users`

**Body de ejemplo:**
```json
{
  "nombre": "Usuario Semana 1",
  "email": "usuariosemanal@test.com",
  "password": "123456",
  "rol": "CLIENTE"
}
