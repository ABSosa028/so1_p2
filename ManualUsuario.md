# Manual de Usuario para el Proyecto "2023 Weather Tweets"

## Introducción

Este manual está diseñado para ayudar a los usuarios a interactuar con el sistema "2023 Weather Tweets", que muestra tweets sobre el clima a nivel mundial. El sistema utiliza una arquitectura distribuida implementada en Kubernetes y tecnologías como Locust, Go, Redis, MongoDB, Kafka, Grafana y Kepler.

## Requisitos Previos

Antes de usar el sistema, asegúrese de tener acceso a:

- Un navegador web moderno (Chrome, Firefox, Edge, Safari).
- La URL del sistema proporcionada por el administrador.

## Instrucciones de Uso

### Acceso al Sistema

1. **Acceder a la URL**:
   - Abra la interface de locus a utilizar.

### Uso de Locust para Pruebas de Carga

1. **Interfaz de Locust**:
   - Acceda a la interfaz de Locust en `http://<locust-ip>:8089`.
   - Ingrese el número de usuarios (clientes concurrentes) y la tasa de aumento (hatch rate) de usuarios por segundo.
   - Haga clic en "Start swarming" para iniciar las pruebas de carga.

### Visualización de Datos en Grafana

1. **Acceso a Grafana**:
   - Diríjase a la URL de Grafana proporcionada por el administrador (por ejemplo, `http://<grafana-ip>:3000`).
   - Inicie sesión con las credenciales proporcionadas.
   - Navegue a los dashboards preconfigurados para visualizar los datos en tiempo real sobre el clima y el consumo de recursos del sistema.

### Interacción con la API

1. **Envío de Tweets**:
   - Use herramientas como `curl` o Postman para enviar solicitudes a la API.
   - Ejemplo de solicitud con `curl`:
     ```sh
     curl -X POST http://<api-ip>/tweets -d '{"texto": "El clima es agradable", "pais": "Guatemala"}'
     ```
   - La API aceptará los datos y los procesará para su almacenamiento y visualización.

### Monitoreo del Consumo de Energía con Kepler

1. **Acceso a Kepler**:
   - Acceda a la interfaz de Kepler en la URL proporcionada por el administrador (por ejemplo, `http://<kepler-ip>:<puerto>`).
   - Visualice el consumo de energía y las emisiones de carbono por Pod en el clúster de Kubernetes.

## Consideraciones de Uso

- **Rendimiento del Sistema**:
  El sistema está diseñado para manejar alta concurrencia. Sin embargo, asegúrese de que las pruebas de carga no excedan los límites establecidos por el administrador.
- **Datos Sensibles**:
  No envíe datos sensibles a través de la API, ya que los tweets y otra información se almacenarán en bases de datos accesibles para monitoreo y análisis.
- **Soporte Técnico**:
  Si encuentra problemas o tiene preguntas, contacte al administrador del sistema o al equipo de soporte técnico.

## Solución de Problemas

### Problemas Comunes

1. **No se puede acceder a la URL del sistema**:

   - Verifique que la URL sea correcta.
   - Asegúrese de que su dispositivo esté conectado a Internet.
   - Contacte al administrador si el problema persiste.

2. **Interfaz de Grafana no muestra datos**:

   - Asegúrese de que los datos se estén enviando correctamente a la API.
   - Verifique que los servicios de Redis y MongoDB estén funcionando.

3. **Error al enviar solicitudes a la API**:
   - Verifique que la URL de la API sea correcta.
   - Asegúrese de que el formato de la solicitud sea válido.

### Contacto de Soporte

Para soporte técnico, puede comunicarse con el equipo responsable del proyecto:

- **Correo Electrónico**: allanbarillass@gmail.com
- **Teléfono**: +502 5862 4710

---

**Referencias**

- [Locust Documentation](https://docs.locust.io/en/stable/)
- [Grafana Documentation](https://grafana.com/docs/)
- [Kepler Documentation](https://sustainable-computing.io/)

Este manual proporciona una guía clara para los usuarios finales sobre cómo interactuar con el sistema "2023 Weather Tweets" de manera efectiva.
