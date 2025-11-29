<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    
  <h1>Polígrafo no invasivo basado en voz</h1>
  <p>
    Proyecto de <strong>detección de engaño (verdad vs mentira)</strong> usando únicamente características acústicas extraídas de audios. Se construye un modelo de clasificación que, a partir de la voz, predice si una respuesta es verdadera (0) o falsa (1).
  </p>

  <h2>Contenido del repositorio</h2>
  <pre>
POLIGRAFO-MAIN/
│
├── implementation/
│   ├── audios/            #Audios recolectados del protocolo (verdad/mentira)
│   ├── dataset.csv        #Dataset final con features + etiqueta
│   ├── dataset.xlsx       #Versión en Excel del dataset
│   └── notebook2.ipynb    #Notebook principal del proyecto
│
└── .gitignore
  </pre>

  <h2>Dataset</h2>
  <p>El dataset del proyecto se encuentra en:</p>
  <ul>
    <li><code>implementation/dataset.csv</code></li>
    <li><code>implementation/dataset.xlsx</code></li>
  </ul>
  <p>Incluye:</p>
  <ul>
    <li>Variables acústicas (features) extraídas de la voz.</li>
    <li>Etiqueta objetivo:
      <ul>
        <li><strong>0 = verdad</strong></li>
        <li><strong>1 = mentira</strong></li>
      </ul>
    </li>
  </ul>

  <h2>Requisitos</h2>
  <div class="box">
    <p>Si no cuentas con un <code>requirements.txt</code>, instala al menos:</p>
    <ul>
      <li>Python 3.9+</li>
      <li>pandas</li>
      <li>numpy</li>
      <li>scikit-learn</li>
      <li>xgboost</li>
      <li>librosa (o librería equivalente para audio)</li>
      <li>matplotlib</li>
    </ul>
  </div>

  <p>Instalación rápida:</p>
  <pre><code>pip install pandas numpy scikit-learn xgboost librosa matplotlib</code></pre>

  <h2>Cómo ejecutar el proyecto</h2>
  <p>
    El análisis principal está en el notebook:
    <strong>implementation/notebook2.ipynb</strong>
  </p>

  <h3>Pasos</h3>
  <ol>
    <li>Abrir Jupyter, collab o VSCode:</li>
  </ol>
  <pre><code>jupyter notebook</code></pre>
  <ol start="2">
    <li>Ir a:</li>
  </ol>
  <pre><code>implementation/notebook2.ipynb</code></pre>
  <ol start="3">
    <li>Ejecutar las celdas en orden:
      <ul>
        <li>Carga del dataset</li>
        <li>Preprocesamiento</li>
        <li>Entrenamiento de modelos</li>
        <li>Evaluación (métricas y matrices de confusión)</li>
      </ul>
    </li>
  </ol>

  <h2>Modelos evaluados</h2>
  <p>En el notebook se comparan varios modelos, entre ellos:</p>
  <ul>
    <li>Baselines lineales / redes simples (descartados por bajo rendimiento)</li>
    <li><strong>Random Forest</strong></li>
    <li><strong>XGBoost</strong></li>
  </ul>

  <h2>Resultados (resumen)</h2>
  <ul>
    <li>Modelos lineales y CNN simple: <strong>&lt; 50% accuracy → descartados</strong></li>
    <li>Mejores modelos: <strong>Random Forest</strong> y <strong>XGBoost</strong></li>
    <li>Accuracy aproximada: <strong>61%</strong></li>
    <li>Random Forest elegido por menor cantidad de falsos positivos.</li>
  </ul>

  <h2>Discusión (resumen)</h2>
  <ul>
    <li>El engaño en voz es difícil de distinguir, por eso el rendimiento es moderado.</li>
    <li>La grabación con celular introduce ruido y variabilidad acústica.</li>
    <li>Aun así, los resultados son consistentes con literatura basada solo en voz.</li>
  </ul>

  <h2>Trabajo futuro</h2>
  <ul>
    <li>Ampliar el dataset.</li>
    <li>Mejorar homogeneidad de audios.</li>
    <li>Probar modelos de audio más robustos y features avanzadas.</li>
  </ul>

  <h2>Autoras</h2>
  <ul>
    <li>Sara Osorio Castaño</li>
    <li>Jessica Yurany Yunda Castillo</li>
    <li>Juliana Areiza Cano</li>
  </ul>

</body>
</html>

