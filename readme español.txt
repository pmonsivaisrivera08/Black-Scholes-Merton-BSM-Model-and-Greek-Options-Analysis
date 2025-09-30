Modelo Black-Scholes y Analizador de Griegas
Descripción del Proyecto
Este repositorio contiene una implementación completa del Modelo Black-Scholes-Merton (BSM) en Python, diseñado para la valoración teórica de opciones financieras y el cálculo de sus Griegas asociadas.
El proyecto utiliza datos financieros en tiempo real, integrados a través de la librería yfinance, para proporcionar entradas precisas al modelo y permitir la comparación entre los precios teóricos y las cotizaciones actuales del mercado. Es una herramienta esencial para estudiantes de finanzas cuantitativas, traders y analistas que buscan comprender la mecánica de la valoración de opciones y la gestión de riesgos.
Características Principales
El Notebook de Jupyter (Modelo_Black_Scholes_y_Griegas.ipynb) proporciona las siguientes funcionalidades:
* Precios Black-Scholes-Merton (BSM): Calcula el valor razonable de opciones Call y Put de estilo europeo basándose en cinco variables de entrada: precio del subyacente (  ), precio de ejercicio (  ), tiempo hasta el vencimiento (  ), tasa libre de riesgo (  ) y volatilidad (  ).
* Cálculo de las Griegas de Opciones: Calcula las "Griegas", que miden la sensibilidad del precio de la opción a los cambios en los parámetros de entrada:
   * Delta (  ): Sensibilidad al precio del activo subyacente.
   * Gamma (  ): Sensibilidad de Delta al precio del activo subyacente.
   * Theta (  ): Sensibilidad al paso del tiempo (decaimiento temporal).
   * Vega (V): Sensibilidad a la volatilidad.
   * Rho (  ): Sensibilidad a la tasa de interés libre de riesgo.
      * Solucionador de Volatilidad Implícita (IV): Utiliza optimización numérica (scipy.optimize.brentq) para calcular la volatilidad implícita en el precio de mercado de una opción.
      * Integración de Datos de Mercado: Obtiene automáticamente información bursátil actualizada, volatilidad histórica y datos de la cadena de opciones utilizando la librería yfinance.
      * Comparación de Modelos (Inferido): Incluye cálculos y comparaciones, potencialmente contra el Modelo de Precios de Opciones Binomial (como sugiere la salida del notebook), para validar y contrastar diferentes metodologías de valoración.
Requisitos
Para ejecutar este proyecto, necesitará Python 3.x y las siguientes librerías:
Librería
	Descripción
	numpy
	Para operaciones matemáticas de alto nivel y procesamiento de arrays.
	scipy
	Para computación científica, particularmente la distribución norm y el solucionador brentq para IV.
	yfinance
	Para descargar datos de mercado de Yahoo! Finance.
	matplotlib
	Para trazar y visualizar datos (por ejemplo, visualizar las Griegas vs. tiempo/precio).
	Instalación
      1. Clonar el repositorio:
git clone [https://github.com/pmonsivaisrivera08/your-repo-name.git](https://github.com/pmonsivaisrivera08/your-repo-name.git)
cd your-repo-name

      2. Instalar dependencias:
pip install numpy scipy yfinance matplotlib jupyter

      3. Ejecutar el Notebook:
jupyter notebook Modelo_Black_Scholes_y_Griegas.ipynb

Uso
Abra y ejecute las celdas dentro del Notebook Modelo_Black_Scholes_y_Griegas.ipynb. El código está estructurado para:
         1. Definir la clase BlackScholesModel que contiene todas las funciones necesarias.
         2. Obtener los datos de un ticker bursátil (por ejemplo, TSLA).
         3. Calcular la volatilidad histórica para usarla como la    del modelo.
         4. Ingresar los parámetros actuales de la opción (Precio de Ejercicio, Vencimiento, Precio Medio).
         5. Mostrar el precio teórico, las Griegas y la Volatilidad Implícita para el contrato de opción seleccionado.
Autor
Este proyecto fue creado por:
pmonsivaisrivera08
¡No dude en conectar o contribuir!