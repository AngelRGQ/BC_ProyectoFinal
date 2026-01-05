#  Agente Autónomo con Q-Learning (Taxi-v3)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Gymnasium](https://img.shields.io/badge/Library-Gymnasium-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

Este repositorio contiene la implementación técnica del *Grupo 2* para el Trabajo Grupal de Fin de Ciclo. El proyecto consiste en el desarrollo de un agente de *Aprendizaje por Refuerzo (Reinforcement Learning)* capaz de resolver el entorno Taxi-v3 de manera autónoma y óptima.

## 📋 Descripción del Proyecto

El objetivo principal es demostrar la viabilidad técnica de los algoritmos de IA en entornos dinámicos sin utilizar datasets estáticos. El agente (un taxi) debe aprender por sí mismo a:
1. Navegar en una rejilla de 5x5.
2. Recoger a un pasajero en una ubicación aleatoria (R, G, Y, B).
3. Dejarlo en su destino correcto en el menor tiempo posible.

Se ha implementado el algoritmo *Q-Learning Tabular* con una estrategia de exploración *Epsilon-Greedy*, logrando que el agente aprenda la política óptima mediante el sistema de recompensas y castigos.

## 🛠️ Tecnologías y Librerías

El proyecto ha sido desarrollado en *Python* utilizando las siguientes herramientas:

* **[Gymnasium](https://gymnasium.farama.org/):** Para la simulación del entorno Taxi-v3.
* *NumPy:* Para el manejo eficiente de la Q-Table y operaciones matemáticas.
* *Matplotlib:* Para la visualización de métricas de desempeño y curvas de aprendizaje.

## 🚀 Instalación y Ejecución

Para replicar los resultados de este proyecto en tu máquina local:

1.  *Clonar el repositorio:*
    bash
    git clone [https://github.com/TU_USUARIO/taxi-qlearning-project.git](https://github.com/TU_USUARIO/taxi-qlearning-project.git)
    cd taxi-qlearning-project
    

2.  *Instalar dependencias:*
    Se recomienda usar un entorno virtual.
    bash
    pip install gymnasium numpy matplotlib
    

3.  *Ejecutar el Notebook:*
    Abre el archivo .ipynb en Jupyter Notebook, JupyterLab o Google Colab y ejecuta las celdas secuencialmente.
    bash
    jupyter notebook PRÁCTICA_TAXI_V3.ipynb
    

## 📊 Metodología (Q-Learning)

El agente utiliza una *Q-Table* de dimensiones 500x6 (500 estados posibles x 6 acciones). La actualización de los valores Q se realiza mediante la *Ecuación de Bellman*:

$$Q(s,a) \leftarrow Q(s,a) + \alpha [R + \gamma \max Q(s',a') - Q(s,a)]$$

### Hiperparámetros Clave:
* *Learning Rate ($\alpha$):* 0.1
* *Discount Factor ($\gamma$):* 0.99
* *Epsilon Inicial:* 1.0 (Decaimiento hasta 0.01)
* *Episodios de Entrenamiento:* 2000

## 📈 Resultados Obtenidos

Tras el entrenamiento de 2000 episodios, el agente fue sometido a una fase de evaluación con los siguientes resultados:

| Métrica | Agente Aleatorio | Agente Entrenado (Q-Learning) |
| :--- | :---: | :---: |
| *Tasa de Éxito* | ~5% | *100%* |
| *Pasos Promedio* | > 200 | *~12.5 (Óptimo)* |
| *Recompensa Media* | Negativa | *Positiva* |

> *Nota:* El agente ha convergido a una solución óptima, eliminando movimientos innecesarios y penalizaciones.

## 👥 Autores - Grupo 2

* *Integrante 1:* [Tu Nombre]
* *Integrante 2:* [Nombre Compañero]
* *Integrante 3:* [Nombre Compañero]
* *Institución:* Escuela Superior Politécnica de Chimborazo (ESPOCH)
* *Carrera:* Software

---
Este proyecto es de fines académicos para la asignatura de Inteligencia Artificial.
