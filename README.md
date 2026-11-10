# Quizzes educativos de NeuroMatrona

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24088093.svg)](https://doi.org/10.5281/zenodo.24088093)

**Autora:** Ayleen Bastías, matrona ([ORCID 0009-0008-5954-6821](https://orcid.org/0009-0008-5954-6821)), NeuroMatrona, Chile.

Método, fuentes y verificación de dos herramientas educativas gratuitas en español:

| Quiz | Para qué | Basado en | Verificación |
|---|---|---|---|
| [Quiz SOMP (test de SOP)](https://quiz.neuromatrona.com/) | Ordenar ciclo, andrógenos y ovarios y ver con qué fenotipo (A, B, C o D) calzan las respuestas | Guía internacional de SOP/SOMP 2023 y criterios de Rotterdam | 38 casos clínicos, 10.000 recorridos, 100.000 combinaciones sin incoherencias |
| [Quiz de endometriosis y adenomiosis](https://endometriosis.neuromatrona.com/) | Ordenar el dolor de regla y el sangrado antes de la consulta | ESHRE 2022, FIGO 2018, NICE NG88, ACOG 785 | 39 reglas trazadas a su fuente, 59 casos clínicos, 100.000 recorridos |

**Ninguno diagnostica.** Están basados en guías y probados. El Quiz SOMP tiene además un estudio preliminar de concordancia con la evaluación clínica (abajo); el quiz de endometriosis todavía no.

## Concordancia con la evaluación clínica (v1.1.0)

Estudio retrospectivo preliminar, 42 pacientes que hicieron el Quiz SOMP antes de una sesión clínica, con doble evaluación ciega según los criterios de Rotterdam ([informe completo](quiz-somp/informe-concordancia-quiz-somp.pdf)):

| Medida | Frente a la autora | Frente a una matrona independiente |
|---|---|---|
| Concordancia total | **41/42 (97,6 %)**, IC 95 % 87,7–99,6 | **40/42 (95,2 %)**, IC 95 % 84,2–98,7 |
| Cuando el quiz dio un fenotipo | 17/17 | 17/17 |
| Cuando dio dos fenotipos posibles | 7/7 compatibles | 7/7 compatibles |
| No asignó fenotipo a «no es SOMP» | 8/8 | 7/7 |

Acuerdo entre evaluadoras: 41/42, kappa de Cohen 0,97. Resultados preliminares: requieren confirmación prospectiva. El quiz no diagnostica.

## Contenido

- [`quiz-somp/`](quiz-somp/METODO.md): método, preprint técnico y suplementos.
- [`quiz-endometriosis/`](quiz-endometriosis/METODO.md): método, reglas y fuentes.

## ¿Qué significa «validado»?

Hay tres niveles: validez de contenido (las preguntas salen de guías y las revisa una experta), consistencia
(la misma respuesta da el mismo resultado) y exactitud diagnóstica (el resultado coincide con un diagnóstico
clínico). Estos quizzes cumplen los dos primeros. Explicación completa:
https://neuromatrona.com/tests/test-validado

## Cómo citar

Bastías, A. (2026). *Quizzes educativos de NeuroMatrona: Quiz SOMP (test de SOP) y quiz de endometriosis y adenomiosis. Método, fuentes y verificación* (v1.0.0). Zenodo. https://doi.org/10.5281/zenodo.24088093

## Licencia

Documentos bajo [CC BY 4.0](LICENSE). El código de los quizzes no se publica.

Más información: https://neuromatrona.com/tests
