# 🏛️ Data Warehouse de Homicidios en Colombia

En la segunda parte del trabajo en clase de nuestra materia **Introducción al Big Data y sus Aplicaciones**, tuvimos la oportunidad de realizar una creación de un **Data Warehouse (DWH)** estructurado con un **modelo estrella**. El objetivo seria almacenar y analizar información relacionada con homicidios en Colombia gracias a DataLake anteriormente realizado.

---

## 🧱 Arquitectura: Modelo Estrella

El modelo estrella está conformado por:

- Una **tabla de hechos**: `f_homicidios`
- Varias **tablas de dimensión**, relacionadas por claves foráneas

### ⭐ Esquema del modelo estrella


## 🧾 Tablas de Dimensión

| Tabla             | Descripción                              |
|------------------|------------------------------------------|
| dim_departamento | Información de departamentos de Colombia |
| dim_municipios   | Municipios, vinculados a departamentos   |
| dim_fechas       | Fechas completas (día, mes, año)         |
| dim_dias_semana  | Día de la semana                         |
| dim_meses        | Meses del año                            |
| dim_trimestres   | Trimestres del año                       |
| dim_zonas        | Zonas geográficas o rurales/urbanas      |
| dim_sexo         | Género de la víctima                     |


## 📊 Tabla de Hechos: `f_homicidios`

Contiene los registros de homicidios vinculados a las dimensiones mencionadas. Algunos campos típicos incluyen:

- id_fecha
- id_municipio
- id_zona
- id_sexo


## 🔄 Proceso de Carga (ETL)

1. **Creación de tablas** con scripts `*_create.sql`
2. **Inserción de datos** con scripts `*_insert.sql`
3. La tabla `f_homicidios` se alimenta con datos consolidados desde el Data Lake curado.


## 🧰 Herramientas Utilizadas

- **SQLserver**: para la creación de tablas y carga de datos


## 📈 Posibles Consultas de Análisis

- Número de homicidios por año y departamento
- Evolución mensual de homicidios
- Comparación entre zonas rurales y urbanas
- Distribución por género y tipo de zona


