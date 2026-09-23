ICN292-LAB3-NOVOA-VICENTE
ICN292 - Laboratorio 3: Automatización de Procesos (AndesHogar SpA)

Autor: Vicente Novoa Rodriguez 
RUT:220455610
Semilla (S):561
Fecha: 23-09-2026

Descripción del Repositorio
Este repositorio contiene la evidencia técnica de la solución de automatización desarrollada para AndesHogar SpA utilizando n8n y Google Sheets, abarcando los flujos de Emisor, Triage y Resumen programado.

Contenido de Archivos y Cómo Reproducirlos

1.Flujo de Triage (Parte A):ICN292-LAB3-Triage.json
Descripción: Workflow principal encargado de recibir solicitudes vía Webhook, evaluar las reglas paramétricas (U = 41.000 y D = 14 días), consultar la API de indicadores económicos y registrar los datos en Google Sheets.
Cómo abrir: Importar este archivo .json en una instancia limpia de n8n. Asegurarse de configurar las credenciales propias de Google Sheets y activar el nodo Webhook o poner el flujo en modo Active.

2. Flujo Emisor: Emisor-ICN292-LAB3.json
Descripción: Workflow simulador que emite el lote de 15 solicitudes de prueba mediante peticiones HTTP POST hacia el webhook de Triage.
Cómo abrir: Importar el .json en n8n y ejecutar manualmente para inyectar las solicitudes de prueba.

3. Flujo Programado de Resumen (Parte B): ICN292-LAB3-Resumen.json
Descripción: Workflow accionado por un *Schedule Trigger* diario (18:00 hrs) que lee la planilla de Google Sheets, agrupa los datos por ruta y consolida el reporte diario.
Cómo abrir:Importar el .json en n8n, ajustar las credenciales de la hoja de cálculo y activar el disparador programado.

4. Informe Técnico: Informe-Lab3-AndesHogar.pdf
   Descripción: Documento formal con el desarrollo completo de la actividad, análisis del MVP y diagnóstico de negocio.
