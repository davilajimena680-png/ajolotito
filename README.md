# Ajolotito Hambriento

## 1. Preparar el proyecto y dependencias

Configuración de dependencias (`flutter_local_notifications`, `timezone`, `shared_preferences`, `app_settings`) y permisos en Android e iOS

![Dependencias del proyecto](assets/dependecias.png)

---

## 2. El reloj y el ajolote (`mascota.dart`)

Rojo: la prueba falla porque `Mascota` y `Humor` todavía no existen[cite: 7, 8].

![Mascota rojo](assets/R02_Prueba_Roja_Mascota.png)

Verde: se implementan `Reloj`, `Mascota` y `Humor` (saciedad, predicción de hambre, alimentar y guardado en JSON), y pasan las pruebas

![Mascota verde](assets/R02_Prueba_Verde_Mascota.png)

---

## 4. Política de buena educación y payload (`politica.dart`, `payload.dart`)

Rojo: la prueba falla porque faltan `PoliticaNotificaciones` (horas de silencio de 22:00 a 08:00 y ajuste de horario) y `PayloadNotif`

![Política y payload rojo](assets/R04_Prueba_Roja_politica_payload.png)

Verde: se implementan `PoliticaNotificaciones` y `PayloadNotif` con validación de formato versionado (`v1:...`), y pasan las pruebas

![Política y payload verde](assets/R04_Prueba_Verde_politica_payload.png)

---

## 6. El planificador (`planificador.dart`)

Rojo: la prueba falla porque `Planificador` e `Ids` todavía no existen

![Planificador rojo](assets/R06_Prueba_Roja_planificador.png)

Verde: se implementa `Planificador` con IDs fijos, respeto a horas de silencio, ventana móvil de sorpresas y tope diario

![Planificador verde](assets/R06_Prueba_Verde_planificador.png)

---

## 8. Gestión de permisos (`gestor_permiso.dart`, `almacen.dart`)

Rojo: la prueba falla porque `GestorPermiso` y `Almacen` todavía no existen

![Permiso rojo](assets/R08_Prueba_Roja_permiso.png)

Verde: se implementa `GestorPermiso` para pedir permiso en contexto una sola vez y guiar a Ajustes si se deniega

![Permiso verde](assets/R08_Prueba_Verde_permiso.png)

---

## 9. El servicio (`servicio.dart`)

Rojo: la prueba falla porque `ServicioAjolote` todavía no existe

![Servicio rojo](assets/R09_Prueba_Roja_servicio.png)

Verde: se implementa `ServicioAjolote` para sincronizar el estado, reprogramar al alimentar y distinguir primer plano de segundo plano

![Servicio verde](assets/R09_Prueba_Verde_servicio.png)

---

## 11. ViewModel y pantallas (`ajolote_vm.dart`, `pantalla_ajolote.dart`)

Rojo: las pruebas del ViewModel y de los widgets de pantalla fallan porque todavía no existen

![ViewModel rojo](assets/R11_Prueba_Roja_vm.png)

![Pantalla rojo](assets/R11_Prueba_Roja_pantalla.png)

Verde: se implementan `AjoloteViewModel`, `DibujoAjolote`, `PantallaAjolote` y `PantallaAjustes`, y pasan las pruebas

![ViewModel verde](assets/R11_Prueba_Verde_vm.png)

![Pantalla verde](assets/R11_Prueba_Verde_pantalla.png)

---

## Suite completa de pruebas

Ejecución de `flutter test` con todas las pruebas unitarias y de widgets pasando en verde[cite: 47, 50].

![Todas las pruebas](<assets/Todas las pruebas.png>)
