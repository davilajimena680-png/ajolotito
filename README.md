# Ajolotito Hambriento

## 1. Preparar el proyecto y dependencias

Configuración de dependencias (`flutter_local_notifications`, `timezone`, `shared_preferences`, `app_settings`) y permisos en Android e iOS[cite: 5, 6].

![Dependencias del proyecto](assets/dependecias.png)

---

## 2. El reloj y el ajolote (`mascota.dart`)

Rojo: la prueba falla porque `Mascota` y `Humor` todavía no existen[cite: 7, 8].

![Mascota rojo](assets/R02_Prueba_Roja_Mascota.png)

Verde: se implementan `Reloj`, `Mascota` y `Humor` (saciedad, predicción de hambre, alimentar y guardado en JSON), y pasan las pruebas[cite: 7, 9, 10, 11].

![Mascota verde](assets/R02_Prueba_Verde_Mascota.png)

---

## 4. Política de buena educación y payload (`politica.dart`, `payload.dart`)

Rojo: la prueba falla porque faltan `PoliticaNotificaciones` (horas de silencio de 22:00 a 08:00 y ajuste de horario) y `PayloadNotif`[cite: 14, 15, 17].

![Política y payload rojo](assets/R04_Prueba_Roja_politica_payload.png)

Verde: se implementan `PoliticaNotificaciones` y `PayloadNotif` con validación de formato versionado (`v1:...`), y pasan las pruebas[cite: 15, 16, 17].

![Política y payload verde](assets/R04_Prueba_Verde_politica_payload.png)

---

## 6. El planificador (`planificador.dart`)

Rojo: la prueba falla porque `Planificador` e `Ids` todavía no existen[cite: 18, 20].

![Planificador rojo](assets/R06_Prueba_Roja_planificador.png)

Verde: se implementa `Planificador` con IDs fijos, respeto a horas de silencio, ventana móvil de sorpresas y tope diario[cite: 18, 20, 21, 22].

![Planificador verde](assets/R06_Prueba_Verde_planificador.png)

---

## 8. Gestión de permisos (`gestor_permiso.dart`, `almacen.dart`)

Rojo: la prueba falla porque `GestorPermiso` y `Almacen` todavía no existen[cite: 25, 26].

![Permiso rojo](assets/R08_Prueba_Roja_permiso.png)

Verde: se implementa `GestorPermiso` para pedir permiso en contexto una sola vez y guiar a Ajustes si se deniega[cite: 25, 26, 27].

![Permiso verde](assets/R08_Prueba_Verde_permiso.png)

---

## 9. El servicio (`servicio.dart`)

Rojo: la prueba falla porque `ServicioAjolote` todavía no existe[cite: 28, 30].

![Servicio rojo](assets/R09_Prueba_Roja_servicio.png)

Verde: se implementa `ServicioAjolote` para sincronizar el estado, reprogramar al alimentar y distinguir primer plano de segundo plano[cite: 28, 31, 32].

![Servicio verde](assets/R09_Prueba_Verde_servicio.png)

---

## 11. ViewModel y pantallas (`ajolote_vm.dart`, `pantalla_ajolote.dart`)

Rojo: las pruebas del ViewModel y de los widgets de pantalla fallan porque todavía no existen[cite: 37, 41].

![ViewModel rojo](assets/R11_Prueba_Roja_vm.png)

![Pantalla rojo](assets/R11_Prueba_Roja_pantalla.png)

Verde: se implementan `AjoloteViewModel`, `DibujoAjolote`, `PantallaAjolote` y `PantallaAjustes`, y pasan las pruebas[cite: 39, 42, 43, 45].

![ViewModel verde](assets/R11_Prueba_Verde_vm.png)

![Pantalla verde](assets/R11_Prueba_Verde_pantalla.png)

---

## Suite completa de pruebas

Ejecución de `flutter test` con todas las pruebas unitarias y de widgets pasando en verde[cite: 47, 50].

![Todas las pruebas](<assets/Todas las pruebas.png>)
