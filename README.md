# GeoRisk-Platform

```text
GeoRisk-platform/
│
├── frontend/                         # 🟦 CAPA DE PRESENTACIÓN
│   ├── src/
│   │   ├── components/               # Componentes reutilizables de UI
│   │   ├── pages/                    # Dashboard, mapa, evaluación, reportes
│   │   ├── services/                 # Consumo de API del backend
│   │   ├── hooks/                    # Hooks personalizados
│   │   ├── types/                    # Tipos/interfaces
│   │   ├── assets/                   # Imágenes, iconos, etc.
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   ├── package.json
│   └── vite.config.js
│
├── backend/                          # 🟨 API / ORQUESTACIÓN
│   ├── app/
│   │   ├── api/
│   │   │   └── routes/
│   │   │       ├── risk.py           # Endpoints de scoring
│   │   │       ├── zones.py          # Endpoints de zonas
│   │   │       ├── maps.py           # Datos para mapa
│   │   │       └── reports.py        # Generación de reportes
│   │   │
│   │   ├── services/
│   │   │   ├── risk_service.py       # Lógica de evaluación
│   │   │   ├── zone_service.py       # Gestión de zonas
│   │   │   └── report_service.py     # Orquestación de reportes
│   │   │
│   │   ├── integrations/             # 🟧 CAPA DE INTEGRACIÓN
│   │   │   ├── sap/
│   │   │   │   ├── datasphere.py     # SAP Datasphere / BDC
│   │   │   │   ├── ai_core.py        # SAP AI Core
│   │   │   │   └── joule.py          # SAP Joule
│   │   │   │
│   │   │   ├── gis/
│   │   │   │   └── gis_client.py     # GIS / datos geográficos
│   │   │   │
│   │   │   └── external/
│   │   │       ├── minem.py          # Fuente MINEM
│   │   │       └── senace.py         # Fuente SENACE
│   │   │
│   │   ├── schemas/
│   │   │   ├── risk_schema.py        # Entrada/salida del scoring
│   │   │   ├── zone_schema.py
│   │   │   └── report_schema.py
│   │   │
│   │   ├── config/
│   │   │   └── settings.py           # Configuración y variables de entorno
│   │   │
│   │   └── main.py                   # Punto de entrada FastAPI
│   │
│   ├── requirements.txt
│   └── Dockerfile
│
├── ml/                               # 🟪 CAPA DE IA
│   ├── src/
│   │   ├── preprocessing.py           # Limpieza/preparación de datos
│   │   ├── features.py                # Variables/features
│   │   ├── train.py                   # Entrenamiento
│   │   ├── predict.py                 # Predicción
│   │   └── evaluate.py                # Métricas del modelo
│   │
│   ├── models/
│   │   └── risk_model.*               # Modelo entrenado
│   │
│   └── notebooks/
│       └── exploration.ipynb          # Exploración/análisis
│
├── data/                             # 🟩 CAPA DE DATOS
│   ├── raw/                           # Dataset original, sin modificar
│   ├── processed/                     # Dataset procesado
│   └── mock/                          # Datos simulados para desarrollo
│
├── docs/                             # 📚 DOCUMENTACIÓN
│   ├── architecture.md               # Arquitectura del sistema
│   ├── model.md                      # Variables, pesos, scoring
│   ├── data-sources.md               # Fuentes de datos
│   ├── legal-rules.md                # Reglas/criterios legales
│   ├── limitations.md                # Limitaciones del modelo
│   └── api-contract.md               # Contrato Backend ↔ Frontend
│
├── tests/                            # 🧪 PRUEBAS
│   ├── backend/
│   ├── ml/
│   └── frontend/
│
├── .env                              # 🔐 Variables de entorno
├── .gitignore
├── README.md                         # 📖 Explicación principal del proyecto
└── docker-compose.yml                # 🐳 Levantar servicios
```



