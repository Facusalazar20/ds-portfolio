# Segmentación de Clientes con RFM y KMeans

Este proyecto tiene como objetivo analizar el comportamiento de compra de los clientes de un e-commerce mediante el modelo RFM (Recency, Frequency, Monetary) y aplicar clustering con KMeans para segmentarlos en grupos relevantes para estrategias comerciales.

## 📌 Objetivo
Identificar distintos perfiles de clientes para:
- Focalizar acciones de marketing.
- Retener clientes valiosos.
- Reactivar clientes dormidos.
- Entender el comportamiento de compra.

## 🧪 Dataset
El dataset contiene información de transacciones de un e-commerce:
- `InvoiceNo`, `StockCode`, `Description`
- `Quantity`, `UnitPrice`
- `InvoiceDate`, `CustomerID`, `Country`

## 🧹 Procesamiento de datos
- Eliminación de datos nulos e inconsistentes.
- Filtrado de valores negativos (devoluciones).
- Análisis exploratorio de variables clave (`Quantity`, `UnitPrice`).
- Generación de las métricas RFM por cliente.

## 📈 Modelo RFM
- **Recency**: Días desde la última compra.
- **Frequency**: Total de compras realizadas.
- **Monetary**: Monto total gastado.
- Se normalizaron los valores y se aplicó KMeans con 4 clusters.

## 🔍 Resultados

Los clientes se agruparon en 4 clústeres:

| Clúster | Recency | Frequency | Monetary | Interpretación |
|--------:|--------:|----------:|----------:|----------------|
| 1 | 1.0 | 148.0 | 43780.4 | Clientes premium: muy frecuentes y de alto gasto |
| 2 | 12.4 | 18.4 | 5342.5 | Clientes fieles, pero con ticket más bajo |
| 0 | 42.8 | 3.4 | 841.9 | Clientes ocasionales |
| 3 | 245.8 | 1.5 | 310.3 | Clientes dormidos o perdidos |

## 📊 Visualización final

Se generó un gráfico de torta con la distribución de clientes por clúster. Se observó:

- El **clúster 0** representa la mayoría de los clientes, aunque no necesariamente los más rentables.
- El **clúster 1** contiene muy pocos clientes, pero altamente valiosos.
- El **clúster 3** agrupa a clientes inactivos.
- El **clúster 2** tiene un tamaño reducido, pero con potencial de crecimiento.

## 🛠️ Librerías utilizadas

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## 🚀 Cómo ejecutarlo

1. Clonar el repositorio.
2. Instalar las dependencias:
```bash
pip install -r requirements.txt
```
3. Ejecutar el notebook `.ipynb`.

## 📬 Contacto

Facundo Salazar Garzón  
[LinkedIn](https://www.linkedin.com)
