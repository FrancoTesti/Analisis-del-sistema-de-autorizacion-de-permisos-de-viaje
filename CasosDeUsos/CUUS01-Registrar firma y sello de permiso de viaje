# CUUS01 - Registrar firma y sello de permiso de viaje

* **Nivel:** Usuario
* **Alcance:** Sistema
* **Estructura:** Sin estructurar
* **Interacción:** Semántica
* **Instanciación:** Real
* **Meta:** Activar la vigencia del permiso de viaje.
* **Actor Primario:** Representante Legal.
* **Otros:** Sistema de Migraciones (SIMI), Plataforma

---

## Precondiciones

### De negocio
* `<vacío>`

### De sistema
* Documentación requerida registrada y validada.
* El pago debe estar acreditado.

---

## Disparador
Representante Legal atiende a progenitores.

---

## Flujo de Sucesos

### Camino Básico
1. Representante Legal registra la validación de la documentación física en el sistema. Sistema registra la conformidad.
2. Representante Legal solicita generación de permiso. Sistema genera permiso y calcula fechas de vigencia.
3. Representante Legal adjunta documento firmado. Sistema registra archivo, activa vigencia, imprime permiso y notifica al SIMI.

### Caminos Alternativos
* No hay

---

## Postcondiciones

### De sistema
* **De Éxito:** Permiso registrado y activo.
* **De Éxito alternativo:** `<vacío>`
* **De Fracaso:** `<vacío>`

### De Negocio
* **De Éxito:** Progenitores obtienen permiso de viaje para el menor.
* **De Éxito alternativo:** `<vacío>`
* **De Fracaso:** `<vacío>`
