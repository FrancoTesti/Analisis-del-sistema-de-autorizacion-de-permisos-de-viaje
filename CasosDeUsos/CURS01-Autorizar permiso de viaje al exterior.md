# CURS01 - Autorizar permiso de viaje al exterior

* **Nivel:** Resumen
* **Alcance:** Sistema
* **Estructura:** Sin Estructurar
* **Interacción:** Semántica
* **Instanciación:** Real
* **Meta:** Autorizar permiso de viaje al exterior.
* **Actor Primario:** Progenitor/Tutor.
* **Otros:** Representante legal, SIMI.

---

## Precondiciones

### De negocio
* El progenitor cuenta con la documentación necesaria para cargar.

### De sistema
* Sedes de atención, canales de pago y conexión al SIMI registrados y operativos.

---

## Disparador
Progenitor/tutor decide solicitar un permiso de viaje para un menor.

---

## Flujo de Sucesos

### Camino Básico
1. Progenitor/tutor carga la documentación y solicita un turno en el sistema. El sistema valida la edad, registra la solicitud, asigna el turno y guarda la documentación.
2. Representante Legal solicita acceso al expediente del turno. El sistema muestra la documentación digitalizada.
3. Representante Legal solicita generar el permiso de viaje. El sistema genera el permiso calculando fechas de emisión y vencimiento.
4. Representante Legal sube la foto del permiso firmado y sellado en el sistema. El sistema activa la vigencia del documento, lo imprime y notifica al SIMI.

### Caminos Alternativos
* **1.a `<durante>` Sistema detecta que el menor alcanzó la mayoría de edad:**
  * 1.a.1 El sistema informa el rechazo de la solicitud y aborta el trámite. FCU.
* **3.a `<previo>` El pago del sellado se realizó presencialmente:**
  * 3.a.1 Representante Legal escanea y agrega el comprobante. El sistema vincula el pago al expediente. Continúa en paso 3.
* **3.b `<previo>` El pago se realizó por canal digital:**
  * 3.b.1 El sistema verifica y confirma el pago acreditado. Continúa en paso 3.

---

## Postcondiciones

### De sistema
* **De Éxito:** Permiso registrado, activo y notificado al SIMI.
* **De Éxito alternativo:** Permiso registrado y activo con comprobante de pago manual vinculado.
* **De Fracaso:** Solicitud abortada por mayoría de edad.

### De Negocio
* **De Éxito:** Progenitores obtienen la autorización legal de viaje para el menor.
* **De Éxito alternativo:** `<vacío>`
* **De Fracaso:** Solicitud abortada por mayoría de edad.
